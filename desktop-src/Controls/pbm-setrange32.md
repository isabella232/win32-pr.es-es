---
title: PBM_SETRANGE32 mensaje (Commctrl.h)
description: Establece los valores mínimo y máximo de una barra de progreso en valores de 32 bits y vuelve a dibujar la barra para reflejar el nuevo intervalo.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- PBM_SETRANGE32 controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e29022b4b3cb1c42c8e661e8366324ac10ae9853f104f31722dae8852edf71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169861"
---
# <a name="pbm_setrange32-message"></a>Mensaje \_ SETRANGE32 de PBM

Establece los valores mínimo y máximo de una barra de progreso en valores de 32 bits y vuelve a dibujar la barra para reflejar el nuevo intervalo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de intervalo mínimo. De forma predeterminada, el valor mínimo es cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor máximo del intervalo. Este valor debe ser mayor que *wParam.* De forma predeterminada, el valor máximo es 100.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene el límite inferior de 16 bits anterior en [**su LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y el límite superior de 16 bits anterior en [**su HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Si los intervalos anteriores eran valores de 32 bits, el valor devuelto consta de **loword** de ambos límites de 32 bits.

## <a name="remarks"></a>Comentarios

Para recuperar todos los valores altos y bajos de 32 bits, use el [**mensaje \_ GETRANGE de PBM.**](pbm-getrange.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

