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
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567473"
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



 

## <a name="remarks"></a>Observaciones

Si no hay ninguna **barra de título** y, por lo tanto, no hay ninguna ventana o borde, debe usar el método **size** para cambiar el tamaño del **elemento VIEW.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> </dl>

 

 





