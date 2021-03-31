---
description: Se produce cuando el tamaño de la selección actual ha cambiado, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: Evento InkOverlay. SelectionResized (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf9cbb01821756d830b7c0a24adc55dad11b403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278853"
---
# <a name="inkoverlayselectionresized-event"></a>Evento InkOverlay. SelectionResized

Se produce cuando el tamaño de la selección actual ha cambiado, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .

## <a name="syntax"></a>Sintaxis


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OldSelectionRect* \[ de\]
</dt> <dd>

Rectángulo delimitador de la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) seleccionada tal y como existía antes de que se activara el evento **SelectionResized** .

> [!Note]  
> Este rectángulo se especifica en coordenadas de espacio de tinta, lo que permite escenarios de deshacer.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOESelectionResized.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Selection (propiedad)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**Clase InkRectangle**](inkrectangle-class.md)
</dt> </dl>

 

