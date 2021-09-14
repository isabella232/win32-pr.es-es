---
title: TTM_TRACKPOSITION mensaje (Commctrl.h)
description: Establece la posición de una información sobre herramientas de seguimiento.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- TTM_TRACKPOSITION controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165834"
---
# <a name="ttm_trackposition-message"></a>Mensaje \_ TRACKPOSITION de TTM

Establece la posición de una información sobre herramientas de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Loword [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la coordenada x del punto en el que se mostrará la información sobre herramientas de seguimiento, en coordenadas de pantalla. HIWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la coordenada y del punto en el que se mostrará la información sobre herramientas de seguimiento, en coordenadas de pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

El control de información sobre herramientas elige dónde mostrar la ventana de información sobre herramientas en función de las coordenadas que proporcione con este mensaje. Esto hace que la ventana de información sobre herramientas aparezca junto a la herramienta a la que corresponde. Para que las ventanas de información sobre herramientas se muestren en coordenadas específicas, incluya la marca TTF ABSOLUTE en el \_ **miembro uFlags** de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) al agregar la herramienta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Usar controles de información sobre herramientas](using-tooltip-contro.md)
</dt> </dl>

 

