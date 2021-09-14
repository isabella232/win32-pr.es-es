---
title: TB_GETTOOLTIPS mensaje (Commctrl.h)
description: Recupera el identificador del control de información sobre herramientas, si lo hay, asociado a la barra de herramientas.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- TB_GETTOOLTIPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166742"
---
# <a name="tb_gettooltips-message"></a>Mensaje \_ DE TB GETTOOLTIPS

Recupera el identificador del control de información sobre herramientas, si lo hay, asociado a la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de información sobre herramientas o **NULL si** la barra de herramientas no tiene información sobre herramientas asociada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





