---
title: Mensaje de LB_GETLISTBOXINFO (Winuser. h)
description: Obtiene el número de elementos por columna de un cuadro de lista especificado.
ms.assetid: 925bebd9-2563-4892-a7d7-73d4ef012b42
keywords:
- LB_GETLISTBOXINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETLISTBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f49f96e3f12b1c21e81e8b5358e174e576d07f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079269"
---
# <a name="lb_getlistboxinfo-message"></a>\_Mensaje lb GETLISTBOXINFO

Obtiene el número de elementos por columna de un cuadro de lista especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de elementos por columna.

## <a name="remarks"></a>Observaciones

Este mensaje es equivalente a [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo)
</dt> </dl>

 

 





