---
title: Propiedad AxWindowsMediaPlayer.versionInfo
description: La propiedad versionInfo obtiene un valor que especifica la versión del Reproductor de Windows Media.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- propiedad versionInfo Reproductor de Windows Media
- Propiedad versionInfo Reproductor de Windows Media , clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , propiedad versionInfo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd7491af0fc102f03da9855b78ecef79ac0a09ca9b3ab8b49f9bf6b948f0d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118841166"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a>Propiedad AxWindowsMediaPlayer.versionInfo

La propiedad versionInfo obtiene un valor que especifica la versión del Reproductor de Windows Media.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a>Valor de propiedad

System.String que es la información de versión en el formato siguiente: "*X*.0.0. *YYYY "* donde *X* representa el número de versión principal y *YYYY representa* el número de compilación.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un botón que, al hacer clic en él, muestra un cuadro de mensaje que contiene la información de versión de Reproductor de Windows Media. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





