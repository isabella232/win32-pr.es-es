---
description: Especifica un archivo XSD para procesar la información del contrato.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: elemento xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f790375c34a4d5afc3dc345691c8e26e5f95cebe0bbde283e2986e838cce554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995095"
---
# <a name="xsd-element"></a>elemento xsd

Especifica un archivo XSD para procesar la información del contrato.

## <a name="usage"></a>Uso

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a>Atributos



| Atributo           | Tipo                       | Requerido       | Descripción                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| **path**<br/> | cadena pathname<br/> | Sí<br/> | Archivo y ruta de acceso del archivo de entrada XSD.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                               | Descripción                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [**typeUri**](typeuri.md)<br/> | Especifica un tipo que se va a incluir desde un archivo XSD.<br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
typeUri*
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                     | Descripción                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentarios

La cadena de nombre de archivo también debe incluir información de ruta de acceso completa.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




