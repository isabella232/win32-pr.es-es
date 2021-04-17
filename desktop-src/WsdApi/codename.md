---
description: Define el nombre que se va a utilizar para identificar el espacio de nombres en el código generado.
ms.assetid: 4e476be2-fa73-4b3e-b0cc-799c8d16b5de
title: Nombre del elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44c10b937f503c2d3994543db8852b5d7ee923b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706923"
---
# <a name="codename-element"></a>Nombre del elemento

Define el nombre que se va a utilizar para identificar el espacio de nombres en el código generado.

## <a name="usage"></a>Uso

``` syntax
<codeName/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                         | Descripción                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**System.IO**](namespace.md)<br/>                       | Espacio de nombres que se va a utilizar para la generación de código.<br/> <br/>       |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/> | Genera declaraciones de constantes de C para los tipos de puerto.<br/> <br/> |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>   | Genera constantes de C para los tipos de puerto.<br/> <br/>             |



## <a name="remarks"></a>Observaciones

Este elemento invalida el nombre de código predeterminado usado para el código generado. De forma predeterminada, el código generado crea un nombre de código a partir del URI o nombre completo.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




