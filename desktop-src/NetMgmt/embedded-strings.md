---
title: Cadenas incrustadas
description: Las estructuras de información no contendrán cadenas insertadas. Esto mejora la alineación de las estructuras de información y permite la flexibilidad del OEM en las funciones principales.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777113"
---
# <a name="embedded-strings"></a><span data-ttu-id="3ced2-104">Cadenas incrustadas</span><span class="sxs-lookup"><span data-stu-id="3ced2-104">Embedded Strings</span></span>

<span data-ttu-id="3ced2-105">Las estructuras de información no contendrán cadenas insertadas.</span><span class="sxs-lookup"><span data-stu-id="3ced2-105">Information structures will not contain embedded strings.</span></span> <span data-ttu-id="3ced2-106">Esto mejora la alineación de las estructuras de información y permite la flexibilidad del OEM en las funciones principales.</span><span class="sxs-lookup"><span data-stu-id="3ced2-106">This improves the alignment of the information structures and allows for OEM flexibility in the core functions.</span></span>

<span data-ttu-id="3ced2-107">Se garantiza que todos los campos de información que se devuelven en una llamada de enumeración que se pueden usar posteriormente como clave para la llamada a una función de administración de red GetInfo están presentes en el búfer de enumeración.</span><span class="sxs-lookup"><span data-stu-id="3ced2-107">Any information field that is returned in an enumeration call that can be subsequently used as a key for the call to a GetInfo network management function is guaranteed to be present in the enumeration buffer.</span></span> <span data-ttu-id="3ced2-108">Si la cadena de información de longitud variable que especificaría el valor del campo de clave no cabe, no se devolverá toda la estructura de longitud fija de la entrada.</span><span class="sxs-lookup"><span data-stu-id="3ced2-108">If the variable-length information string that would specify the key field value will not fit, then the entire fixed-length structure for the entry is not returned.</span></span> <span data-ttu-id="3ced2-109">Otros campos de longitud variable se devolverán como un puntero **nulo** para el caso en el que la cadena no cabe.</span><span class="sxs-lookup"><span data-stu-id="3ced2-109">Other variable-length fields will be returned as a **NULL** pointer for the case in which the string does not fit.</span></span>

 

 




