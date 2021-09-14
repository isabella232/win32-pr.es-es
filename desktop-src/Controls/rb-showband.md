---
title: RB_SHOWBAND mensaje (Commctrl.h)
description: Muestra u oculta una banda determinada en un control rebar.
ms.assetid: 18097aca-e1b4-4359-9d08-4e62406f3f7f
keywords:
- RB_SHOWBAND controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_SHOWBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27c9cedeb42e7eeed9432af9c2a040ac4991810
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167250"
---
# <a name="rb_showband-message"></a>Mensaje \_ SHOWBAND de RB

Muestra u oculta una banda determinada en un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de una banda en el control rebar.

</dd> <dt>

*lParam* 
</dt> <dd>

**Valor BOOL** que indica si se debe mostrar u ocultar la banda. Si este valor es distinto de cero, se mostrará la banda. De lo contrario, la banda se ocultará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





