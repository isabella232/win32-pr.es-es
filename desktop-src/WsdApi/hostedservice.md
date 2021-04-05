---
description: Define un servicio que se va a hospedar en una función de host Builder.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: hostedService (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908661"
---
# <a name="hostedservice-element"></a>hostedService (elemento)

Define un servicio que se va a hospedar en una función de host Builder.

## <a name="usage"></a>Uso

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                     | Descripción                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nombre**](codename.md)<br/>     | Especifica el nombre que se va a usar para el tipo de puerto en el código generado. De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.<br/> <br/> |
| [**portType**](porttype.md)<br/>     | Tipo de puerto para el que se va a generar el código.<br/> <br/>                                                                                                       |
| [**proxyClass**](proxyclass.md)<br/> | Nombre de clase que se generará a partir de la función de generador.<br/> <br/>                                                                                                      |
| [**ServiceID**](serviceid.md)<br/>   | URI que representa el identificador del servicio.<br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [**archivo**](file.md)<br/> | Especificación del archivo de salida para el generador de código.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




