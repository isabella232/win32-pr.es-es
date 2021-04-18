---
description: Genera funciones para crear servidores proxy con tipo.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: elemento proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706839"
---
# <a name="proxybuilderimplementations-element"></a>elemento proxyBuilderImplementations

Genera funciones para crear servidores proxy con tipo.

## <a name="usage"></a>Uso

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                     | Descripción                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nombre**](codename.md)<br/>     | Nombre que se va a usar para el tipo de puerto en el código generado. De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.<br/> <br/> |
| [**portType**](porttype.md)<br/>     | Tipo de puerto para el que se va a generar el código.<br/> <br/>                                                                                             |
| [**proxyClass**](proxyclass.md)<br/> | Nombre de clase que se generará a partir de la función de generador de proxy.<br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
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
| Puede estar vacío                        | No            |



 

 




