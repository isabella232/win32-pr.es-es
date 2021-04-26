---
description: Especifica un archivo WSDL que se procesará para obtener información del contrato.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: elemento wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef4bc7b76ce22184e4c2f1ceaa2131ef163a26d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994712"
---
# <a name="wsdl-element"></a>elemento wsdl

Especifica un archivo WSDL que se procesará para obtener información del contrato.

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
| [**excludeImport**](excludeimport.md)<br/> | Impide la generación de instrucciones de importación para destinos especificados denominados en \<wsdl:import> un elemento de un archivo WSDL. <br/> <br/> |
| [**importHint**](importhint.md)<br/>       | Especifica la ubicación de descarga de una directiva que no especifica \<wsdl:import> explícitamente una ubicación.<br/> <br/>           |
| [**Camino**](path.md)<br/>                   | Archivo y ruta de acceso del archivo de entrada WSDL.<br/> <br/>                                                                                      |



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
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Se omitirán todos los elementos [**importHint**](importhint.md) o [**excludeImport**](excludeimport.md) que aparezcan después del elemento [**path**](path.md) en un archivo de configuración XML.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




