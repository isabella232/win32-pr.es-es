---
description: Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: elemento stubDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ceaa8871928031edff90db0491483cfd06bdcc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717291"
---
# <a name="stubdeclarations-element"></a>elemento stubDeclarations

Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.

## <a name="usage"></a>Uso

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**events**](events.md)<br/>       | Especifica si los eventos relacionados se incluyen en las funciones generadas.<br/> <br/> |
| [**sesión**](operation.md)<br/> | Especifica una operación para la que se va a generar código.<br/> <br/>                 |
| [**portType**](porttype.md)<br/>   | Especifica el tipo de puerto para el que se generará el código.<br/> <br/>                |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




