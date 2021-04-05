---
title: Mensaje de LB_ITEMFROMPOINT (Winuser. h)
description: Obtiene el índice de base cero del elemento más próximo al punto especificado en un cuadro de lista.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- LB_ITEMFROMPOINT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803416"
---
# <a name="lb_itemfrompoint-message"></a>\_Mensaje lb ITEMFROMPOINT

Obtiene el índice de base cero del elemento más próximo al punto especificado en un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la coordenada x de un punto, con respecto a la esquina superior izquierda del área cliente del cuadro de lista.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la coordenada y de un punto con respecto a la esquina superior izquierda del área cliente del cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto contiene el índice del elemento más cercano en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)). El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es cero si el punto especificado se encuentra en el área cliente del cuadro de lista, o en uno si está fuera del área cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

