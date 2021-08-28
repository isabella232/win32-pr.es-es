---
title: AmbientAttributes.height
description: El atributo height especifica o recupera el alto del control.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- AmbientAttributes.height Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbc03f631fffc4d1544906721476f229cbeb926e5d56b08dc1647f2dfd3b243
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098955"
---
# <a name="ambientattributesheight"></a>AmbientAttributes.height

El **atributo height** especifica o recupera el alto del control.

``` syntax
        elementID.height
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** **(long)** que representa el alto del control en píxeles. El valor predeterminado es cero o el alto de la imagen especificada en el atributo **image del** control.

## <a name="remarks"></a>Comentarios

Si el alto especificado es menor que el alto de la imagen proporcionada, se recortará la imagen. Si el alto es mayor que el alto de la imagen, la región de clic superará el límite de la imagen. Independientemente del valor que se le asigna a este atributo, la imagen no puede crecer más allá de su **elemento primario VIEW** o **SUBVIEW.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 





