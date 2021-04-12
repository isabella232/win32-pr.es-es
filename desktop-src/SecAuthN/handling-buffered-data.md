---
description: Varias de las funciones de proveedor de red toman la dirección y el tamaño de un búfer en el que la función coloca una estructura de datos de tamaño variable.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Controlar los datos almacenados en búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e123fc1ccccae6120b6db1c9ada554acc5b02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278141"
---
# <a name="handling-buffered-data"></a><span data-ttu-id="29fdd-103">Controlar los datos almacenados en búfer</span><span class="sxs-lookup"><span data-stu-id="29fdd-103">Handling Buffered Data</span></span>

<span data-ttu-id="29fdd-104">Varias de las funciones de proveedor de red toman la dirección y el tamaño de un búfer en el que la función coloca una estructura de datos de tamaño variable.</span><span class="sxs-lookup"><span data-stu-id="29fdd-104">Several of the network provider functions take the address and size of a buffer into which the function places a variable-sized data structure.</span></span>

<span data-ttu-id="29fdd-105">En cada caso, el mecanismo utilizado es el mismo.</span><span class="sxs-lookup"><span data-stu-id="29fdd-105">In each case, the mechanism used is the same.</span></span> <span data-ttu-id="29fdd-106">El autor de la llamada asigna un búfer y pasa su dirección a la función.</span><span class="sxs-lookup"><span data-stu-id="29fdd-106">The caller allocates a buffer and passes its address to the function.</span></span> <span data-ttu-id="29fdd-107">También pasa la dirección de un **valor DWORD** que especifica el tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="29fdd-107">It also passes the address of a **DWORD** that specifies the size of the buffer, in bytes.</span></span>

<span data-ttu-id="29fdd-108">A continuación, la función copia la gran parte de la estructura de datos solicitada tal y como se puede hacer en el búfer.</span><span class="sxs-lookup"><span data-stu-id="29fdd-108">The function then copies as much of the requested data structure as it can into the buffer.</span></span> <span data-ttu-id="29fdd-109">Si todos los datos caben en el búfer, la función devuelve WN \_ Success.</span><span class="sxs-lookup"><span data-stu-id="29fdd-109">If all of the data fits into the buffer, the function returns WN\_SUCCESS.</span></span> <span data-ttu-id="29fdd-110">Si los datos no caben en el búfer, los datos se pueden dejar incompletos y la función establece el \_ error de más datos de WN \_ .</span><span class="sxs-lookup"><span data-stu-id="29fdd-110">If the data does not fit into the buffer, the data may be left incomplete, and the function sets the WN\_MORE\_DATA error.</span></span> <span data-ttu-id="29fdd-111">En cualquier caso, el **valor DWORD** que indica el tamaño del búfer se establece en el número de bytes realmente requerido por la estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="29fdd-111">In either case, the **DWORD** indicating the size of the buffer is set to the number of bytes actually required by the data structure.</span></span> <span data-ttu-id="29fdd-112">De este modo, si el búfer pasado es demasiado pequeño y se produjo un error en la función, el llamador puede asignar un nuevo búfer del tamaño requerido y volver a llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="29fdd-112">This way, if the buffer passed in was too small and the function failed, the caller may allocate a new buffer of the required size and call the function again.</span></span>

<span data-ttu-id="29fdd-113">Cuando las estructuras de datos devueltas incluyen cadenas de longitud variable, las estructuras de datos individuales normalmente contienen punteros a estas cadenas.</span><span class="sxs-lookup"><span data-stu-id="29fdd-113">When the data structures returned include variable-length strings, the individual data structures typically contain pointers to these strings.</span></span> <span data-ttu-id="29fdd-114">Las propias cadenas también se deben colocar en el búfer.</span><span class="sxs-lookup"><span data-stu-id="29fdd-114">The strings themselves should also be placed within the buffer.</span></span> <span data-ttu-id="29fdd-115">Sin embargo, es importante colocarlos al final del búfer.</span><span class="sxs-lookup"><span data-stu-id="29fdd-115">However, it is important to place them at the end of the buffer.</span></span> <span data-ttu-id="29fdd-116">De lo contrario, hará que la indización en la estructura nth sea imposible.</span><span class="sxs-lookup"><span data-stu-id="29fdd-116">Otherwise, they will make indexing to the Nth structure impossible.</span></span> <span data-ttu-id="29fdd-117">En otras palabras, todas las estructuras se colocan de forma contigua al principio del búfer.</span><span class="sxs-lookup"><span data-stu-id="29fdd-117">In other words, all structures are located contiguously at the beginning of the buffer.</span></span> <span data-ttu-id="29fdd-118">Los punteros a cadenas o datos de longitud variable deben ser punteros reales, no desplazamientos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="29fdd-118">Pointers to strings or variable length data must be actual pointers, not offsets into the buffer.</span></span>

<span data-ttu-id="29fdd-119">Cuando se usa un búfer para pasar y devolver datos que solo se componen de cadenas, el **valor DWORD** que especifica el tamaño del búfer se debe establecer en el número total de caracteres que quepan en estas cadenas, no en el número de bytes.</span><span class="sxs-lookup"><span data-stu-id="29fdd-119">When a buffer is used to pass in and return data that consists only of strings, the **DWORD** specifying the size of the buffer should be set to the total number of characters that will fit in these strings, not to the number of bytes.</span></span>

 

 



