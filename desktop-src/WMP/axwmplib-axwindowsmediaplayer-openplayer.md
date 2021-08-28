---
title: Método AxWindowsMediaPlayer.openPlayer
description: El método openPlayer se Reproductor de Windows Media con la dirección URL especificada. | Método AxWindowsMediaPlayer.openPlayer
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- Método openPlayer Reproductor de Windows Media
- Método openPlayer Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media método , openPlayer
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a2ae5660969e78aeb165c5f9fd9420ea04c79a6aeec9a57c4627cd61d32ef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764715"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>Método AxWindowsMediaPlayer.openPlayer

El **método openPlayer** se Reproductor de Windows Media mediante la dirección URL especificada.

## <a name="syntax"></a>Sintaxis


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System.String que** es la dirección URL del elemento multimedia que se va a reproducir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método inicia Reproductor de Windows Media con la dirección URL especificada establecida como elemento multimedia actual. Si el reproductor se cerró previamente en modo de máscara, se abrirá con la última máscara elegida por el usuario. De lo contrario, el reproductor se abre en modo completo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





