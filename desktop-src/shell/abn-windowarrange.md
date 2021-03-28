---
description: Notifica a una Appbar que el usuario ha seleccionado el comando en cascada, mosaico horizontal o mosaico vertical en el menú contextual de la barra de tareas.
title: Mensaje de ABN_WINDOWARRANGE (ShellAPI. h)
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
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540587"
---
# <a name="abn_windowarrange-message"></a>Mensaje de ABN \_ WINDOWARRANGE

Notifica a una Appbar que el usuario ha seleccionado el comando en cascada, mosaico horizontal o mosaico vertical en el menú contextual de la barra de tareas.


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fBeginning* 
</dt> <dd>

Marca que especifica si se está iniciando la operación Cascade o Tile. Este parámetro es **true** si se está iniciando la operación y las ventanas todavía no se han cambiado. Es **false** si se ha completado la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El sistema envía este mensaje de notificación dos veces primero con *lParam* establecido en **true** y, a continuación, con *lParam* establecido en **false**. La primera notificación se envía antes de que las ventanas estén en cascada o en mosaico, y la segunda se envía después de que se haya realizado la operación Cascade o Tile.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

 




