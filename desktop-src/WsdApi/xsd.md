---
description: Especifica un archivo XSD que se va a procesar para obtener información del contrato.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: elemento xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851ce31230ff88ea2465040c33dc131e0902392c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994552"
---
# <a name="xsd-element"></a>elemento xsd

Especifica un archivo XSD que se va a procesar para obtener información del contrato.

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
| **path**<br/> | pathname string<br/> | Sí<br/> | Archivo y ruta de acceso del archivo de entrada XSD.<br/> <br/> |



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



 

 




