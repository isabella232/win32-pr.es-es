---
description: Genera una función que crea un host con tipo.
ms.assetid: 2b4a4016-cc5d-4912-8e08-ce3a11ab0a06
title: elemento hostBuilderImplementation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d333287acd199f4fe2aa8967a1b8d6458ff3ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567173"
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
| [**hostedService**](hostedservice.md)<br/> | Servicio que se va a incluir para el host. <br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
hostedService+
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




