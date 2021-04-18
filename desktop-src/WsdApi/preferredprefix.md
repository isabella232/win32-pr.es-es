---
description: Define el prefijo al que se debe asignar el espacio de nombres para que el código XML sea más legible.
ms.assetid: 955f4785-5657-4a89-9728-bce99a0a4234
title: elemento preferredPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71f124756f29aaf29ba30d254f9b03ab4495f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706138"
---
# <a name="preferredprefix-element"></a>elemento preferredPrefix

Define el prefijo al que se debe asignar el espacio de nombres para que el código XML sea más legible.

## <a name="usage"></a>Uso

``` syntax
<preferredPrefix/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                   | Descripción                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [**System.IO**](namespace.md)<br/> | Espacio de nombres que se va a utilizar para la generación de código.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este elemento invalida el prefijo de URI predeterminado usado para el código generado. Por ejemplo, un espacio de nombres relacionado con el contenido multimedia podría tener el prefijo preferido "AV" (para audio/visual).

De forma predeterminada, el código generado crea un prefijo preferido a partir del URI.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




