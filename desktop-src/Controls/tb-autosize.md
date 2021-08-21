---
title: TB_AUTOSIZE mensaje (Commctrl.h)
description: Hace que se cambie el tamaño de una barra de herramientas.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- TB_AUTOSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b363546c5a079d2d73a0a3573a582ac27d6348b4db879d6c4371d639021f5d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018733"
---
# <a name="tb_autosize-message"></a>Mensaje \_ DE TAMAÑO AUTOMÁTICO DE TB

Hace que se cambie el tamaño de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Una aplicación envía el mensaje **\_ TB AUTOSIZE** después de hacer que el tamaño de una barra de herramientas cambie estableciendo el tamaño del botón o del mapa de bits o agregando cadenas por primera vez.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





