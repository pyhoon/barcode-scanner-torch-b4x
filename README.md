# b4x-barcode-scanner-torch
https://www.b4x.com/android/forum/threads/b4x-b4xpages-barcode-reader-with-torch.123781/

```
Sub btnTorch_Click
	If Capturing Then
	#If B4i
		If scanner.TorchMode = scanner.TORCH_OFF Then
			scanner.TorchMode = scanner.TORCH_ON
			btnTorch.Text = "Torch Off"
		Else
			scanner.TorchMode = scanner.TORCH_OFF
			btnTorch.Text = "Torch On"
		End If
	#Else If B4A
		If camEx.GetFlashMode <> "torch" Then
			camEx.SetFlashMode("torch")
			camEx.CommitParameters
			btnTorch.Text = "Torch Off"
		Else
			camEx.SetFlashMode("off")
			camEx.CommitParameters
			btnTorch.Text = "Torch On"
		End If
	#End If
	End If
End Sub
```
