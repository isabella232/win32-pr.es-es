---
description: Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: elemento proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9f03834ca59ede41f2f3c3dff00d7dacdd54db
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995762"
---
# <a name="proxyfunctionimplementations-element"></a>elemento proxyFunctionImplementations

Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.

## <a name="usage"></a>Uso

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                     | Descripción                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>           | Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.<br/> <br/>         |
| [**Eventos**](events.md)<br/>         | Especifica si los eventos relacionados se incluyen en las funciones generadas.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>   | Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.<br/> <br/> |
| [**Operación**](operation.md)<br/>   | Especifica una operación para la que se va a generar código.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>     | Especifica el tipo de puerto para el que se va a generar el código.<br/> <br/>                                       |
| [**proxyClass**](proxyclass.md)<br/> | Especifica el nombre de la clase de proxy del lado cliente.<br/> <br/>                                               |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Genera un archivo del generador de código.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




