---
title: Propiedad AxWindowsMediaPlayer.windowlessVideo
description: La propiedad windowlessVideo obtiene o establece un valor que indica si el control Reproductor de Windows Media representa vídeo en modo sin ventanas.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- windowlessVideo, propiedad Reproductor de Windows Media
- Propiedad windowlessVideo Reproductor de Windows Media , clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , propiedad windowlessVideo
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241515"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>Propiedad AxWindowsMediaPlayer.windowlessVideo

La propiedad windowlessVideo obtiene o establece un valor que indica si el control Reproductor de Windows Media representa vídeo en modo sin ventanas.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Valor System.Boolean que indica si el control Reproductor de Windows Media representa el vídeo en modo sin ventanas. El valor predeterminado es false.

## <a name="remarks"></a>Observaciones

De forma predeterminada, un control Reproductor de Windows Media representa vídeo en su propia ventana dentro del área cliente. Cuando **windowlessVideo** se establece en true, el objeto Reproductor de Windows Media representa vídeo directamente en el área cliente, por lo que puede aplicar efectos especiales o aplicar capas de texto al vídeo.

En Windows Vista, la representación de vídeo en modo sin ventanas puede degradar el rendimiento.

No se admite la obtención de un valor para esta propiedad para Netscape Navigator. Establecer un valor para esta propiedad en Netscape Navigator puede producir resultados inesperados.

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

 

 





