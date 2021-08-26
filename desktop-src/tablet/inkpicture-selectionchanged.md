---
description: Se produce cuando la selección de entrada de lápiz dentro del control InkPicture ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad Selection.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: Evento InkPicture.SelectionChanged (Msalterut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1fce27d9aa0dd043c5e474d790c1bd9737a9c10bffbed3eff6a287be67030f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939005"
---
# <a name="inkpictureselectionchanged-event"></a>Evento InkPicture.SelectionChanged

Se produce cuando la selección de entrada de lápiz dentro del control [InkPicture](inkpicture-control-reference.md) ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

## <a name="syntax"></a>Sintaxis


```C++
void SelectionChanged();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre este evento, consulte el evento [**SelectionChanged**](inkoverlay-selectionchanged.md) del objeto [**InkOverlay,**](inkoverlay-class.md) que tiene la misma funcionalidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Propiedad Selection \[ InkPicture (Control)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> </dl>

 

 




