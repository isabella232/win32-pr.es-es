---
title: Mensaje de TVM_SETLINECOLOR (commctrl. h)
description: El \_ mensaje TVM SETLINECOLOR establece el color de línea actual.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- TVM_SETLINECOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079483"
---
# <a name="tvm_setlinecolor-message"></a>\_Mensaje de SETLINECOLOR TVM

El mensaje **TVM \_ SETLINECOLOR** establece el color de línea actual.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo color de línea. Use el \_ valor predeterminado de CLR para restaurar los colores predeterminados del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de línea anterior.

## <a name="remarks"></a>Observaciones

Este mensaje solo cambia los colores de línea. Para cambiar los colores de los "+" y "-" dentro de los botones, use el mensaje [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETLINECOLOR**](tvm-getlinecolor.md)
</dt> </dl>

 

 





