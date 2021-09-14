---
title: TCM_HIGHLIGHTITEM mensaje (Commctrl.h)
description: Establece el estado de resaltado de un elemento de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ HighlightItem.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- TCM_HIGHLIGHTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166242"
---
# <a name="tcm_highlightitem-message"></a>Mensaje \_ HIGHLIGHTITEM de TCM

Establece el estado de resaltado de un elemento de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ HighlightItem.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **INT** que especifica el índice de base cero de un elemento de control de pestaña.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **valor BOOL** que especifica el estado de resaltado que se va a establecer. Si este valor es **TRUE**, la pestaña está resaltada; si **es FALSE**, la pestaña se establece en su estado predeterminado. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

En Comctl32.dll versión 6.0, este mensaje no tiene ningún efecto visible cuando un tema está activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

