---
title: Top-Level y punteros incrustados
description: Para entender cómo se asignan los punteros y sus elementos de datos asociados en Microsoft RPC, debe diferenciar entre los punteros de nivel superior y los punteros incrustados.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486999"
---
# <a name="top-level-and-embedded-pointers"></a><span data-ttu-id="a624c-103">Top-Level y punteros incrustados</span><span class="sxs-lookup"><span data-stu-id="a624c-103">Top-Level and Embedded Pointers</span></span>

<span data-ttu-id="a624c-104">Para entender cómo se asignan los punteros y sus elementos de datos asociados en Microsoft RPC, debe diferenciar entre los punteros de *nivel superior* y los *punteros incrustados*.</span><span class="sxs-lookup"><span data-stu-id="a624c-104">To understand how pointers and their associated data elements are allocated in Microsoft RPC, you have to differentiate between *top-level pointers* and *embedded pointers*.</span></span> <span data-ttu-id="a624c-105">También es útil hacer referencia al conjunto de todos los punteros que no son punteros de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="a624c-105">It is also useful to refer to the set of all pointers that are not top-level pointers.</span></span>

<span data-ttu-id="a624c-106">Los *punteros de nivel superior* son aquellos que se especifican como nombres de parámetros en prototipos de función.</span><span class="sxs-lookup"><span data-stu-id="a624c-106">*Top-level pointers* are those that are specified as the names of parameters in function prototypes.</span></span> <span data-ttu-id="a624c-107">Los punteros de nivel superior y sus correspondientes siempre se asignan en el servidor.</span><span class="sxs-lookup"><span data-stu-id="a624c-107">Top-level pointers and their referents are always allocated on the server.</span></span>

<span data-ttu-id="a624c-108">Los *punteros incrustados* son punteros que se incrustan en estructuras de datos como matrices, estructuras y uniones.</span><span class="sxs-lookup"><span data-stu-id="a624c-108">*Embedded pointers* are pointers that are embedded in data structures such as arrays, structures, and unions.</span></span> <span data-ttu-id="a624c-109">Cuando los punteros incrustados solo escriben la salida en un búfer y son NULL en la entrada, la aplicación de servidor puede cambiar sus valores a un valor distinto de NULL.</span><span class="sxs-lookup"><span data-stu-id="a624c-109">When embedded pointers only write output to a buffer and are null on input, the server application can change their values to non-null.</span></span> <span data-ttu-id="a624c-110">En este caso, el código auxiliar del cliente asigna memoria nueva para estos datos.</span><span class="sxs-lookup"><span data-stu-id="a624c-110">In this case, the client stubs allocate new memory for this data.</span></span>

<span data-ttu-id="a624c-111">Si el puntero incrustado no es null en el cliente antes de la llamada, el código auxiliar no asigna memoria en el cliente en la devolución.</span><span class="sxs-lookup"><span data-stu-id="a624c-111">If the embedded pointer is not null on the client before the call, the stubs do not allocate memory on the client on return.</span></span> <span data-ttu-id="a624c-112">En su lugar, el código auxiliar intenta escribir la memoria asociada al puntero incrustado en la memoria existente en el cliente asociado a ese puntero, sobrescribiendo los datos ya existentes.</span><span class="sxs-lookup"><span data-stu-id="a624c-112">Instead, the stubs attempt to write the memory associated with the embedded pointer into the existing memory on the client associated with that pointer, overwriting the data already there.</span></span>

> [!Note]  
> <span data-ttu-id="a624c-113">En el caso de los datos leídos o escritos en un búfer y que no especifica el tamaño del búfer, la longitud de salida debe ser menor o igual que la longitud de entrada.</span><span class="sxs-lookup"><span data-stu-id="a624c-113">For data read from or writen to a buffer, and which does not specify the buffer size, output length must be less than or equal to input length.</span></span> <span data-ttu-id="a624c-114">Se produce una excepción RPC cuando se detecta desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="a624c-114">An RPC exception is raised when overflow is detected.</span></span> <span data-ttu-id="a624c-115">En el caso de los datos de cadena, la longitud de salida se determina mediante la comprobación de la longitud de la cadena de entrada.</span><span class="sxs-lookup"><span data-stu-id="a624c-115">For string data, output length is determined by checking length of the input string.</span></span> <span data-ttu-id="a624c-116">Por lo tanto, las cadenas de salida no pueden superar la longitud de las cadenas de entrada.</span><span class="sxs-lookup"><span data-stu-id="a624c-116">Therefore, output strings cannot exceed length of input strings.</span></span> <span data-ttu-id="a624c-117">La guía de procedimientos recomendados es evitar esto al incluir siempre un parámetro especificado por el tamaño para indicar el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="a624c-117">Best practice guidance is to avoid this by always including a size-specified parameter to indicate size of the buffer.</span></span>

 

<span data-ttu-id="a624c-118">Los punteros de solo escritura incrustados se tratan en [combinación de atributos direccionales y de puntero](combining-pointer-and-directional-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="a624c-118">Embedded write-only pointers are discussed in [Combining Pointer and Directional Attributes](combining-pointer-and-directional-attributes.md).</span></span>

<span data-ttu-id="a624c-119">El término *punteros de nivel nontop* hace referencia a todos los punteros que no se especifican como nombres de parámetro en el prototipo de función, incluidos los punteros incrustados y varios niveles de punteros anidados.</span><span class="sxs-lookup"><span data-stu-id="a624c-119">The term *nontop-level pointers* refers to all pointers that are not specified as parameter names in the function prototype, including both embedded pointers and multiple levels of nested pointers.</span></span>

 

 




