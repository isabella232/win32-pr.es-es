---
description: Genera una función que crea un host con tipo.
ms.assetid: 2b4a4016-cc5d-4912-8e08-ce3a11ab0a06
title: elemento hostBuilderImplementation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9cfabb9ab4193162044420fc3980f0bbeeb55a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715806"
---
# <a name="hostbuilderimplementation-element"></a>elemento hostBuilderImplementation

Genera una función que crea un host con tipo.

## <a name="usage"></a>Uso

``` syntax
<hostBuilderImplementation>
  child elements
</hostBuilderImplementation>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                           | Descripción                                                      |
|---------------------------------------------------|------------------------------------------------------------------|
| [**hostedService**](hostedservice.md)<br/> | El servicio que se va a incluir para el host. <br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
hostedService+
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



 

 




