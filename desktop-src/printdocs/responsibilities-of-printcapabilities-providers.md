---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilidades de los proveedores de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bbf355f7b62f8f9c8b3f3b0c59714cdd6ade5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698002"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="5a6f7-104">Responsabilidades de los proveedores de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="5a6f7-104">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="5a6f7-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-105">This topic is not current.</span></span> <span data-ttu-id="5a6f7-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5a6f7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5a6f7-107">Los proveedores de PrintCapabilities deben admitir un conjunto mínimo de funciones, que son implícitas por la interfaz del proveedor de PrintTicket/PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-107">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="5a6f7-108">Estas funcionalidades se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-108">These capabilities are listed here.</span></span>

-   <span data-ttu-id="5a6f7-109">Deben seguir la dirección de la propagación? Atributo XML, cuando aparece en el contexto adecuado y contiene un valor válido para ese contexto.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-109">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="5a6f7-110">Deben generar un documento de PrintCapabilities que se ajuste al esquema de PrintCapabilities y satisfaga los requisitos especificados en el esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-110">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="5a6f7-111">Deben ser capaces de reconocer un PrintTicket válido.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-111">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="5a6f7-112">Deben ser capaces de interpretar un PrintTicket y comprender la configuración específica que representa.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-112">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="5a6f7-113">Deben ser capaces de determinar si la configuración contiene conflictos de restricción.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-113">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="5a6f7-114">Deben poder modificar un PrintTicket no válido o en conflicto mediante la realización del cambio menos significativo necesario para que sea válido y sin conflictos.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-114">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="5a6f7-115">Deben poder generar un documento de PrintCapabilities para una configuración de dispositivo concreta.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-115">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="5a6f7-116">Deben poder generar una configuración o un PrintTicket predeterminados.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-116">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="5a6f7-117">Deben poder generar un documento de PrintCapabilities que se corresponda con la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-117">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="5a6f7-118">Deben implementar un proceso de puntuación de opciones definido por el controlador de dispositivo capaz de determinar la proximidad de la coincidencia entre dos instancias de opción que pertenecen a la misma característica.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-118">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="5a6f7-119">Este algoritmo se usa en el proceso de validación de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-119">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="5a6f7-120">Además de los requisitos anteriores, el documento de PrintCapabilities debe contener valores válidos y correctos para cada atributo XML (por ejemplo, restringido) de cada opción.</span><span class="sxs-lookup"><span data-stu-id="5a6f7-120">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a6f7-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a6f7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a6f7-122">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5a6f7-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



