# b4x-barcode-scanner-torch
https://www.b4x.com/android/forum/threads/b4x-b4xpages-barcode-reader-with-torch.123781/

```
Sub btnFlash_Click
	If Capturing Then
	#If B4i
	If scanner.TorchMode = scanner.TORCH_OFF Then
		scanner.TorchMode = scanner.TORCH_ON
		btnFlash.Text = "Flash Off"
	Else
		scanner.TorchMode = scanner.TORCH_OFF
		btnFlash.Text = "Flash On"
	End If	
	#Else If B4A		
		'Log(camEx.GetSupportedFlashModes) 'ignore	
		'Log(camEx.GetFlashMode)
		If camEx.GetFlashMode <> "torch" Then
			camEx.SetFlashMode("torch")
			camEx.CommitParameters
			btnFlash.Text = "Flash Off"
		Else
			camEx.SetFlashMode("off")
			camEx.CommitParameters
			btnFlash.Text = "Flash On"
		End If	
	#End If
	End If
End Sub
```
