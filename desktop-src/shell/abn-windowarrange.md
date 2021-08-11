---
description: Notifica a una barra de aplicaciones que el usuario ha seleccionado los comandos Cascada, Mosaico horizontal o Mosaico vertical en el menú contextual de la barra de tareas.
title: ABN_WINDOWARRANGE mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 27c679b7ccdb5eb92ebe87676cd136c71adcda862472f6f300056511001a683a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225026"
---
# <a name="abn_windowarrange-message"></a>MENSAJE \_ ABN WINDOWARRANGE

Notifica a una barra de aplicaciones que el usuario ha seleccionado los comandos Cascada, Mosaico horizontal o Mosaico vertical en el menú contextual de la barra de tareas.


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fBeginning* 
</dt> <dd>

Marca que especifica si se está iniciando la operación en cascada o en mosaico. Este parámetro es **TRUE si** la operación se está iniciando y las ventanas aún no se han movido. Es **FALSE si** se ha completado la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El sistema envía este mensaje de notificación dos veces primero con *lParam* establecido en **TRUE** y, después, con *lParam* establecido en **FALSE.** La primera notificación se envía antes de que las ventanas se en cascada o en mosaico, y la segunda se envía después de que se haya producido la operación en cascada o de mosaico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




