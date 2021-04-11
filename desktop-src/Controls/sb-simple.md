---
title: Mensaje de SB_SIMPLE (commctrl. h)
description: Especifica si una ventana de estado muestra texto simple o muestra todos los elementos de ventana establecidos por un mensaje SETPARTS de SB anterior \_ .
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150747"
---
# <a name="sb_simple-message"></a>\_Mensaje simple de SB

Especifica si una ventana de estado muestra texto simple o muestra todos los elementos de ventana establecidos por un mensaje [**\_ SETPARTS de SB**](sb-setparts.md) anterior.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca de tipo de presentación. Si este parámetro es **true**, la ventana muestra texto simple. Si es **false**, muestra varias partes.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="remarks"></a>Observaciones

Si la ventana de estado se está cambiando de no simple a simple, o viceversa, la ventana se vuelve a dibujar inmediatamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





