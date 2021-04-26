---
description: Genera declaraciones de implementación para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: elemento subscriptionFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7389b30ef7da17f9466fa8aefd24fa04f4c99f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995462"
---
# <a name="subscriptionfunctiondeclarations-element"></a>elemento subscriptionFunctionDeclarations

Genera declaraciones de implementación para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.

## <a name="usage"></a>Uso

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
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



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
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



 

 




