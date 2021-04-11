---
description: Se produce cuando la posición de la selección actual está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: Evento InkPicture. SelectionMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2dbc0064e22f21faf80d67f51ca1eeb58b6433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083315"
---
# <a name="inkpictureselectionmoving-event"></a>Evento InkPicture. SelectionMoving

Se produce cuando la posición de la selección actual está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .

## <a name="syntax"></a>Sintaxis


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CurSelectionRect* \[ de\]
</dt> <dd>

Rectángulo al que se mueve la selección después del evento **SelectionMoving** .

> [!Note]  
> Este rectángulo se especifica en coordenadas de la ventana del cliente, lo que permite escenarios como el mantenimiento de la relación de aspecto al cambiar el tamaño.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las interfaces de solo envío **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** (dispinterfaces) con un identificador de DISPID \_ IOESelectionMoving.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Propiedad de selección \[ InkPicture (control)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**Clase InkRectangle**](inkrectangle-class.md)
</dt> </dl>

 

 




