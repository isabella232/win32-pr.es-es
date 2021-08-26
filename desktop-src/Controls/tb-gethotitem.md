---
title: TB_GETHOTITEM mensaje (Commctrl.h)
description: Recupera el índice del elemento de acceso rápido en una barra de herramientas.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- TB_GETHOTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f33566a586ceaa524f720a9d688897f132ee227950f1f786093150955eafa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918835"
---
# <a name="tb_gethotitem-message"></a>Mensaje \_ GETHOTITEM de TB

Recupera el índice del elemento de acceso rápido en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento de acceso actual o -1 si no se establece ningún elemento de acceso. Los controles de barra de herramientas que no tienen [**el estilo TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) no tienen elementos de acceso rápido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





