# DOCKER-VERSION 1.1.0

# Inherit from the base container, which have all the needed script to launch tasks
FROM    ingi/inginious-c-base
LABEL   org.inginious.grading.name="cpp-gcc8-openmpi"

# Install Developer Toolset 8
RUN     yum install -y centos-release-scl && \
        yum-config-manager --enable rhel-server-rhscl-8-rpms && \
        yum install -y openmpi openmpi-devel devtoolset-8-gcc devtoolset-8-gcc-c++ devtoolset-8-gdb devtoolset-8-cpp devtoolset-8-make cmake devtoolset-8-valgrind devtoolset-8-binutils libstdc++ clang clang-analyzer clang-devel llvm automake check check-devel CUnit CUnit-devel zlib-devel openssl-devel time jansson-devel graphviz graphviz-devel cppcheck && \
        yum clean all    

# Make GCC-8 default compiler
ENV	PATH=/opt/rh/devtoolset-8/root/usr/bin${PATH:+:${PATH}}
ENV	MANPATH=/opt/rh/devtoolset-8/root/usr/share/man:${MANPATH}
ENV	INFOPATH=/opt/rh/devtoolset-8/root/usr/share/info${INFOPATH:+:${INFOPATH}}
ENV	PCP_DIR=/opt/rh/devtoolset-8/root
ENV	PERL5LIB=/opt/rh/devtoolset-8/root//usr/lib64/perl5/vendor_perl:/opt/rh/devtoolset-8/root/usr/lib/perl5:/opt/rh/devtoolset-8/root//usr/share/perl5/vendor_perl${PERL5LIB:+:${PERL5LIB}}
ENV	LD_LIBRARY_PATH=/opt/rh/devtoolset-8/root/usr/lib64:/opt/rh/devtoolset-8/root/usr/lib:/opt/rh/devtoolset-8/root/usr/lib64/dyninst:/opt/rh/devtoolset-8/root/usr/lib/dyninst:/opt/rh/devtoolset-8/root/usr/lib64:/opt/rh/devtoolset-8/root/usr/lib${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
ENV	PYTHONPATH=/opt/rh/devtoolset-8/root/usr/lib64/python2.8/site-packages:/opt/rh/devtoolset-8/root/usr/lib/python2.8/site-packages${PYTHONPATH:+:${PYTHONPATH}}
ENV     PATH=/usr/lib64/openmpi/bin${PATH:+:${PATH}}
