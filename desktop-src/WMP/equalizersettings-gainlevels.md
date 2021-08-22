---
title: EQUALIZERSETTINGS.gainLevels
description: El atributo gainLevels especifica o recupera el nivel de ganancia de la banda correspondiente al índice proporcionado.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- EQUALIZERSETTINGS.gainLevels Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb3c00725ebbe75d607636e8b143146dfce9112b4d1a9dacd430a3d61b3cce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838275"
---
# <a name="equalizersettingsgainlevels"></a>EQUALIZERSETTINGS.gainLevels

El **atributo gainLevels** especifica o recupera el nivel de ganancia de la banda correspondiente al índice proporcionado.

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que normalmente oscila entre 20 y +20.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*
</dt> <dd>

**Número**(**long**) entre 1 y 10 que indica el índice de la banda.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este atributo toma un parámetro, pero su valor se especifica en el código de script de la misma manera que otros valores de atributo. No se puede especificar en el elemento EQUALIZERSETTINGS ni se puede usar con el **atributo de escucha wmpprop.** En su lugar, se proporcionan los atributos de nivel de ganancia numerado para estas situaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**Atributos de escucha**](listening-attributes.md)
</dt> </dl>

 

 





