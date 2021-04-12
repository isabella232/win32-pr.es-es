---
title: Matrices de caracteres contables
description: El atributo \ size \_ es \ indica el límite superior de la matriz mientras que el atributo \ length \_ es \ indica el número de elementos de matriz que se van a transmitir.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487986"
---
# <a name="counted-character-arrays"></a><span data-ttu-id="3d04f-103">Matrices de caracteres contables</span><span class="sxs-lookup"><span data-stu-id="3d04f-103">Counted Character Arrays</span></span>

<span data-ttu-id="3d04f-104">El \[ [atributo \_ size](/windows/desktop/Midl/size-is) \] indica el límite superior de la matriz mientras que la \[ [longitud \_ es](/windows/desktop/Midl/length-is) \] Attribute indica el número de elementos de matriz que se van a transmitir.</span><span class="sxs-lookup"><span data-stu-id="3d04f-104">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute indicates the upper bound of the array while the \[ [length\_is](/windows/desktop/Midl/length-is)\] attribute indicates the number of array elements to transmit.</span></span> <span data-ttu-id="3d04f-105">Además de la matriz, el prototipo de procedimiento remoto debe incluir las variables que representan la longitud o el tamaño que determinan los elementos de la matriz transmitida (pueden ser parámetros independientes o agrupados con la cadena en una estructura).</span><span class="sxs-lookup"><span data-stu-id="3d04f-105">In addition to the array, the remote procedure prototype must include any variables representing length or size that determine the transmitted array elements (they can be separate parameters or bundled with the string in a structure).</span></span> <span data-ttu-id="3d04f-106">Estos atributos se pueden usar con matrices de caracteres anchos o de un solo byte, tal y como lo harían con matrices de otros tipos.</span><span class="sxs-lookup"><span data-stu-id="3d04f-106">These attributes can be used with wide-character or single-byte character arrays just as they would be with arrays of other types.</span></span>

<span data-ttu-id="3d04f-107">La información de esta sección describe los prototipos de parámetros de procedimientos remotos para las matrices de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3d04f-107">The information in this section describes remote procedure parameter prototypes for character arrays.</span></span> <span data-ttu-id="3d04f-108">Se divide en los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="3d04f-108">It is divided into the following topics:</span></span>

-   <span data-ttu-id="3d04f-109">[\[in, out, el tamaño \_ es \] prototype](-in-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="3d04f-109">[\[in, out, size\_is\] Prototype](-in-out-size-is-prototype.md)</span></span>
-   <span data-ttu-id="3d04f-110">[\[en, el tamaño \_ es y fuera, el tamaño \_ es \] prototipo](-in-size-is-and-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="3d04f-110">[\[in, size\_is and out, size\_is\] Prototype](-in-size-is-and-out-size-is-prototype.md)</span></span>

 

 