---
description: Define el prefijo al que se debe asignar el espacio de nombres para que el XML sea más legible.
ms.assetid: 955f4785-5657-4a89-9728-bce99a0a4234
title: elemento preferredPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98fa0310872a43811ceb626ae0684fa45a2f6666
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973689"
---
# <a name="preferredprefix-element"></a>elemento preferredPrefix

Define el prefijo al que se debe asignar el espacio de nombres para que el XML sea más legible.

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
| [**Nombres**](namespace.md)<br/> | Espacio de nombres que se va a usar para la generación de código.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este elemento invalida el prefijo URI predeterminado utilizado para el código generado. Por ejemplo, un espacio de nombres relacionado con medios podría tener el prefijo preferido "av" (para audio/objeto visual).

De forma predeterminada, el código generado crea un prefijo preferido a partir del URI.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




