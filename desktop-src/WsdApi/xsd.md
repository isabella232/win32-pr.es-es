---
description: Especifica un archivo XSD para procesar la información de contrato.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: elemento XSD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103909954"
---
# <a name="xsd-element"></a>elemento XSD

Especifica un archivo XSD para procesar la información de contrato.

## <a name="usage"></a>Uso

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a>Atributos



| Atributo           | Tipo                       | Obligatorio       | Descripción                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| **path**<br/> | cadena pathname<br/> | Sí<br/> | Archivo y ruta de acceso del archivo de entrada XSD.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                               | Descripción                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [**typeUri**](typeuri.md)<br/> | Especifica un tipo que se va a incluir de un archivo XSD.<br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
typeUri*
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                     | Descripción                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código de WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Observaciones

La cadena de nombre de archivo debe incluir también la información de ruta de acceso completa.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




