---
title: TB_SETDISABLEDIMAGELIST mensaje (Commctrl.h)
description: Establece la lista de imágenes que usará el control de barra de herramientas para mostrar los botones deshabilitados.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- TB_SETDISABLEDIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9125c5e5ac742f4692fc5464cd51c89e111558c4d0004e08d7cef9c862d03cbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167495"
---
# <a name="tb_setdisabledimagelist-message"></a>Mensaje \_ SETDISABLEDIMAGELIST de TB

Establece la lista de imágenes que usará el control de barra de herramientas para mostrar los botones deshabilitados.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes que se establecerá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes usada anteriormente para mostrar los botones deshabilitados, o **NULL** si no se estableció previamente ninguna lista de imágenes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





