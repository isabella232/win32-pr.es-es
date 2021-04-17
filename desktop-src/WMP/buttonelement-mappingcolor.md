---
title: BUTTONELEMENT. mappingColor
description: El atributo mappingColor especifica o recupera la clave de color que identifica este BUTTONELEMENT en BUTTONGROUP.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- BUTTONELEMENT. mappingColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698687"
---
# <a name="buttonelementmappingcolor"></a>BUTTONELEMENT. mappingColor

El atributo **mappingColor** especifica o recupera la clave de color que identifica este **BUTTONELEMENT** en **BUTTONGROUP**.

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene cualquier valor de color de Microsoft Internet Explorer. No tiene valor predeterminado.

## <a name="remarks"></a>Observaciones

Este atributo especifica el color de la región en el grupo de botones **mappingImage** que corresponde a este elemento de botón. Todos los clics en esta región se controlan mediante este elemento de botón.

Si se especifica un color no válido, **BUTTONELEMENT** no se activa.

## <a name="examples"></a>Ejemplos

El ejemplo siguiente es un archivo de definición de máscara completo que muestra cómo se usan algunos de los atributos **BUTTONELEMENT** . Se puede encontrar en el directorio Samples que se instaló con el SDK.


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de color**](color-reference.md)
</dt> <dt>

[**BUTTONELEMENT (elemento)**](buttonelement-element.md)
</dt> <dt>

[**BUTTONGROUP.mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





