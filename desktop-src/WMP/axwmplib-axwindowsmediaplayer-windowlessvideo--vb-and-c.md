---
title: Propiedad AxWindowsMediaPlayer. windowlessVideo
description: La propiedad windowlessVideo obtiene o establece un valor que indica si el control de Windows Media Player representa el vídeo en el modo sin ventanas.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- propiedades de windowlessVideo Media Player de Windows
- propiedad windowlessVideo Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad windowlessVideo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700392"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>Propiedad AxWindowsMediaPlayer. windowlessVideo

La propiedad windowlessVideo obtiene o establece un valor que indica si el control de Windows Media Player representa el vídeo en el modo sin ventanas.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Un valor System. Boolean que indica si el control de Media Player de Windows representa el vídeo en modo sin ventanas. El valor predeterminado es false.

## <a name="remarks"></a>Observaciones

De forma predeterminada, un control incrustado de Windows Media Player representa el vídeo en su propia ventana dentro del área cliente. Cuando **windowlessVideo** se establece en true, el objeto de Media Player de Windows representa el vídeo directamente en el área de cliente, de modo que puede aplicar efectos especiales o capas del vídeo con texto.

En Windows Vista, la representación de vídeo en el modo sin ventanas puede degradar el rendimiento.

La obtención de un valor para esta propiedad no es compatible con Netscape Navigator. Establecer un valor para esta propiedad en Netscape Navigator puede producir resultados inesperados.

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

 

 





