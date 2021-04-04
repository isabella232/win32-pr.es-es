---
title: Formatos de datos y medios de transferencia
description: Formatos de datos y medios de transferencia
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6893fabd776d196cbc7354dde7c330f9caffb0a
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104078591"
---
# <a name="data-formats-and-transfer-media"></a><span data-ttu-id="e5da9-103">Formatos de datos y medios de transferencia</span><span class="sxs-lookup"><span data-stu-id="e5da9-103">Data Formats and Transfer Media</span></span>

<span data-ttu-id="e5da9-104">La mayoría de las plataformas, incluidas Windows, definen un protocolo estándar para transferir datos entre aplicaciones, en función de un conjunto de funciones denominado portapapeles.</span><span class="sxs-lookup"><span data-stu-id="e5da9-104">Most platforms, including Windows, define a standard protocol for transferring data between applications, based on a set of functions called the clipboard.</span></span> <span data-ttu-id="e5da9-105">Las aplicaciones que usan estas funciones pueden compartir datos incluso si sus formatos de datos nativos son muy diferentes.</span><span class="sxs-lookup"><span data-stu-id="e5da9-105">Applications using these functions can share data even if their native data formats are wildly different.</span></span> <span data-ttu-id="e5da9-106">Por lo general, estos portapapeles tienen dos lagunas significativas que COM ha superado.</span><span class="sxs-lookup"><span data-stu-id="e5da9-106">Generally, these clipboards have two significant shortcomings that COM has overcome.</span></span>

<span data-ttu-id="e5da9-107">En primer lugar, las descripciones de datos usan solo un identificador de formato, como el único identificador de formato del portapapeles de 16 bits en Windows, lo que significa que el portapapeles solo puede describir la estructura de los datos, es decir, el orden de los bits.</span><span class="sxs-lookup"><span data-stu-id="e5da9-107">First, data descriptions use only a format identifier, such as the single 16-bit clipboard format identifier on Windows, which means the clipboard can only describe the structure of its data, that is, the ordering of the bits.</span></span> <span data-ttu-id="e5da9-108">Puede notificar, "tengo un mapa de bits" o tengo algo de texto ", pero no puede especificar los dispositivos de destino para los que se componen los datos, qué vistas o aspectos de los datos pueden proporcionar, o qué medios de almacenamiento son más adecuados para su transferencia.</span><span class="sxs-lookup"><span data-stu-id="e5da9-108">It can report, "I have a bitmap" "or I have some text," but it cannot specify the target devices for which the data is composed, which views or aspects of itself the data can provide, or which storage media are best suited for its transfer.</span></span> <span data-ttu-id="e5da9-109">Por ejemplo, no puede notificar, "tengo una cadena de texto que se almacena en memoria global y con formato para presentación en pantalla o en una impresora" o "tengo un mapa de bits de boceto en miniatura representado para una impresora de matriz de puntos de PPP 100 y se almacena como un archivo de disco".</span><span class="sxs-lookup"><span data-stu-id="e5da9-109">For example, it cannot report, "I have a string of text that is stored in global memory and formatted for presentation either on screen or on a printer" or "I have a thumbnail sketch bitmap rendered for a 100 dpi dot-matrix printer and stored as a disk file."</span></span>

<span data-ttu-id="e5da9-110">En segundo lugar, todas las transferencias de datos mediante el portapapeles suelen producirse a través de la memoria global.</span><span class="sxs-lookup"><span data-stu-id="e5da9-110">Second, all data transfers using the clipboard generally occur through global memory.</span></span> <span data-ttu-id="e5da9-111">El uso de memoria global es razonablemente eficaz para pequeñas cantidades de datos, pero horriblemente ineficaz para grandes cantidades, como un objeto multimedia de 20 MB.</span><span class="sxs-lookup"><span data-stu-id="e5da9-111">Using global memory is reasonably efficient for small amounts of data but horribly inefficient for large amounts, such as a 20 MB multimedia object.</span></span> <span data-ttu-id="e5da9-112">La memoria global es lenta para un objeto de datos de gran tamaño, cuyo tamaño requiere un intercambio considerable a la memoria virtual en el disco.</span><span class="sxs-lookup"><span data-stu-id="e5da9-112">Global memory is slow for a large data object, whose size requires considerable swapping to virtual memory on disk.</span></span> <span data-ttu-id="e5da9-113">En los casos en los que los datos que se intercambian van a residir principalmente en el disco, forzarlo a través de este cuello de botella de la memoria virtual es muy ineficaz.</span><span class="sxs-lookup"><span data-stu-id="e5da9-113">In cases where the data being exchanged is going to reside mostly on disk anyway, forcing it through this virtual-memory bottleneck is highly inefficient.</span></span> <span data-ttu-id="e5da9-114">Una manera mejor sería omitir completamente la memoria global y simplemente transferir los datos directamente al disco.</span><span class="sxs-lookup"><span data-stu-id="e5da9-114">A better way would skip global memory entirely and simply transfer the data directly to disk.</span></span>

<span data-ttu-id="e5da9-115">Para mitigar estos problemas, COM proporciona dos estructuras de datos: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span><span class="sxs-lookup"><span data-stu-id="e5da9-115">To alleviate these problems, COM provides two data structures: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) and [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span></span> <span data-ttu-id="e5da9-116">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e5da9-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e5da9-117">La estructura FORMATETC</span><span class="sxs-lookup"><span data-stu-id="e5da9-117">The FORMATETC Structure</span></span>](the-formatetc-structure.md)
-   [<span data-ttu-id="e5da9-118">La estructura STGMEDIUM</span><span class="sxs-lookup"><span data-stu-id="e5da9-118">The STGMEDIUM Structure</span></span>](the-stgmedium-structure.md)

## <a name="related-topics"></a><span data-ttu-id="e5da9-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5da9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5da9-120">Transferencia de datos</span><span class="sxs-lookup"><span data-stu-id="e5da9-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




