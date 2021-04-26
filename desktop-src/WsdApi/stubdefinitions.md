---
description: Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: elemento stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42c60b071c901538122751f6e92cfd7049f7be88
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994693"
---
# <a name="stubdefinitions-element"></a>elemento stubDefinitions

Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.

## <a name="usage"></a>Uso

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                         | Descripción                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**deallocator**](deallocator.md)<br/>                   | Especifica el tipo de desasignador que va a usar una función de código auxiliar.<br/> <br/>                                 |
| [**eventArg**](eventarg.md)<br/>                         | Especifica si los argumentos de evento relacionados se incluyen en las funciones generadas.<br/> <br/>               |
| [**Eventos**](events.md)<br/>                             | Especifica si los eventos relacionados se incluyen en las funciones generadas.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>                       | Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.<br/> <br/> |
| [**Operación**](operation.md)<br/>                       | Especifica una operación para la que se va a generar código.<br/> <br/>                                        |
| [**operationDeallocator**](operationdeallocator.md)<br/> | Especifica el tipo de desasignador que va a usar la función de código auxiliar de una operación.<br/> <br/>                    |
| [**portType**](porttype.md)<br/>                         | Especifica el tipo de puerto para el que se va a generar el código.<br/> <br/>                                       |
| [**serverClass**](serverclass.md)<br/>                   | Especifica el nombre de la clase de servidor del lado host.<br/> <br/>                                                |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
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
| Puede estar vacío                        | No            |



 

 




