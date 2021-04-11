---
description: Especifica un archivo WSDL que se va a procesar para la información del contrato.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: elemento WSDL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb54f946f32fb4962b8384dea7c6cf4b3c0ebe3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276957"
---
# <a name="wsdl-element"></a>elemento WSDL

Especifica un archivo WSDL que se va a procesar para la información del contrato.

## <a name="usage"></a>Uso

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                           | Descripción                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**excludeImport**](excludeimport.md)<br/> | Evita la generación de instrucciones Import para destinos especificados con nombre en un elemento <WSDL: Import> en un archivo WSDL. <br/> <br/> |
| [**importHint**](importhint.md)<br/>       | Especifica la ubicación de descarga de una directiva <WSDL: Import> que no especifica explícitamente una ubicación.<br/> <br/>           |
| [**camino**](path.md)<br/>                   | Archivo y ruta de acceso del archivo de entrada WSDL.<br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                     | Descripción                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código de WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Se omitirán todos los elementos [**importHint**](importhint.md) o [**excludeImport**](excludeimport.md) que aparezcan después del elemento [**path**](path.md) en un archivo de configuración XML.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




