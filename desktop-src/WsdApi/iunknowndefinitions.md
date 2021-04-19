---
description: Genera implementaciones para las funciones QueryInterface, AddRef y Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715802"
---
# <a name="iunknowndefinitions-element"></a>Elemento IUnknownDefinitions

Genera implementaciones para las funciones QueryInterface, AddRef y Release.

## <a name="usage"></a>Uso

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a>Atributos



| Atributo                  | Tipo                         | Obligatorio       | Descripción                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| **proxyClass**<br/>  | cadena de caracteres \_<br/> | Sí<br/> | Nombre de la clase de implementación.<br/> <br/> |
| **refCountVar**<br/> | cadena de caracteres \_<br/> | Sí<br/> | Nombre de la variable de recuento de referencias.<br/> <br/>  |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [**interfaz**](interface.md)<br/> | Nombre de la interfaz que se va a devolver mediante QueryInterface.<br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
interface
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



 

 




