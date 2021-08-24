---
title: Elemento Application
description: Representa el elemento de nivel superior de la especificación de marcado Windows marco de la cinta de opciones.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Cinta de opciones del Windows aplicación
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4055e271ecf3313596b73aa36a5cbea37250416d9b517fb4512b89fbc203293a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810815"
---
# <a name="application-element"></a>Elemento Application

Representa el elemento de nivel superior de la especificación de marcado Windows marco de la cinta de opciones.

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
| **xmlns**<br/> | xs:string<br/> | Sí<br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> URI del enlace de espacio de nombres de marcado de la cinta de opciones. <br/> </dd> </dl> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                               | Descripción                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [**Application.Commands**](windowsribbon-element-application-commands.md)<br/> | Puede producirse como máximo una vez<br/> <br/>  |
| [**Application.Views**](windowsribbon-element-application-views.md)<br/>       | Debe producirse exactamente una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios

No hay elementos primarios.

## <a name="remarks"></a>Comentarios

Obligatorio.

Debe producirse exactamente una vez como contenedor para todo el marcado de la cinta de opciones.

Los elementos secundarios del **elemento Application** deben producirse en el orden especificado:

1.  [**Application.Commands**](windowsribbon-element-application-commands.md)
2.  [**Application.Views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra una **declaración de elemento** Application.


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Declarar comandos y controles con marcado de cinta](windowsribbon-schema.md)
</dt> </dl>

 

 





