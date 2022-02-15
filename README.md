开发中遇到的问题总结：

1、BottomSheetDialog布局跟随键盘上移，关键配置为设置theme中的windowSoftInputMode属性。核心代码如下：

      BottomSheetDialog dialog = new BottomSheetDialog(context, R.style.BottomSheetDialog);
      dialog.setContentView(R.layout.layout_edit_dlg);
      dialog.show();
                
      <style name="BottomSheetDialog" parent="BottomSheetDialogRoot">
        <item name="android:windowSoftInputMode">stateHidden|adjustResize</item>
        <item name="android:windowIsFloating">false</item>
      </style>
      
效果图：
![image](https://user-images.githubusercontent.com/5469061/154032108-844c4f20-ce7f-4ab2-aa5d-bce8cdd9a7df.png)

