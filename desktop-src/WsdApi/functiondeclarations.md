---
description: Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: elemento functionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508cbac6d220c0ebdee0c6306d5f8a8ab5f26770
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998822"
---
# <a name="functiondeclarations-element"></a>elemento functionDeclarations

Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.

## <a name="usage"></a>Uso

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>         | Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.<br/> <br/>         |
| [**Eventos**](events.md)<br/>       | Especifica si los eventos relacionados se incluyen en las funciones generadas.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.<br/> <br/> |
| [**Operación**](operation.md)<br/> | Especifica una operación para la que se va a generar código.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>   | Especifica el tipo de puerto para el que se va a generar el código.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Este elemento genera declaraciones de funciones miembro correspondientes a las operaciones a las que llama el contrato. Estas declaraciones están en un formato adecuado para su consumo por parte de un compilador de C++ y se usan generalmente en archivos .cpp.

Ejemplo:

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




