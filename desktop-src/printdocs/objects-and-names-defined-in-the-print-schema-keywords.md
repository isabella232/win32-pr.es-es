---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Objetos y nombres definidos en las palabras clave del esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2347c73dd647f90a88821658cdcf9e2ed846e83
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279859"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="e0fa9-104">Objetos y nombres definidos en las palabras clave del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e0fa9-104">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="e0fa9-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="e0fa9-105">This topic is not current.</span></span> <span data-ttu-id="e0fa9-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e0fa9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e0fa9-107">El marco de trabajo del esquema de impresión define un espacio de nombres que incluye los elementos y los atributos XML definidos en las palabras clave del esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="e0fa9-107">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="e0fa9-108">Esto incluye elementos como Feature, Option y ScoredProperty; nombres de atributo como Name y Propagate; los valores y para los atributos XML, como Constrained.</span><span class="sxs-lookup"><span data-stu-id="e0fa9-108">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="e0fa9-109">En otras palabras, cada uso de un nombre que se define en las palabras clave del esquema de impresión se debe calificar explícitamente con este espacio de nombres o se debe asociar implícitamente a este espacio de nombres mediante el uso de un atributo xmlns predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e0fa9-109">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="e0fa9-110">El documento imprimir palabras clave del esquema define las instancias del elemento público que pueden aparecer en cualquier contexto o ubicación determinados.</span><span class="sxs-lookup"><span data-stu-id="e0fa9-110">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="e0fa9-111">Las instancias de elemento deben aparecer solo en el contexto o la ubicación designada en el marco de trabajo del esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="e0fa9-111">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="e0fa9-112">Por ejemplo, la <PSF: Option name = "PSK: Letter" > instancia que se define en las palabras clave del esquema de impresión debe aparecer dentro de la <PSF: Feature name = "PSK: PageMediaSize" > (también se define en las palabras clave del esquema de impresión).</span><span class="sxs-lookup"><span data-stu-id="e0fa9-112">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="e0fa9-113">No tiene la libertad de usar una instancia de opción determinada fuera de su contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="e0fa9-113">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="e0fa9-114">Las instancias de elementos definidas de forma privada pueden aparecer en cualquier parte siempre que el tipo de elemento aparezca en un contexto permitido por el marco de trabajo del esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="e0fa9-114">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0fa9-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0fa9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0fa9-116">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e0fa9-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



