---
title: La colección AnimationNames
description: La colección AnimationNames
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903486"
---
# <a name="the-animationnames-collection"></a>La colección AnimationNames

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

La colección [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) es una colección especial que contiene la lista de nombres de animación compilados para un carácter. Puede utilizar la colección para enumerar los nombres de las animaciones de un carácter. Por ejemplo, en Visual Basic o VBScript (2,0 o posterior) puede tener acceso a estos nombres mediante la **... Instrucciones siguientes** :


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Los elementos de la colección no tienen ninguna propiedad, por lo que no se puede tener acceso a los elementos individuales directamente.

Para. Los caracteres ACF, la colección devuelve todas las animaciones definidas para el carácter, no solo las que se han recuperado con el método [**Get**](get-method.md) .

 

 




