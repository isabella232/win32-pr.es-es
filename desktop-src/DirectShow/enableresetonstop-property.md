---
description: La propiedad EnableResetOnStop establece o recupera un valor que determina cómo se reanudará la reproducción cuando el gráfico de filtros realiza una transición desde un estado detenido.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Propiedad EnableResetOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4bfda62839f55dcb4c4597fdad6654072f4dfeb2450c3bce3ed99c13a418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107865"
---
# <a name="enableresetonstop-property"></a>Propiedad EnableResetOnStop

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La propiedad establece o recupera un valor que determina cómo se reanudará la reproducción cuando el gráfico de filtros realiza una transición desde `EnableResetOnStop` un estado detenido.

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica dónde se volverá a reproducir el objeto MSWebDVD después de detener el gráfico de filtro.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura.

Los valores posibles de esta propiedad son: con un valor predeterminado de true.



| Value | Descripción                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | DVD Navigator restablecerá e iniciará la reproducción desde el principio del disco. Este es el valor predeterminado |
| false | DVD Navigator reanudará la reproducción donde lo dejó.                                                 |



 

 

 



