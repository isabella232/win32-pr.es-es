---
title: EM_EXLINEFROMCHAR mensaje (Richedit.h)
description: Determina qué línea contiene el carácter especificado en un control de edición enriquecido.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- EM_EXLINEFROMCHAR controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c41f5fbe540a4d765a48292d4ffd5b4af5849681dd1a82f4512b79348a6249d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915645"
---
# <a name="em_exlinefromchar-message"></a>Mensaje \_ EM EXLINEFROMCHAR

Determina qué línea contiene el carácter especificado en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice de base cero del carácter.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el índice de base cero de la línea.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





