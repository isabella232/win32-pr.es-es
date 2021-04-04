---
title: Mensaje de PBM_SETRANGE32 (commctrl. h)
description: Establece los valores mínimo y máximo de una barra de progreso en valores de 32 bits y vuelve a dibujar la barra para reflejar el nuevo intervalo.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- PBM_SETRANGE32 controles de mensajes de Windows
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
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803049"
---
# <a name="pbm_setrange32-message"></a>Mensaje de SETRANGE32 de PBM \_

Establece los valores mínimo y máximo de una barra de progreso en valores de 32 bits y vuelve a dibujar la barra para reflejar el nuevo intervalo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de intervalo mínimo. De forma predeterminada, el valor mínimo es cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor de intervalo máximo. Este valor debe ser mayor que *wParam*. De forma predeterminada, el valor máximo es 100.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que contiene el límite inferior de 16 bits anterior en su [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y el límite superior de 16 bits anterior en su [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Si los intervalos anteriores eran valores de 32 bits, el valor devuelto consta de los **LOWORD** s de ambos límites de 32 bits.

## <a name="remarks"></a>Observaciones

Para recuperar los valores de 32 bits altos y bajos completos, use el [**mensaje \_ GETRANGE de PBM**](pbm-getrange.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

