---
title: Método AxWindowsMediaPlayer.launchURL
description: El método launchURL envía una dirección URL al explorador predeterminado del usuario que se va a representar. | Método AxWindowsMediaPlayer.launchURL
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- Método launchURL Reproductor de Windows Media
- Método launchURL Reproductor de Windows Media , clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , método launchURL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b4f3ad10a6defe4e7db252a1703888550ff5a89fe2a0d0618dd9886fc5f74bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123995"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a>Método AxWindowsMediaPlayer.launchURL

El método launchURL envía una dirección URL al explorador predeterminado del usuario que se va a representar.

## <a name="syntax"></a>Sintaxis


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System.String que** es la dirección URL que se va a iniciar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método solo abre páginas web mediante los protocolos HTTP o HTTPS.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un botón que, al hacer clic en él, muestra el sitio web de Microsoft en una nueva ventana del explorador. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

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

 

 





