---
description: Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: Elemento idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966964"
---
# <a name="idlfunctiondeclarations-element"></a>Elemento idlFunctionDeclarations

Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.

## <a name="usage"></a>Uso

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Async**](async.md)<br/>         | Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.<br/> <br/>         |
| [**eventArg**](eventarg.md)<br/>   | Especifica si los argumentos de evento relacionados se incluyen en las funciones generadas.<br/> <br/>               |
| [**events**](events.md)<br/>       | Especifica si los eventos relacionados se incluyen en las funciones generadas.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.<br/> <br/> |
| [**Operación**](operation.md)<br/> | Especifica una operación para la que se va a generar código.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>   | Especifica el tipo de puerto para el que se va a generar el código.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**file**](file.md)<br/> | Genera un archivo del generador de código.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este elemento genera declaraciones de funciones miembro correspondientes a las operaciones a las que llama el contrato. Estas declaraciones tienen un formato adecuado para su consumo por parte del compilador midl y se usan generalmente en archivos .idl.

Ejemplo:

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




