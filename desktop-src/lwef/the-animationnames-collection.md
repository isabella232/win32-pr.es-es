---
title: Colección AnimationNames
description: Colección AnimationNames
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c9ee781b836599ccf9689bfae974fd4cf3af32d75df2070e984ae9b6596f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960665"
---
# <a name="the-animationnames-collection"></a>Colección AnimationNames

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

La [**colección AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) es una colección especial que contiene la lista de nombres de animación compilados para un carácter. Puede usar la colección para enumerar los nombres de las animaciones de un carácter. Por ejemplo, en Visual Basic o VBScript (2.0 o posterior) puede acceder a estos nombres mediante **for Each... Instrucciones** siguientes:


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Los elementos de la colección no tienen propiedades, por lo que no se puede acceder directamente a los elementos individuales.

Para. Caracteres ACF, la colección devuelve todas las animaciones que se han definido para el carácter, no solo las que se han recuperado con el [**método Get.**](get-method.md)

 

 




