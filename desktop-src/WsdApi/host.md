---
description: Define los elementos ServiceID y Types para el host de servicio.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: elemento host
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe0637c358fabe27f2a1203306cd53407d85ab8b52f2dcd7a827dd49becffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738611"
---
# <a name="host-element"></a>elemento host

Define los [**elementos ServiceID**](serviceid.md) y [**Types**](types.md) para el host de servicio.

## <a name="usage"></a>Uso

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [**ServiceID**](serviceid.md)<br/> | Define el identificador de servicio para el host de servicio.<br/> <br/> |
| [**Tipos**](types.md)<br/>         | Define una lista de nombres completos XSD.<br/> <br/>               |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                         | Descripción                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | Metadatos de hospedaje para el dispositivo que se va a implementar.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




