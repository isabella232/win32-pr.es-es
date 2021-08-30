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
ms.openlocfilehash: 312344248dbf280e1f46d52efd7b4960b47625131d29d30c410939c19b593e5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985385"
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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





