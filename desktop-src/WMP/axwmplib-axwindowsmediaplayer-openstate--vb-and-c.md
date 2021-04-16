---
title: Propiedad AxWindowsMediaPlayer. openState
description: La propiedad openState obtiene un valor de enumeración que indica el estado del origen de contenido.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- propiedades de openState Media Player de Windows
- propiedad openState Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad openState
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699392"
---
# <a name="axwindowsmediaplayeropenstate-property"></a>Propiedad AxWindowsMediaPlayer. openState

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

El valor de enumeración WMPLib. WMPOpenState.

## <a name="remarks"></a>Observaciones

No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado. Además, no todos los Estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de los Estados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer. OpenStateChange**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**WMPLib.WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





