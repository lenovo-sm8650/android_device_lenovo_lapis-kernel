# Lenovo Yoga Tab Plus (lapis) kernel prebuilts

From the stock ZUI_17.5.10.362 firmware of the Lenovo Yoga Tab Plus
(TB520FU, codename lapis). The kernel image itself is built from source
(`kernel/lenovo/sm8650`, Android common kernel android14-6.1); these are the
Lenovo and Qualcomm parts without matching public source:

- `dtb/`, `dtbo.img`: device trees. The dtb comes from an installed
  vendor_boot whose region string was changed from ROW to PRC by LTBox.
- `modules/vendor_boot/`, `modules/vendor_dlkm/`: vendor kernel modules
  (unsigned; GKI loads them with MODULE_SIG_PROTECT) and their load lists.
