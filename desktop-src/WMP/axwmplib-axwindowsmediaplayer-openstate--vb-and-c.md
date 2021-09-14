---
title: Propiedad AxWindowsMediaPlayer.openState
description: La propiedad openState obtiene un valor de enumeración que indica el estado del origen de contenido.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- propiedad openState Reproductor de Windows Media
- propiedad openState Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , propiedad openState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889681"
---
# <a name="axwindowsmediaplayeropenstate-property"></a>Propiedad AxWindowsMediaPlayer.openState

La propiedad openState obtiene un valor de enumeración que indica el estado del origen de contenido.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a>Valor de propiedad

Valor de enumeración WMPLib.WMPOpenState.

## <a name="remarks"></a>Observaciones

Reproductor de Windows Media se garantiza que los estados se produzcan en un orden determinado. Además, no todos los estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer.OpenStateChange**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**WMPLib.WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





