---
title: Mensaje de PBM_SETRANGE (commctrl. h)
description: Establece los valores mínimo y máximo de una barra de progreso y vuelve a dibujar la barra para reflejar el nuevo intervalo.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- PBM_SETRANGE controles de mensajes de Windows
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
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905422"
---
# <a name="pbm_setrange-message"></a>\_Mensaje de SetRange de PBM

Establece los valores mínimo y máximo de una barra de progreso y vuelve a dibujar la barra para reflejar el nuevo intervalo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el valor de intervalo mínimo y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el valor de intervalo máximo. El valor de intervalo mínimo no debe ser negativo. De forma predeterminada, el valor mínimo es cero. El valor de intervalo máximo debe ser mayor que el valor de intervalo mínimo. De forma predeterminada, el valor de intervalo máximo es 100.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve los valores de intervalo anteriores si se realiza correctamente, o bien cero en caso contrario. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el valor mínimo anterior y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el valor máximo anterior.

## <a name="remarks"></a>Observaciones

Si no establece los valores del intervalo, el sistema establece el valor mínimo en 0 y el valor máximo en 100. Dado que este mensaje expresa el intervalo como un entero sin signo de 16 bits, puede extenderse de 0 a 65.535. El valor mínimo del intervalo puede ser de 0 a 65.535. Del mismo modo, el valor máximo puede ser de 0 a 65.535.

Para establecer un intervalo mayor, llame a [**PBM \_ SETRANGE32**](pbm-setrange32.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GETRANGE de PBM \_**](pbm-getrange.md)
</dt> <dt>

[**SETRANGE32 de PBM \_**](pbm-setrange32.md)
</dt> </dl>

 

