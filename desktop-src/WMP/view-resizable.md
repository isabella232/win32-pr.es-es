---
title: VISTA. redimensionable
description: El atributo de tamaño variable recupera un valor que indica si se puede cambiar el tamaño de la vista.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- VISTA. redimensionable de Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718607"
---
# <a name="viewresizable"></a>VISTA. redimensionable

El atributo de tamaño **variable** recupera un valor que indica si se puede cambiar el tamaño de la **vista** .

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **booleano** de solo lectura con un valor predeterminado igual al atributo **TitleBar** .



| Valores | Descripción             |
|--------|-------------------------|
| true   | Se puede cambiar el tamaño de la vista.    |
| false  | No se puede cambiar el tamaño de la vista. |



 

## <a name="remarks"></a>Observaciones

Si no hay ninguna **TitleBar** y, por tanto, no hay ninguna ventana o borde, debe utilizar el método **size** para cambiar el tamaño del elemento de **vista** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vista**](view-element.md)
</dt> </dl>

 

 





