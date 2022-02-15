pushd orocos_kdl &&
mkdir build && cd build &&
cmake -DCMAKE_INSTALL_PREFIX=/usr \
      -DCMAKE_BUILD_TYPE=RELEASE \
      -Wno-dev .. &&
default_make &&
popd &&
devoke_installwatch &&

pushd python_orocos_kdl &&
mkdir build && cd build &&
cmake -DCMAKE_INSTALL_PREFIX=/usr \
      -DCMAKE_BUILD_TYPE=RELEASE \
      -Wno-dev .. &&
default_make &&
popd
