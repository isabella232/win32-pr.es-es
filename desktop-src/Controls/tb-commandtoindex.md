---
title: TB_COMMANDTOINDEX mensaje (Commctrl.h)
description: Recupera el índice de base cero para el botón asociado al identificador de comando especificado.
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- TB_COMMANDTOINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0257f55e01db59f1d23d59583f1ef78f44b1dac1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166885"
---
# <a name="tb_commandtoindex-message"></a>Mensaje \_ COMMANDTOINDEX de TB

Recupera el índice de base cero para el botón asociado al identificador de comando especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando asociado al botón.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero para el botón o -1 si el identificador de comando especificado no es válido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





