---
title: TBM_GETTOOLTIPS mensaje (Commctrl.h)
description: Recupera el identificador del control de información sobre herramientas asignado a la barra de seguimiento, si lo hay.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166466"
---
# <a name="tbm_gettooltips-message"></a>Mensaje \_ GETTOOLTIPS de TBM

Recupera el identificador del control de información sobre herramientas asignado a la barra de seguimiento, si lo hay.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de información sobre herramientas asignado a la barra de seguimiento o **NULL** si la información sobre herramientas no está en uso. Si el control trackbar no usa el estilo [**TBS \_ TOOLTIPS,**](trackbar-control-styles.md) el valor devuelto es **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





