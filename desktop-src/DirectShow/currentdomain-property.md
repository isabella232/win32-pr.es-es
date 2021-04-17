---
description: La propiedad CurrentDomain recupera el dominio de DVD en el que se encuentra el objeto MSWebDVD.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: Propiedad CurrentDomain
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495149"
---
# <a name="currentdomain-property"></a>Propiedad CurrentDomain

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `CurrentDomain` propiedad recupera el dominio de DVD en el que se encuentra el objeto MSWebDVD.

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el dominio actual.

## <a name="remarks"></a>Observaciones

Los valores posibles de la propiedad son:



| Value | Descripción          |
|-------|----------------------|
| 1     | Primer juego           |
| 2     | Menú del administrador de vídeos   |
| 3     | Menú de conjunto de títulos de vídeo |
| 4     | Title                |
| 5     | Stop                 |



 

Llame a este método para asegurarse de que el navegador de DVD se encuentre en un dominio válido para el método que va a llamar. Por ejemplo, antes de llamar a [**PlayTitle**](playtitle-method.md), Compruebe la `CurrentDomain` propiedad para asegurarse de que el navegador de DVD no se encuentra en el dominio STOP o First Play.

 

 



