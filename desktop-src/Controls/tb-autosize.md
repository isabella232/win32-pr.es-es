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
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166905"
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

## <a name="remarks"></a>Observaciones

Una aplicación envía el mensaje **\_ TB AUTOSIZE** después de hacer que el tamaño de una barra de herramientas cambie estableciendo el botón o el tamaño del mapa de bits o agregando cadenas por primera vez.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





