---
description: Cuando se usan estructuras de datos de tamaño variable para transmitir información entre TAPI y la aplicación, la aplicación es responsable de asignar la memoria necesaria.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Estructuras de datos de tamaño variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873fcbaa1e4e3bda772d92ad2de9b1f6258363cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278557"
---
# <a name="variably-sized-data-structures"></a><span data-ttu-id="140ac-103">Estructuras de datos de tamaño variable</span><span class="sxs-lookup"><span data-stu-id="140ac-103">Variably Sized Data Structures</span></span>

<span data-ttu-id="140ac-104">Cuando se usan estructuras de datos de tamaño variable para transmitir información entre TAPI y la aplicación, la aplicación es responsable de asignar la memoria necesaria.</span><span class="sxs-lookup"><span data-stu-id="140ac-104">When variably sized data structures are used to transmit information between TAPI and the application, the application is responsible for allocating the necessary memory.</span></span> <span data-ttu-id="140ac-105">La cantidad de memoria asignada debe ser lo suficientemente grande como para la parte fija de la estructura de datos y la establece la aplicación en el miembro **dwTotalSize** de la estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="140ac-105">The amount of memory allocated must be at least large enough for the fixed portion of the data structure, and is set by the application in the **dwTotalSize** member of the data structure.</span></span> <span data-ttu-id="140ac-106">Los miembros **dwUsedSize** y **dwNeededSize** se rellenan con TAPI.</span><span class="sxs-lookup"><span data-stu-id="140ac-106">The **dwUsedSize** and **dwNeededSize** members are filled in by TAPI.</span></span> <span data-ttu-id="140ac-107">Si **dwTotalSize** es menor que el tamaño de la parte fija, se devuelve LINEERR/PHONEERR \_ STRUCTURETOOSMALL.</span><span class="sxs-lookup"><span data-stu-id="140ac-107">If **dwTotalSize** is less than the size of the fixed portion, then LINEERR/ PHONEERR\_STRUCTURETOOSMALL is returned.</span></span> <span data-ttu-id="140ac-108">Si una función devuelve Success, se han rellenado todos los campos de la parte fija.</span><span class="sxs-lookup"><span data-stu-id="140ac-108">If a function returns success, then all the fields in the fixed portion have been filled in.</span></span> <span data-ttu-id="140ac-109">Los miembros **dwUsedSize** y **dwNeededSize** pueden compararse para determinar si se han rellenado todas las partes variables y cuánto espacio se necesitaría para rellenarlos todo en.</span><span class="sxs-lookup"><span data-stu-id="140ac-109">The **dwUsedSize** and **dwNeededSize** members can be compared to determine if all variable parts have been filled in, and how much space would be required to fill them all in.</span></span>

<span data-ttu-id="140ac-110">Si **dwNeededSize** es igual a **dwUsedSize**, se han rellenado todos los elementos fijos y variables.</span><span class="sxs-lookup"><span data-stu-id="140ac-110">If **dwNeededSize** is equal to **dwUsedSize**, then all fixed and variable parts have been filled in.</span></span> <span data-ttu-id="140ac-111">Si **dwNeededSize** es mayor que **dwUsedSize**, es posible que se hayan rellenado algunas partes variables, pero que los campos de tamaño de variable se hayan rellenado no estén definidos.</span><span class="sxs-lookup"><span data-stu-id="140ac-111">If **dwNeededSize** is larger than **dwUsedSize**, some variable parts may have been filled in, but exactly which variably sized fields have been filled in is undefined.</span></span> <span data-ttu-id="140ac-112">Ninguna parte variable se trunca nunca y las partes variables que se habrían truncado debido a la falta de espacio se indican al tener las partes de "desplazamiento" y "tamaño" correspondientes establecidas en cero.</span><span class="sxs-lookup"><span data-stu-id="140ac-112">No variable part is ever truncated, and variable parts that would have been truncated due to insufficient space are indicated by having both of their corresponding "Offset" and "Size" parts set to zero.</span></span> <span data-ttu-id="140ac-113">Si no son cero (y no se devolvió ningún error), indican el desplazamiento y el tamaño de los datos de partes variables no truncados válidos.</span><span class="sxs-lookup"><span data-stu-id="140ac-113">If these are not both zero (and no error was returned), they indicate the offset and size of valid, nontruncated variable-part data.</span></span>

<span data-ttu-id="140ac-114">Una aplicación siempre puede garantizar que todas las partes variables se rellenan asignando e indicando **dwNeededSize** bytes para la estructura y llamando a la función "Get" hasta que la función devuelve Success y **dwNeededSize** es igual a **dwUsedSize**.</span><span class="sxs-lookup"><span data-stu-id="140ac-114">An application can always guarantee that all variable parts are filled in by allocating and indicating **dwNeededSize** bytes for the structure and calling the "Get" function again until the function returns success and **dwNeededSize** equals **dwUsedSize**.</span></span> <span data-ttu-id="140ac-115">Esto debe ocurrir en el segundo intento excepto en las condiciones de carrera que producen cambios en el tamaño de las partes variables entre las llamadas, que deben ser una situación poco frecuente.</span><span class="sxs-lookup"><span data-stu-id="140ac-115">This should happen on the second try except for race conditions that cause changes in the size of variable parts between calls, which should be a rare occurrence.</span></span>

> [!Note]  
> <span data-ttu-id="140ac-116">Todas las cadenas de texto, independientemente de la codificación, en las estructuras de tamaño de variable deben terminar en **null** según las convenciones normales de control de cadenas de C.</span><span class="sxs-lookup"><span data-stu-id="140ac-116">All text strings, regardless of encoding, in variably sized structures should be **NULL**-terminated according to normal C string-handling conventions.</span></span>

 

 

 



