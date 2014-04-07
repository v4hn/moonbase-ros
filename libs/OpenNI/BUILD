# print build process
sedit "s:> ':| tee ':; /doxygen/ d" Platform/Linux/CreateRedist/Redist_OpenNi.py &&

sedit "s:USED_LIBS += glut:\0\nUSED_LIBS += GL:" Platform/Linux/Build/Samples/{NiSimpleViewer,NiViewer,NiUserTracker,NiUserSelection,NiHandTracker}/Makefile &&

cd Platform/Linux/CreateRedist &&

bash ./RedistMaker             &&
cd ../Redist/*                 &&

prepare_install                &&
./install.sh                   &&

cp {${SCRIPT_DIRECTORY},.}/libopenni.pc &&
sed -i "s@%VERSION%@${VERSION#*-}@" libopenni.pc &&
install -Dm0644 {.,/usr/lib/pkgconfig}/libopenni.pc
