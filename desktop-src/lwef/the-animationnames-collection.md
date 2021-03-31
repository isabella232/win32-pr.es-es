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
# <a name="the-animationnames-collection"></a><span data-ttu-id="074dd-103">La colección AnimationNames</span><span class="sxs-lookup"><span data-stu-id="074dd-103">The AnimationNames Collection</span></span>

<span data-ttu-id="074dd-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="074dd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="074dd-105">La colección [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) es una colección especial que contiene la lista de nombres de animación compilados para un carácter.</span><span class="sxs-lookup"><span data-stu-id="074dd-105">The [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) collection is a special collection that contains the list of animation names compiled for a character.</span></span> <span data-ttu-id="074dd-106">Puede utilizar la colección para enumerar los nombres de las animaciones de un carácter.</span><span class="sxs-lookup"><span data-stu-id="074dd-106">You can use the collection to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="074dd-107">Por ejemplo, en Visual Basic o VBScript (2,0 o posterior) puede tener acceso a estos nombres mediante la **... Instrucciones siguientes** :</span><span class="sxs-lookup"><span data-stu-id="074dd-107">For example, in Visual Basic or VBScript (2.0 or later) you can access these names using the **For Each...Next** statements:</span></span>


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



<span data-ttu-id="074dd-108">Los elementos de la colección no tienen ninguna propiedad, por lo que no se puede tener acceso a los elementos individuales directamente.</span><span class="sxs-lookup"><span data-stu-id="074dd-108">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span>

<span data-ttu-id="074dd-109">Para. Los caracteres ACF, la colección devuelve todas las animaciones definidas para el carácter, no solo las que se han recuperado con el método [**Get**](get-method.md) .</span><span class="sxs-lookup"><span data-stu-id="074dd-109">For .ACF characters, the collection returns all the animations that have been defined for the character, not just the ones that have been retrieved with the [**Get**](get-method.md) method.</span></span>

 

 




