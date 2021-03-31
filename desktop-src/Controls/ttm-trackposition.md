---
title: Mensaje de TTM_TRACKPOSITION (commctrl. h)
description: Establece la posición de una información sobre herramientas de seguimiento.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- TTM_TRACKPOSITION controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079523"
---
# <a name="ttm_trackposition-message"></a>TTM \_ TRACKPOSITION

Establece la posición de una información sobre herramientas de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la coordenada x del punto en el que se mostrará la información sobre herramientas de seguimiento, en coordenadas de pantalla. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la coordenada y del punto en el que se mostrará la información sobre herramientas de seguimiento, en coordenadas de pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

El control ToolTip elige dónde Mostrar la ventana de información sobre herramientas en función de las coordenadas proporcionadas con este mensaje. Esto hace que la ventana de información sobre herramientas aparezca junto a la herramienta a la que corresponde. Para que las ventanas de información sobre herramientas se muestren en coordenadas específicas, incluya la \_ marca absoluta ttf en el miembro **uFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) al agregar la herramienta.

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

[**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Usar controles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

