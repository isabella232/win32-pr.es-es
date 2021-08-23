---
description: La propiedad CurrentDomain recupera el dominio DVD en el que se encuentra el objeto MSWebDVD.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: Propiedad CurrentDomain
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf022d44cc3580a4d5208c5bc96413dfa445b0f2fcbf74eeb938ee77fa0677bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953394"
---
# <a name="currentdomain-property"></a>Propiedad CurrentDomain

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La propiedad recupera el dominio DE DVD en el que se encuentra `CurrentDomain` el objeto MSWebDVD.

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el dominio actual.

## <a name="remarks"></a>Comentarios

Los valores posibles de la propiedad son:



| Value | Descripción          |
|-------|----------------------|
| 1     | Primera reproducción           |
| 2     | Menú Administrador de vídeo   |
| 3     | Menú Conjunto de títulos de vídeo |
| 4     | Título                |
| 5     | Stop                 |



 

Llame a este método para asegurarse de que el navegador de DVD está en un dominio válido para el método al que va a llamar. Por ejemplo, antes de llamar a [**PlayTitle,**](playtitle-method.md)compruebe la propiedad para asegurarse de que el navegador de DVD no está en el `CurrentDomain` dominio Stop o First Play.

 

 



