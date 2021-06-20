---
description: Los proveedores de PrintCapabilities deben admitir un conjunto mínimo de funcionalidades, que están implícitas en la interfaz del proveedor PrintTicket/PrintCapabilities.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilidades de los proveedores de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc04137eacdd2395205b96233db3c53964bc02
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404918"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="6977b-103">Responsabilidades de los proveedores de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="6977b-103">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="6977b-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="6977b-104">This topic is not current.</span></span> <span data-ttu-id="6977b-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6977b-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6977b-106">Los proveedores de PrintCapabilities deben admitir un conjunto mínimo de funcionalidades, que están implícitas en la interfaz del proveedor PrintTicket/PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="6977b-106">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="6977b-107">Esta funcionalidad se incluye a continuación.</span><span class="sxs-lookup"><span data-stu-id="6977b-107">These capabilities are listed here.</span></span>

-   <span data-ttu-id="6977b-108">¿Deben seguir la dirección de la propagación?? Atributo XML, cuando aparece en el contexto adecuado y contiene un valor válido para ese contexto.</span><span class="sxs-lookup"><span data-stu-id="6977b-108">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="6977b-109">Deben generar un documento PrintCapabilities que se ajuste al esquema PrintCapabilities y cumpla los requisitos especificados en el esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="6977b-109">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="6977b-110">Deben poder reconocer un PrintTicket válido.</span><span class="sxs-lookup"><span data-stu-id="6977b-110">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="6977b-111">Deben poder interpretar un PrintTicket y comprender la configuración específica que representa.</span><span class="sxs-lookup"><span data-stu-id="6977b-111">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="6977b-112">Deben ser capaces de determinar si esa configuración contiene conflictos de restricción.</span><span class="sxs-lookup"><span data-stu-id="6977b-112">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="6977b-113">Deben poder modificar un PrintTicket no válido o en conflicto realizando el cambio menos significativo necesario para que sea válido y sin conflictos.</span><span class="sxs-lookup"><span data-stu-id="6977b-113">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="6977b-114">Deben poder generar un documento PrintCapabilities para una configuración de dispositivo determinada.</span><span class="sxs-lookup"><span data-stu-id="6977b-114">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="6977b-115">Deben poder generar una configuración predeterminada o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6977b-115">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="6977b-116">Deben poder generar un documento PrintCapabilities que se corresponda con la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6977b-116">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="6977b-117">Deben implementar un proceso de puntuación de opciones definido por el controlador de dispositivo capaz de determinar la proximidad de la coincidencia entre dos instancias de opción que pertenecen a la misma característica.</span><span class="sxs-lookup"><span data-stu-id="6977b-117">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="6977b-118">Este algoritmo se usa en el proceso de validación PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6977b-118">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="6977b-119">Además de los requisitos anteriores, el documento PrintCapabilities debe contener valores válidos y correctos para cada atributo XML (por ejemplo, restringido) de cada opción.</span><span class="sxs-lookup"><span data-stu-id="6977b-119">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6977b-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6977b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6977b-121">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="6977b-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



