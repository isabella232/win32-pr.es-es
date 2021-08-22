---
title: TB_ISBUTTONPRESSED mensaje (Commctrl.h)
description: Determina si se presiona el botón especificado en una barra de herramientas.
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- TB_ISBUTTONPRESSED controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187b7dd6c39fb972d53391dcbd67d7b45bb895a2e521fa8db22c2a7a411c05e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503645"
---
# <a name="tb_isbuttonpressed-message"></a>Mensaje \_ ISBUTTONPRESSED de TB

Determina si se presiona el botón especificado en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se presiona el botón o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





