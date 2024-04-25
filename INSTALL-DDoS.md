## Build DPDK for traffic loader test

```

git clone https://github.com/vincentmli/dpdk.git

cd dpdk

git checkout dpdk-ddos

meson setup -Denable_apps=test-pmd build (build test-pmd app)

ninja -C build

ninja -C build install

ldconfig

dpdk-hugepages.py -p 2M --setup 2G (setup huge page)

dpdk-devbind.py --bind=uio_pci_generic 01:00.0 (bind NIC https://dpdk-guide.gitlab.io/dpdk-guide/setup/binding.html)

```
