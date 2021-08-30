---
title: LVM_GETSELECTEDCOLUMN mensaje (Commctrl.h)
description: Recupera un entero que especifica la columna seleccionada.
ms.assetid: 5aba5d96-50fd-439b-9782-fd5d8684b17f
keywords:
- LVM_GETSELECTEDCOLUMN controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d17cb13a98493022b81a86485422e0021b86605bb45bd757067d1d1c9050d92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968265"
---
# <a name="lvm_getselectedcolumn-message"></a>Mensaje DE LVM \_ GETSELECTEDCOLUMN

Recupera un entero que especifica la columna seleccionada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **UINT** que especifica la columna seleccionada.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





