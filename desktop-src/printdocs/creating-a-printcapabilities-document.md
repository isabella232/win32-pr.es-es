---
description: Una vez validado printTicket, se puede usar para crear una instantánea de PrintCapabilities.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Creación de un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96ea51cef9dfd0f351704b3b71a7f6163737736
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409518"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="b795a-103">Creación de un documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="b795a-103">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="b795a-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="b795a-104">This topic is not current.</span></span> <span data-ttu-id="b795a-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b795a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b795a-106">Una vez validado printTicket, se puede usar para crear una instantánea de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b795a-106">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="b795a-107">El proveedor debe tener una representación interna para cualquier propiedad cuyo valor dependa de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b795a-107">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="b795a-108">Por ejemplo, si SpotDiameter es una propiedad que depende de las características Resolution y MediaType, una representación interna de SpotDiameter en relación con los distintos valores de Resolution y MediaType podría aparecer como en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="b795a-108">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="b795a-109">Solución</span><span class="sxs-lookup"><span data-stu-id="b795a-109">Resolution</span></span>      | <span data-ttu-id="b795a-110">MediaType</span><span class="sxs-lookup"><span data-stu-id="b795a-110">MediaType</span></span>         | <span data-ttu-id="b795a-111">SpotDiameter</span><span class="sxs-lookup"><span data-stu-id="b795a-111">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="b795a-112">300</span><span class="sxs-lookup"><span data-stu-id="b795a-112">300</span></span><br/>  | <span data-ttu-id="b795a-113">vinculación</span><span class="sxs-lookup"><span data-stu-id="b795a-113">Bond</span></span><br/>   | <span data-ttu-id="b795a-114">520</span><span class="sxs-lookup"><span data-stu-id="b795a-114">520</span></span><br/> |
| <span data-ttu-id="b795a-115">300</span><span class="sxs-lookup"><span data-stu-id="b795a-115">300</span></span><br/>  | <span data-ttu-id="b795a-116">Brillante</span><span class="sxs-lookup"><span data-stu-id="b795a-116">Glossy</span></span><br/> | <span data-ttu-id="b795a-117">350</span><span class="sxs-lookup"><span data-stu-id="b795a-117">350</span></span><br/> |
| <span data-ttu-id="b795a-118">600</span><span class="sxs-lookup"><span data-stu-id="b795a-118">600</span></span><br/>  | <span data-ttu-id="b795a-119">vinculación</span><span class="sxs-lookup"><span data-stu-id="b795a-119">Bond</span></span><br/>   | <span data-ttu-id="b795a-120">330</span><span class="sxs-lookup"><span data-stu-id="b795a-120">330</span></span><br/> |
| <span data-ttu-id="b795a-121">600</span><span class="sxs-lookup"><span data-stu-id="b795a-121">600</span></span><br/>  | <span data-ttu-id="b795a-122">Brillante</span><span class="sxs-lookup"><span data-stu-id="b795a-122">Glossy</span></span><br/> | <span data-ttu-id="b795a-123">180</span><span class="sxs-lookup"><span data-stu-id="b795a-123">180</span></span><br/> |
| <span data-ttu-id="b795a-124">1200</span><span class="sxs-lookup"><span data-stu-id="b795a-124">1200</span></span><br/> | <span data-ttu-id="b795a-125">vinculación</span><span class="sxs-lookup"><span data-stu-id="b795a-125">Bond</span></span><br/>   | <span data-ttu-id="b795a-126">250</span><span class="sxs-lookup"><span data-stu-id="b795a-126">250</span></span><br/> |
| <span data-ttu-id="b795a-127">1200</span><span class="sxs-lookup"><span data-stu-id="b795a-127">1200</span></span><br/> | <span data-ttu-id="b795a-128">Brillante</span><span class="sxs-lookup"><span data-stu-id="b795a-128">Glossy</span></span><br/> | <span data-ttu-id="b795a-129">100</span><span class="sxs-lookup"><span data-stu-id="b795a-129">100</span></span><br/> |



 

<span data-ttu-id="b795a-130">En este ejemplo, el proveedor PrintCapabilities debe usar el printTicket proporcionado para seleccionar la entrada adecuada de la tabla interna y notificarlo como valor de la propiedad SpotDiameter.</span><span class="sxs-lookup"><span data-stu-id="b795a-130">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="b795a-131">Este proceso se repite para cada propiedad multivalor (para cada propiedad cuyo valor depende de la configuración).</span><span class="sxs-lookup"><span data-stu-id="b795a-131">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="b795a-132">En [la sección Esquema de PrintCapabilities](printcapabilities-schema-and-document-construction.md) y Construcción de documentos se describen los demás pasos necesarios para crear una instantánea de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b795a-132">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="b795a-133">Para crear una instantánea del documento PrintCapabilities predeterminado, proporcione un PrintTicket predeterminado (en lugar de un PrintTicket arbitrario) al método que crea documentos PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b795a-133">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b795a-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b795a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b795a-135">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="b795a-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




