---
title: Mensaje de SB_SETBKCOLOR (commctrl. h)
description: Establece el color de fondo de una barra de estado.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422516"
---
# <a name="sb_setbkcolor-message"></a>\_Mensaje SETBKCOLOR de SB

Establece el color de fondo de una barra de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor [**COLORREF**](/windows/desktop/gdi/colorref) que especifica el nuevo color de fondo. Especifique el \_ valor predeterminado de CLR para que la barra de estado use su color de fondo predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de fondo anterior, o el \_ valor predeterminado de CLR si el color de fondo es el color predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

