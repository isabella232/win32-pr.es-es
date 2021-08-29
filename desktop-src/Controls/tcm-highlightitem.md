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
ms.openlocfilehash: b355b1a0ad4d228fc8f67051497b0327885f7cafc3860af9c74bac0812b344ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876515"
---
# <a name="tcm_highlightitem-message"></a>Mensaje \_ HIGHLIGHTITEM de TCM

Establece el estado de resaltado de un elemento de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ HighlightItem.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **INT** que especifica el índice de base cero de un elemento de control de ficha.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **VALOR BOOL** que especifica el estado de resaltado que se va a establecer. Si este valor es **TRUE,** la pestaña está resaltada; si **es FALSE**, la pestaña se establece en su estado predeterminado. HIWORD [**debe**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

En Comctl32.dll versión 6.0, este mensaje no tiene ningún efecto visible cuando un tema está activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

