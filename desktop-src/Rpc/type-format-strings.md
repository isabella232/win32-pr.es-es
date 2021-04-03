---
title: Cadenas de formato de tipo
description: Los caracteres de formato indican objetos de interés para el motor de NDR.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076086"
---
# <a name="type-format-strings"></a><span data-ttu-id="ff420-103">Cadenas de formato de tipo</span><span class="sxs-lookup"><span data-stu-id="ff420-103">Type Format Strings</span></span>

<span data-ttu-id="ff420-104">Los caracteres de formato indican objetos de interés para el motor de NDR.</span><span class="sxs-lookup"><span data-stu-id="ff420-104">Format characters denote objects of interest to the NDR engine.</span></span> <span data-ttu-id="ff420-105">Hay un carácter de formato para cada tipo básico, para varios tipos complejos y para descripciones de punteros, empaquetado, alineación y otros objetos varios.</span><span class="sxs-lookup"><span data-stu-id="ff420-105">There is a format character for each basic type, for various complex types, and for descriptions of pointers, packing, alignment, and other miscellaneous objects.</span></span> <span data-ttu-id="ff420-106">En el caso de los tipos compuestos, se reconocen varias categorías de estructuras y matrices en función de sus propiedades de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="ff420-106">For compound types, several categories of structures and arrays are recognized based on their performance properties.</span></span> <span data-ttu-id="ff420-107">Una cadena de formato para cada categoría comienza con un token de FC que identifica la cadena de formato en particular.</span><span class="sxs-lookup"><span data-stu-id="ff420-107">A format string for each category starts with an FC token identifying the particular format string.</span></span> <span data-ttu-id="ff420-108">Los caracteres de formato de las categorías de estructuras y matrices pueden compartir las correcciones en el nombre del token de FC inicial que se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ff420-108">Format characters for structures and arrays categories may share the in-fixes in the name of the leading FC token shown in the following table.</span></span>



| <span data-ttu-id="ff420-109">Carácter de formato</span><span class="sxs-lookup"><span data-stu-id="ff420-109">Format character</span></span> | <span data-ttu-id="ff420-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff420-110">Description</span></span>                                    |
|------------------|------------------------------------------------|
| <span data-ttu-id="ff420-111">C</span><span class="sxs-lookup"><span data-stu-id="ff420-111">C</span></span>                | <span data-ttu-id="ff420-112">Indica la información de conformidad en el tipo.</span><span class="sxs-lookup"><span data-stu-id="ff420-112">Indicates conformance information in the type.</span></span> |
| <span data-ttu-id="ff420-113">V</span><span class="sxs-lookup"><span data-stu-id="ff420-113">V</span></span>                | <span data-ttu-id="ff420-114">Indica la información de la varianza en el tipo.</span><span class="sxs-lookup"><span data-stu-id="ff420-114">Indicates variance information in the type.</span></span>    |
| <span data-ttu-id="ff420-115">P</span><span class="sxs-lookup"><span data-stu-id="ff420-115">P</span></span>                | <span data-ttu-id="ff420-116">Indica que los punteros son una parte del tipo.</span><span class="sxs-lookup"><span data-stu-id="ff420-116">Indicates pointers are a part of the type.</span></span>     |



 

<span data-ttu-id="ff420-117">Por ejemplo, FC \_ CSTRUCT y la \_ CArray de FC identifican la estructura compatible y los descriptores de matriz compatibles, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ff420-117">For example, FC\_CSTRUCT and FC\_CARRAY identify the conformant structure and conformant array descriptors, respectively.</span></span>

<span data-ttu-id="ff420-118">A continuación se muestran caracteres de formato con significados especiales.</span><span class="sxs-lookup"><span data-stu-id="ff420-118">The following are format characters with special meanings.</span></span>



| <span data-ttu-id="ff420-119">Carácter de formato</span><span class="sxs-lookup"><span data-stu-id="ff420-119">Format character</span></span> | <span data-ttu-id="ff420-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff420-120">Description</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ff420-121">FC \_ PP</span><span class="sxs-lookup"><span data-stu-id="ff420-121">FC\_PP</span></span>           | <span data-ttu-id="ff420-122">Indica el principio de la sección de Descripción del puntero de una estructura o una matriz.</span><span class="sxs-lookup"><span data-stu-id="ff420-122">Indicates the beginning of the pointer description section of a structure or array.</span></span> |



 

<span data-ttu-id="ff420-123">Las cadenas de formato de tipo NDR de RPC se describen con más detalle en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="ff420-123">RPC NDR type format strings are described in more detail in the following topics:</span></span>

-   [<span data-ttu-id="ff420-124">Tipos simples</span><span class="sxs-lookup"><span data-stu-id="ff420-124">Simple Types</span></span>](simple-types-tfs.md)
-   [<span data-ttu-id="ff420-125">Punteros</span><span class="sxs-lookup"><span data-stu-id="ff420-125">Pointers</span></span>](pointers-tfs.md)
-   [<span data-ttu-id="ff420-126">Matrices</span><span class="sxs-lookup"><span data-stu-id="ff420-126">Arrays</span></span>](arrays-tfs.md)
-   [<span data-ttu-id="ff420-127">Cadenas</span><span class="sxs-lookup"><span data-stu-id="ff420-127">Strings</span></span>](strings-tfs.md)
-   [<span data-ttu-id="ff420-128">Descriptores de correlación</span><span class="sxs-lookup"><span data-stu-id="ff420-128">Correlation Descriptors</span></span>](correlation-descriptors-tfs.md)
-   [<span data-ttu-id="ff420-129">Estructuras</span><span class="sxs-lookup"><span data-stu-id="ff420-129">Structures</span></span>](structures-tfs.md)
-   [<span data-ttu-id="ff420-130">Diseño de puntero</span><span class="sxs-lookup"><span data-stu-id="ff420-130">Pointer Layout</span></span>](pointer-layout-tfs.md)
-   [<span data-ttu-id="ff420-131">Uniones</span><span class="sxs-lookup"><span data-stu-id="ff420-131">Unions</span></span>](unions-tfs.md)
-   [<span data-ttu-id="ff420-132">Transmitir \_ como y representar \_ como</span><span class="sxs-lookup"><span data-stu-id="ff420-132">Transmit\_as and Represent\_as</span></span>](transmit-as-and-represent-as-tfs.md)
-   [<span data-ttu-id="ff420-133">Serialización de usuario</span><span class="sxs-lookup"><span data-stu-id="ff420-133">User-marshal</span></span>](user-marshal-tfs.md)

 

 




