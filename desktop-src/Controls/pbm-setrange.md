---
title: PBM_SETRANGE mensaje (Commctrl.h)
description: Establece los valores mínimo y máximo de una barra de progreso y vuelve a dibujar la barra para reflejar el nuevo intervalo.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- PBM_SETRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5dca4e4be30b50627d8583a67801dc5cb246ef65e9cd267e6d7b3ee3ed7869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170202"
---
# <a name="pbm_setrange-message"></a>Mensaje \_ SETRANGE de PBM

Establece los valores mínimo y máximo de una barra de progreso y vuelve a dibujar la barra para reflejar el nuevo intervalo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el valor de intervalo mínimo y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el valor de intervalo máximo. El valor de intervalo mínimo no debe ser negativo. De forma predeterminada, el valor mínimo es cero. El valor de intervalo máximo debe ser mayor que el valor de intervalo mínimo. De forma predeterminada, el valor de intervalo máximo es 100.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve los valores de intervalo anteriores si se realiza correctamente o cero en caso contrario. LOWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el valor mínimo anterior y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el valor máximo anterior.

## <a name="remarks"></a>Comentarios

Si no establece los valores de intervalo, el sistema establece el valor mínimo en 0 y el valor máximo en 100. Dado que este mensaje expresa el intervalo como un entero de 16 bits sin signo, puede extender de 0 a 65 535. El valor mínimo del intervalo puede oscilar entre 0 y 65 535. Del mismo modo, el valor máximo puede ser de 0 a 65 535.

Para establecer un intervalo mayor, llame [**a PBM \_ SETRANGE32**](pbm-setrange32.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**PBM \_ GETRANGE**](pbm-getrange.md)
</dt> <dt>

[**PBM \_ SETRANGE32**](pbm-setrange32.md)
</dt> </dl>

 

