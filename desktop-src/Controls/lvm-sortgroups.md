---
title: LVM_SORTGROUPS mensaje (Commctrl.h)
description: Usa una función de comparación definida por la aplicación para ordenar los grupos por identificador dentro de un control de vista de lista.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- LVM_SORTGROUPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362635"
---
# <a name="lvm_sortgroups-message"></a>Mensaje \_ LVM SORTGROUPS

Usa una función de comparación definida por la aplicación para ordenar los grupos por identificador dentro de un control de vista de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Puntero a una función de comparación definida por la aplicación, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</dd> <dt>

*lParam* 
</dt> <dd>Puntero Void a la información definida por la aplicación.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 1 si se realiza correctamente o 0 en caso contrario.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

