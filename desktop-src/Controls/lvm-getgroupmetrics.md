---
title: LVM_GETGROUPMETRICS mensaje (Commctrl.h)
description: Obtiene información sobre la presentación de grupos.
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- LVM_GETGROUPMETRICS controles de Windows mensaje
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
ms.openlocfilehash: 4b99996adfe7f26342dde8967c95973fdb972290367328875257f5615f0a43c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062615"
---
# <a name="lvm_getgroupmetrics-message"></a>Mensaje \_ GETGROUPMETRICS de LVM

Obtiene información sobre la presentación de grupos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser **NULL.**</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**estructura LVGROUPMETRICS**</a> que recibe las métricas recuperadas.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





