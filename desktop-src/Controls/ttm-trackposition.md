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
ms.openlocfilehash: 547af5014bbf897d320894c4924911b830997ec3d8532e2ce2c7b63f361a11da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542843"
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

## <a name="remarks"></a>Comentarios

El control de información sobre herramientas elige dónde mostrar la ventana de información sobre herramientas en función de las coordenadas que proporcione con este mensaje. Esto hace que la ventana de información sobre herramientas aparezca junto a la herramienta a la que corresponde. Para que las ventanas de información sobre herramientas se muestren en coordenadas específicas, incluya la marca TTF ABSOLUTE en el \_ **miembro uFlags** de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) al agregar la herramienta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Usar controles de información sobre herramientas](using-tooltip-contro.md)
</dt> </dl>

 

