---
title: VIEW.resizable
description: El atributo que se puede cambiar de tamaño recupera un valor que indica si se puede cambiar el tamaño de VIEW.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- View.resizable Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 622c732ce6a1218fa16bbe70c1ef18d53ba4211abfde9d39fc794ec862348033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332913"
---
# <a name="viewresizable"></a>VIEW.resizable

El **atributo que se puede cambiar** de tamaño recupera un valor que indica si se puede cambiar el tamaño de **VIEW.**

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor **booleano** de solo lectura con un valor predeterminado igual al atributo **titlebar.**



| Valores | Descripción             |
|--------|-------------------------|
| true   | Se puede cambiar el tamaño de la vista.    |
| false  | No se puede cambiar el tamaño de la vista. |



 

## <a name="remarks"></a>Comentarios

Si no hay ninguna **barra de título** y, por lo tanto, no hay ninguna ventana o borde, debe usar el método **size** para cambiar el tamaño del **elemento VIEW.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> </dl>

 

 





