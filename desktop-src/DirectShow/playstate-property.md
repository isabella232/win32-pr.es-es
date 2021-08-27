---
description: La propiedad PlayState recupera el estado actual del objeto MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Propiedad PlayState
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b66ae0ddfb1a8ceb296ec647a0149a42de68f635ffd198d6ba6609ff11e4888
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102355"
---
# <a name="playstate-property"></a>Propiedad PlayState

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `PlayState` propiedad recupera el estado actual del objeto **MSWebDVD.**

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor Entero que representa el estado actual del navegador de DVD.



| Código devuelto | Descripción   |
|-------------|---------------|
| -2          | No definido     |
| -1          | No inicializado |
| 0           | Detenido       |
| 1           | En pausa        |
| 2           | En ejecución       |



 

## <a name="remarks"></a>Comentarios

Esta propiedad es de solo lectura sin ningún valor predeterminado.

El **objeto MSWebDVD** controla el DirectShow filtro DVD Navigator, que realiza el trabajo real de navegación de DVD. En realidad, es el estado del navegador de DVD al que hace referencia esta propiedad. El navegador de DVD puede estar en uno de varios estados, como se describió anteriormente. La propiedad puede ser útil como herramienta de diagnóstico, pero por lo general no debería haber ninguna razón para que una aplicación de scripting supervise el estado `PlayState` del navegador de DVD.

 

 



