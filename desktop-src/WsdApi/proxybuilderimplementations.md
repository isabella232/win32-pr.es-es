---
description: Genera funciones para crear servidores proxy con tipo.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: elemento proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18b13ddda25d8fa157b0399c7b9fba070534fb66e11b3fa63a122b1983dea06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815538"
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
| [**Codename**](codename.md)<br/>     | Nombre que se va a usar para el tipo de puerto en el código generado. De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.<br/> <br/> |
| [**portType**](porttype.md)<br/>     | Tipo de puerto para el que se va a generar el código.<br/> <br/>                                                                                             |
| [**proxyClass**](proxyclass.md)<br/> | Nombre de clase que se generará a partir de la función del generador de proxy.<br/> <br/>                                                                                  |



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
| [**Archivo**](file.md)<br/> | Genera un archivo del generador de código.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




