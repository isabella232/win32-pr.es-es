---
title: TB_SETCMDID mensaje (Commctrl.h)
description: Establece el identificador de comando de un botón de la barra de herramientas.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- TB_SETCMDID controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166645"
---
# <a name="tb_setcmdid-message"></a>Mensaje \_ SETCMDID de TB

Establece el identificador de comando de un botón de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del botón cuyo identificador de comando se va a establecer.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del comando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





