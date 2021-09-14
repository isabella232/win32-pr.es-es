---
title: BUTTONELEMENT.mappingColor
description: El atributo mappingColor especifica o recupera la clave de color que identifica este BUTTONELEMENT en BUTTONGROUP.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- BUTTONELEMENT.mappingColor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889313"
---
# <a name="buttonelementmappingcolor"></a>BUTTONELEMENT.mappingColor

El **atributo mappingColor** especifica o recupera la clave de color que identifica **este ELEMENTO BUTTONELEMENT** en **BUTTONGROUP**.

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene cualquier valor de color Internet Explorer Microsoft. No tiene valor predeterminado.

## <a name="remarks"></a>Observaciones

Este atributo especifica el color de la región en el grupo de botones **mappingImage** que corresponde a este elemento de botón. Todos los clics de esta región se controlan mediante este elemento de botón.

Si se especifica un color no válido, **buttonelement** no se activa.

## <a name="examples"></a>Ejemplos

El ejemplo siguiente es un archivo de definición de máscara completo que muestra cómo se usan algunos de los atributos **BUTTONELEMENT.** Se puede encontrar en el directorio Samples que se instaló con el SDK.


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de color**](color-reference.md)
</dt> <dt>

[**Elemento BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONGROUP.mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





