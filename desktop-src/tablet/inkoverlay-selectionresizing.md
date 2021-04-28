---
description: 'Evento InkOverlay.SelectionResizing: se produce cuando el tamaño de la selección actual está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad Selection.'
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: Evento InkOverlay.SelectionResizing (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b5577f83c14ccc2e998fb4257344729e2219a2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086683"
---
# <a name="inkoverlayselectionresizing-event"></a>Evento InkOverlay.SelectionResizing

Se produce cuando el tamaño de la selección actual está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

## <a name="syntax"></a>Sintaxis


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CurSelectionRect* \[ En\]
</dt> <dd>

Rectángulo delimitador de la selección después del **evento SelectionResizing.**

> [!Note]  
> Este rectángulo se especifica en coordenadas de ventana de cliente, lo que permite escenarios como mantener la relación de aspecto al cambiar el tamaño.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo distribución \_ (dispinterfaces) de IInkOverlayEvents e IInkPictureEvents con un identificador \_ de DISPID \_ IOESelectionResizing.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Propiedad Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**InkRectangle (clase)**](inkrectangle-class.md)
</dt> </dl>

 

 




