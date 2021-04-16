---
title: VER. scriptFile
description: El atributo scriptFile especifica los nombres de archivo de los archivos JScript que lo acompañan.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- VIEW. scriptFile Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649991"
---
# <a name="viewscriptfile"></a>VER. scriptFile

El atributo **scriptFile** especifica los nombres de archivo de los archivos JScript que lo acompañan.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de solo escritura sin ningún valor predeterminado. Los nombres de archivo de varios archivos JScript están delimitados por punto y coma. Los espacios iniciales y siguientes y los signos de punto y coma no deben estar presentes.

## <a name="remarks"></a>Observaciones

Cualquier controlador de eventos de la vista puede utilizar el código de los archivos especificados. El código que usan los controladores de eventos en varias vistas puede colocarse en un archivo con el mismo nombre que el archivo de definición de máscara, pero con una extensión. js en lugar de una extensión. WMS. Este archivo se carga automáticamente y no es necesario especificarlo en el archivo de definición de máscara.

## <a name="examples"></a>Ejemplos


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vista**](view-element.md)
</dt> </dl>

 

 





