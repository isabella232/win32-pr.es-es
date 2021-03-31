---
title: Elemento Application
description: Representa el elemento de nivel superior en la especificación de marcado del marco de la cinta de Windows.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Cinta de opciones de Windows, elemento de aplicación
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103797187"
---
# <a name="application-element"></a>Elemento Application

Representa el elemento de nivel superior en la especificación de marcado del marco de la cinta de Windows.

## <a name="usage"></a>Uso

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a>Atributos



| Atributo            | Tipo                 | Obligatorio       | Descripción                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **xmlns**<br/> | xs:string<br/> | Sí<br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> El URI para el enlace del espacio de nombres de marcado de la cinta. <br/> </dd> </dl> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                               | Descripción                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [**Application. Commands**](windowsribbon-element-application-commands.md)<br/> | Puede aparecer como máximo una vez<br/> <br/>  |
| [**Application. views**](windowsribbon-element-application-views.md)<br/>       | Debe aparecer exactamente una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios

No hay elementos primarios.

## <a name="remarks"></a>Observaciones

Obligatorio.

Debe aparecer exactamente una vez como contenedor para todo el marcado de la cinta de opciones.

Los elementos secundarios del elemento **Application** deben aparecer en el orden especificado:

1.  [**Application. Commands**](windowsribbon-element-application-commands.md)
2.  [**Application. views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra una declaración de elemento de **aplicación** .


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Declarar comandos y controles con el marcado de la cinta de opciones](windowsribbon-schema.md)
</dt> </dl>

 

 





