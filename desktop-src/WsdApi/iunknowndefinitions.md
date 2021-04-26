---
description: Genera implementaciones para las funciones QueryInterface, AddRef y Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995152"
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
| **proxyClass**<br/>  | cadena \_ de caracteres<br/> | Sí<br/> | Nombre de la clase de implementación.<br/> <br/> |
| **refCountVar**<br/> | cadena \_ de caracteres<br/> | Sí<br/> | Nombre de la variable de recuento de referencias.<br/> <br/>  |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [**interfaz**](interface.md)<br/> | Nombre de la interfaz que va a devolver QueryInterface.<br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
interface
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



 

 




