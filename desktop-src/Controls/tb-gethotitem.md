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
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166822"
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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





