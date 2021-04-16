---
description: 'Especifica la ubicación de descarga de una directiva <WSDL: Import> que no especifica explícitamente una ubicación.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8da0a7fa45ed00489d405aaba8f1f6d7ab8fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706146"
---
# <a name="importhint-element"></a>elemento importHint

Especifica la ubicación de descarga de una directiva <WSDL: Import> que no especifica explícitamente una ubicación.

## <a name="usage"></a>Uso

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Cód**](location.md)<br/>   | Ubicación del archivo que se va a importar. La ubicación puede ser una ruta de acceso relativa, una ruta de acceso absoluta o una dirección URL HTTP.<br/> <br/> |
| [**System.IO**](namespace.md)<br/> | Espacio de nombres que se va a importar. Debe coincidir con el espacio de nombres especificado en el elemento <WSDL: Import>.<br/> <br/>     |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**mencionados**](wsdl.md)<br/> | Especifica un archivo WSDL que se va a procesar para la información del contrato.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




