obj-$(CONFIG_ZSTD_COMPRESS) += zstd_compress.o
obj-$(CONFIG_ZSTD_DECOMPRESS) += zstd_decompress.o

ccflags-y += -O3

# optimise for size
ccflags-y += $(call cc-option, -g0)
ccflags-y += $(call cc-option, -Os)

zstd_compress-y := fse_compress.o huf_compress.o compress.o \
		   entropy_common.o fse_decompress.o zstd_common.o
zstd_decompress-y := huf_decompress.o decompress.o \
		     entropy_common.o fse_decompress.o zstd_common.o
