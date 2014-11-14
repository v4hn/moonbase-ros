cd Platform/Linux/CreateRedist &&

bash ./RedistMaker             &&
cd ../Redist/*                 &&

prepare_install                &&
./install.sh                   &&

cp {${SCRIPT_DIRECTORY},.}/libopenni.pc &&
sed -i "s@%VERSION%@${VERSION#*-}@" libopenni.pc &&
install -Dm0644 {.,/usr/lib/pkgconfig}/libopenni.pc
