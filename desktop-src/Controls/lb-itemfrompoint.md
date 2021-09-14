---
title: LB_ITEMFROMPOINT mensaje (Winuser.h)
description: Obtiene el índice de base cero del elemento más cercano al punto especificado en un cuadro de lista.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- LB_ITEMFROMPOINT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061875"
---
# <a name="lb_itemfrompoint-message"></a>Mensaje \_ LB ITEMFROMPOINT

Obtiene el índice de base cero del elemento más cercano al punto especificado en un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la coordenada x de un punto, en relación con la esquina superior izquierda del área cliente del cuadro de lista.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la coordenada y de un punto, en relación con la esquina superior izquierda del área cliente del cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto contiene el índice del elemento más cercano en [**loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)). HIWORD [**es**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) cero si el punto especificado está en el área de cliente del cuadro de lista o uno si está fuera del área de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

