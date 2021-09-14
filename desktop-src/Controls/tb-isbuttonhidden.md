---
title: TB_ISBUTTONHIDDEN mensaje (Commctrl.h)
description: Determina si el botón especificado en una barra de herramientas está oculto.
ms.assetid: 3372a64f-8209-4e3f-a6a9-8fe2e7e87ff2
keywords:
- TB_ISBUTTONHIDDEN controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIDDEN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db36f289a05fecfb2a0795965820324a9ce68057
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166706"
---
# <a name="tb_isbuttonhidden-message"></a>Mensaje \_ ISBUTTONHIDDEN de TB

Determina si el botón especificado en una barra de herramientas está oculto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si el botón está oculto o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





