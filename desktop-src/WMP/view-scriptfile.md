---
title: VIEW.scriptFile
description: El atributo scriptFile especifica los nombres de archivo de los archivos JScript adjuntos.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- VIEW.scriptFile Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070765"
---
# <a name="viewscriptfile"></a>VIEW.scriptFile

El **atributo scriptFile** especifica los nombres de archivo de los archivos JScript adjuntos.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de solo **escritura** sin ningún valor predeterminado. Los nombres de archivo de varios JScript se delimitan con punto y coma. Los espacios iniciales y siguientes y los puntos y coma no deben estar presentes.

## <a name="remarks"></a>Observaciones

Cualquier controlador de eventos de la vista puede usar el código de los archivos especificados. El código que usan los controladores de eventos en varias vistas se puede colocar en un archivo con el mismo nombre que el archivo de definición de máscara, pero con una extensión .js en lugar de una extensión .wms. Este archivo se carga automáticamente y no es necesario especificarlo en el archivo de definición de máscara.

## <a name="examples"></a>Ejemplos


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> </dl>

 

 





