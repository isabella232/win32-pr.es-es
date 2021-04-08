---
title: Mensaje de LVM_GETGROUPMETRICS (commctrl. h)
description: Obtiene información acerca de la presentación de grupos.
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- LVM_GETGROUPMETRICS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5af8ec50fe74ab90a0f3e44a69e2cbc7dda583e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996918"
---
# <a name="lvm_getgroupmetrics-message"></a>\_Mensaje GETGROUPMETRICS LVM

Obtiene información acerca de la presentación de grupos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser **null**.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> que recibe las métricas recuperadas.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





