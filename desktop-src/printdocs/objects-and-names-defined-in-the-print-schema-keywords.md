---
description: El marco de trabajo de esquema de impresión define un espacio de nombres que incluye los elementos y atributos XML definidos en las palabras clave de esquema de impresión.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Objetos y nombres definidos en las palabras clave de esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408558"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="ef442-103">Objetos y nombres definidos en las palabras clave de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ef442-103">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="ef442-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="ef442-104">This topic is not current.</span></span> <span data-ttu-id="ef442-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ef442-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ef442-106">El marco de trabajo de esquema de impresión define un espacio de nombres que incluye los elementos y atributos XML definidos en las palabras clave de esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="ef442-106">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="ef442-107">Esto incluye elementos como Feature, Option y ScoredProperty; nombres de atributo como name y propagate; y valores para atributos XML, como restringidos.</span><span class="sxs-lookup"><span data-stu-id="ef442-107">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="ef442-108">En otras palabras, cada uso de un nombre definido en las palabras clave de esquema de impresión debe calificarse explícitamente con este espacio de nombres o debe asociarse implícitamente a este espacio de nombres mediante el uso de un atributo xmlns predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ef442-108">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="ef442-109">El documento Palabras clave de esquema de impresión define las instancias de elementos públicos que pueden aparecer en cualquier contexto o ubicación determinados.</span><span class="sxs-lookup"><span data-stu-id="ef442-109">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="ef442-110">Las instancias de elemento solo deben aparecer dentro del contexto o la ubicación designados en el marco de esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="ef442-110">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="ef442-111">Por ejemplo, la instancia de <psf:Option name= "psk:Letter"> definida en las palabras clave de esquema de impresión debe aparecer dentro de la instancia de <psf:Feature name = "psk:PageMediaSize"> (también se define en las palabras clave de esquema de impresión).</span><span class="sxs-lookup"><span data-stu-id="ef442-111">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="ef442-112">No tiene la libertad de usar una instancia de Option determinada fuera de su contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="ef442-112">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="ef442-113">Las instancias de elementos definidas de forma privada pueden aparecer en cualquier lugar, siempre que el tipo de elemento aparezca en un contexto permitido por el marco de esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="ef442-113">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef442-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef442-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef442-115">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ef442-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



