---
description: Especifica la ubicación de descarga de una directiva wsdl:import que no especifica explícitamente una ubicación.
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bff41d5f58e8e3041873d6283afc032409855a53013e721efad6c5986c6c6ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732245"
---
# <a name="importhint-element"></a>elemento importHint

Especifica la ubicación de descarga de una \<wsdl:import> directiva que no especifica explícitamente una ubicación.

## <a name="usage"></a>Uso

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Ubicación**](location.md)<br/>   | Ubicación del archivo que se importará. La ubicación puede ser una ruta de acceso relativa, una ruta de acceso absoluta o una dirección URL HTTP.<br/> <br/> |
| [**Nombres**](namespace.md)<br/> | Espacio de nombres que se va a importar. Debe coincidir con el espacio de nombres especificado en el \<wsdl:import> elemento .<br/> <br/>     |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**Wsdl**](wsdl.md)<br/> | Especifica un archivo WSDL para procesar la información del contrato.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




