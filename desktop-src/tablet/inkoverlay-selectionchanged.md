---
description: Se produce cuando la selección de entrada de lápiz dentro del control ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad Selection.
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: Evento InkOverlay.SelectionChanged (Msalterut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bbe4e239b1100277adea0b784a93bf16bf8497cfd8dd44877f7fe7e3fd7652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218978"
---
# <a name="inkoverlayselectionchanged-event"></a>Evento InkOverlay.SelectionChanged

Se produce cuando la selección de entrada de lápiz dentro del control ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

## <a name="syntax"></a>Sintaxis


```C++
void SelectionChanged();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

No hay datos de eventos.

Este método de evento se define en las interfaces de solo distribución \_ (dispinterfaces) de IInkOverlayEvents e \_ IInkPictureEvents con un identificador de DISPID \_ IOESelectionChanged.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Propiedad Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

 




