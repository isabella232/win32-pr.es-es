---
title: LVM_SETGROUPMETRICS mensaje (Commctrl.h)
description: Establece información sobre la presentación de grupos.
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- LVM_SETGROUPMETRICS controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215962e6f84aac83a2151b46f489938b575303c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061794"
---
# <a name="lvm_setgroupmetrics-message"></a>Mensaje \_ SETGROUPMETRICS de LVM

Establece información sobre la presentación de grupos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser **NULL.**</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**estructura LVGROUPMETRICS**</a> que contiene las métricas que se establecerán.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





