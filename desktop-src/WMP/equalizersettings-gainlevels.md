---
title: EQUALIZERSETTINGS.gainLevels
description: El atributo gainLevels especifica o recupera el nivel de ganancia de la banda correspondiente al índice proporcionado.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- EQUALIZERSETTINGS. gainLevels Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699446"
---
# <a name="equalizersettingsgainlevels"></a>EQUALIZERSETTINGS.gainLevels

El atributo **gainLevels** especifica o recupera el nivel de ganancia de la banda correspondiente al índice proporcionado.

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**float**) con un valor que normalmente oscila entre 20 y + 20.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*la banda*
</dt> <dd>

**Número**(**largo**) entre 1 y 10 que indica el índice de la banda.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este atributo toma un parámetro, pero su valor se especifica en el código de script de la misma manera que otros valores de atributo. No se puede especificar en el elemento EQUALIZERSETTINGS, ni puede usarse con el atributo de escucha **wmpprop** . En su lugar, se proporcionan los atributos de nivel de ganancia numerado para estas situaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**Atributos de escucha**](listening-attributes.md)
</dt> </dl>

 

 





