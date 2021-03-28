---
description: Un metarchivo mejorado es una matriz de registros.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Registros de metarchivos mejorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984970"
---
# <a name="enhanced-metafile-records"></a><span data-ttu-id="86d51-103">Registros de metarchivos mejorados</span><span class="sxs-lookup"><span data-stu-id="86d51-103">Enhanced Metafile Records</span></span>

<span data-ttu-id="86d51-104">Un metarchivo mejorado es una matriz de registros.</span><span class="sxs-lookup"><span data-stu-id="86d51-104">An enhanced metafile is an array of records.</span></span> <span data-ttu-id="86d51-105">Un registro de metarchivo es una estructura [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="86d51-105">A metafile record is a variable-length [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) structure.</span></span> <span data-ttu-id="86d51-106">Al principio de cada registro de metarchivo mejorado se encuentra una estructura [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) , que contiene dos miembros.</span><span class="sxs-lookup"><span data-stu-id="86d51-106">At the beginning of every enhanced metafile record is an [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) structure, which contains two members.</span></span> <span data-ttu-id="86d51-107">El primer miembro, iType, identifica el tipo de registro que es, la función GDI cuyos parámetros se incluyen en el registro.</span><span class="sxs-lookup"><span data-stu-id="86d51-107">The first member, iType, identifies the record type that is, the GDI function whose parameters are contained in the record.</span></span> <span data-ttu-id="86d51-108">Dado que las estructuras son de longitud variable, el otro miembro, nSize, contiene el tamaño del registro.</span><span class="sxs-lookup"><span data-stu-id="86d51-108">Because the structures are variable in length, the other member, nSize, contains the size of the record.</span></span> <span data-ttu-id="86d51-109">Inmediatamente después del miembro nSize se encuentran los parámetros restantes de la función GDI, si existen.</span><span class="sxs-lookup"><span data-stu-id="86d51-109">Immediately following the nSize member are the remaining parameters, if any, of the GDI function.</span></span> <span data-ttu-id="86d51-110">El resto de la estructura contiene datos adicionales que dependen del tipo de registro.</span><span class="sxs-lookup"><span data-stu-id="86d51-110">The remainder of the structure contains additional data that is dependent on the record type.</span></span>

<span data-ttu-id="86d51-111">El primer registro de un metarchivo mejorado siempre es la estructura [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) , que es el encabezado Enhanced-Metafile.</span><span class="sxs-lookup"><span data-stu-id="86d51-111">The first record in an enhanced metafile is always the [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) structure, which is the enhanced-metafile header.</span></span> <span data-ttu-id="86d51-112">El encabezado especifica la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="86d51-112">The header specifies the following information:</span></span>

-   <span data-ttu-id="86d51-113">Tamaño del metarchivo, en bytes</span><span class="sxs-lookup"><span data-stu-id="86d51-113">Size of the metafile, in bytes</span></span>
-   <span data-ttu-id="86d51-114">Dimensiones del marco de imagen, en unidades de dispositivo</span><span class="sxs-lookup"><span data-stu-id="86d51-114">Dimensions of the picture frame, in device units</span></span>
-   <span data-ttu-id="86d51-115">Dimensiones del marco de imagen, en unidades. 01-milímetros</span><span class="sxs-lookup"><span data-stu-id="86d51-115">Dimensions of the picture frame, in .01-millimeter units</span></span>
-   <span data-ttu-id="86d51-116">Número de registros del metarchivo</span><span class="sxs-lookup"><span data-stu-id="86d51-116">Number of records in the metafile</span></span>
-   <span data-ttu-id="86d51-117">Desplazamiento a una descripción de texto opcional</span><span class="sxs-lookup"><span data-stu-id="86d51-117">Offset to an optional text description</span></span>
-   <span data-ttu-id="86d51-118">Tamaño de la paleta opcional</span><span class="sxs-lookup"><span data-stu-id="86d51-118">Size of the optional palette</span></span>
-   <span data-ttu-id="86d51-119">Resolución del dispositivo original, en píxeles</span><span class="sxs-lookup"><span data-stu-id="86d51-119">Resolution of the original device, in pixels</span></span>
-   <span data-ttu-id="86d51-120">Resolución del dispositivo original, en milímetros</span><span class="sxs-lookup"><span data-stu-id="86d51-120">Resolution of the original device, in millimeters</span></span>

<span data-ttu-id="86d51-121">Una descripción de texto opcional puede seguir el registro de encabezado.</span><span class="sxs-lookup"><span data-stu-id="86d51-121">An optional text description can follow the header record.</span></span> <span data-ttu-id="86d51-122">La descripción del texto describe la imagen y el nombre del autor.</span><span class="sxs-lookup"><span data-stu-id="86d51-122">The text description describes the picture and the author's name.</span></span> <span data-ttu-id="86d51-123">La paleta opcional especifica los colores usados para crear el metarchivo mejorado.</span><span class="sxs-lookup"><span data-stu-id="86d51-123">The optional palette specifies the colors used to create the enhanced metafile.</span></span> <span data-ttu-id="86d51-124">Los registros restantes identifican las funciones GDI utilizadas para crear la imagen.</span><span class="sxs-lookup"><span data-stu-id="86d51-124">The remaining records identify the GDI functions used to create the picture.</span></span> <span data-ttu-id="86d51-125">La siguiente salida hexadecimal corresponde a un registro generado para una llamada a la función [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) .</span><span class="sxs-lookup"><span data-stu-id="86d51-125">The following hexadecimal output corresponds to a record generated for a call to the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function.</span></span>


```C++
00000011 0000000C 00000004 
```



<span data-ttu-id="86d51-126">El valor 0x00000011 especifica el tipo de registro (corresponde a la \_ constante SETMAPMODE de EMR definida en el archivo WinGDI. h).</span><span class="sxs-lookup"><span data-stu-id="86d51-126">The value 0x00000011 specifies the record type (corresponds to the EMR\_SETMAPMODE constant defined in the file Wingdi.h).</span></span> <span data-ttu-id="86d51-127">El valor 0x0000000C especifica la longitud del registro, en bytes.</span><span class="sxs-lookup"><span data-stu-id="86d51-127">The value 0x0000000C specifies the length of the record, in bytes.</span></span> <span data-ttu-id="86d51-128">El valor 0x00000004 identifica el modo de asignación (corresponde a la \_ constante LOENGLISH de mm definida en la función [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) ).</span><span class="sxs-lookup"><span data-stu-id="86d51-128">The value 0x00000004 identifies the mapping mode (corresponds to the MM\_LOENGLISH constant defined in the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function).</span></span>

<span data-ttu-id="86d51-129">Para obtener una lista de tipos de registros adicionales, vea [estructuras de metarchivo](metafile-structures.md).</span><span class="sxs-lookup"><span data-stu-id="86d51-129">For a list of additional record types, see [Metafile Structures](metafile-structures.md).</span></span>

 

 



