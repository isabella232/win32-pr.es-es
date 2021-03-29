---
description: La propiedad EnableResetOnStop establece o recupera un valor que determina cómo se reanudará la reproducción cuando el gráfico de filtros realice una transición desde un estado detenido.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Propiedad EnableResetOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806134"
---
# <a name="enableresetonstop-property"></a>Propiedad EnableResetOnStop

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `EnableResetOnStop` propiedad establece o recupera un valor que determina cómo se reanudará la reproducción cuando el gráfico de filtros realice una transición desde un estado detenido.

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica dónde se iniciará la reproducción del objeto MSWebDVD de nuevo después de que se detenga el gráfico de filtros.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura y escritura.

Los valores posibles de esta propiedad son: con el valor predeterminado True.



| Value | Descripción                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | El navegador de DVD se restablecerá y comenzará a reproducir desde el principio del disco. Este es el valor predeterminado |
| false | El navegador de DVD se reanudará en el punto en que se quedó.                                                 |



 

 

 



