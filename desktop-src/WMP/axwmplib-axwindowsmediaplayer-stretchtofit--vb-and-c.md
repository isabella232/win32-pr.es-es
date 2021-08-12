---
title: Propiedad AxWindowsMediaPlayer.stretchToFit
description: La propiedad stretchToFit obtiene o establece un valor que indica si el vídeo mostrado por el control Reproductor de Windows Media cambia automáticamente de tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- StretchToFit, propiedad Reproductor de Windows Media
- Propiedad stretchToFit Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media propiedad , stretchToFit
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3090889207e0631fbc2f35613398b4c979f4c907cfe240e9f0a7374c74b00b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581515"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>Propiedad AxWindowsMediaPlayer.stretchToFit

La propiedad stretchToFit obtiene o establece un valor que indica si el vídeo mostrado por el control Reproductor de Windows Media cambia automáticamente de tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Valor System.Boolean que indica si el vídeo se ajustará para ajustarse a la ventana. El valor predeterminado es false.

## <a name="remarks"></a>Comentarios

Cuando **stretchToFit** se establece en true, el control Reproductor de Windows Media mantiene la relación de aspecto original del vídeo. Si la relación de aspecto del vídeo no coincide con la relación de aspecto de la ventana de vídeo, las áreas de máscara negra pueden aparecer en la parte superior e inferior, o en la izquierda y derecha, de la imagen de vídeo.

Esta propiedad se aplica al control Reproductor de Windows Media solo cuando se inserta en una página web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





