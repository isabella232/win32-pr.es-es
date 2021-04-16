---
title: Propiedad AxWindowsMediaPlayer. stretchToFit
description: La propiedad stretchToFit obtiene o establece un valor que indica si el vídeo mostrado por el control Media Player de Windows ajusta automáticamente su tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- propiedades de stretchToFit Media Player de Windows
- propiedad stretchToFit Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad stretchToFit
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
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699956"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>Propiedad AxWindowsMediaPlayer. stretchToFit

La propiedad stretchToFit obtiene o establece un valor que indica si el vídeo mostrado por el control Media Player de Windows ajusta automáticamente su tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

El valor System. Boolean que indica si el vídeo se ajustará para ajustarse a la ventana. El valor predeterminado es false.

## <a name="remarks"></a>Observaciones

Cuando **stretchToFit** se establece en true, el control de Media Player de Windows mantiene la relación de aspecto original del vídeo. Si la relación de aspecto del vídeo no coincide con la relación de aspecto de la ventana de vídeo, pueden aparecer áreas de máscara negra en la parte superior e inferior, o izquierda y derecha, de la imagen de vídeo.

Esta propiedad solo se aplica al control Media Player de Windows cuando se incrusta en una página web.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





