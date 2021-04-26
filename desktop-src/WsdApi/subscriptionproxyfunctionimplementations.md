---
description: Genera implementaciones para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: elemento subscriptionProxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9a3cba202c05d3f8b43b31c292dad8d601dc4e4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995322"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a>elemento subscriptionProxyFunctionImplementations

Genera implementaciones para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.

## <a name="usage"></a>Uso

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a>Atributos



| Atributo                 | Tipo               | Obligatorio      | Descripción                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| **extensible**<br/> | boolean<br/> | No<br/> | La capacidad de agregar puntos de extensibilidad a funciones e interfaces. Este valor siempre se establece en true.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                           | Descripción                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**notificationInterface**](notificationinterface.md)<br/> | Especifica el nombre de la interfaz de notificación que se usa con las suscripciones de eventos.<br/> <br/> |
| [**Operación**](operation.md)<br/>                         | Especifica una operación para la que se va a generar código.<br/> <br/>                       |
| [**portType**](porttype.md)<br/>                           | Especifica el tipo de puerto para el que se va a generar el código.<br/> <br/>                      |
| [**proxyClass**](proxyclass.md)<br/>                       | Especifica el nombre de la clase de proxy del lado cliente.<br/> <br/>                              |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




