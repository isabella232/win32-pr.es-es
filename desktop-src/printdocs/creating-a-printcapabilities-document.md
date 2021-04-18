---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Crear un documento de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707581"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="b39a4-104">Crear un documento de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="b39a4-104">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="b39a4-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="b39a4-105">This topic is not current.</span></span> <span data-ttu-id="b39a4-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b39a4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b39a4-107">Una vez validada una PrintTicket, se puede usar para crear una instantánea de la PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b39a4-107">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="b39a4-108">El proveedor debe tener una representación interna para cualquier propiedad cuyo valor dependa de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b39a4-108">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="b39a4-109">Por ejemplo, si SpotDiameter es una propiedad que depende de las características Resolution y MediaType, puede aparecer una representación interna de SpotDiameter en relación con los distintos valores para la resolución y el valor de MediaType, tal como se muestra en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="b39a4-109">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="b39a4-110">Solución</span><span class="sxs-lookup"><span data-stu-id="b39a4-110">Resolution</span></span>      | <span data-ttu-id="b39a4-111">MediaType</span><span class="sxs-lookup"><span data-stu-id="b39a4-111">MediaType</span></span>         | <span data-ttu-id="b39a4-112">SpotDiameter</span><span class="sxs-lookup"><span data-stu-id="b39a4-112">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="b39a4-113">300</span><span class="sxs-lookup"><span data-stu-id="b39a4-113">300</span></span><br/>  | <span data-ttu-id="b39a4-114">Obligación</span><span class="sxs-lookup"><span data-stu-id="b39a4-114">Bond</span></span><br/>   | <span data-ttu-id="b39a4-115">520</span><span class="sxs-lookup"><span data-stu-id="b39a4-115">520</span></span><br/> |
| <span data-ttu-id="b39a4-116">300</span><span class="sxs-lookup"><span data-stu-id="b39a4-116">300</span></span><br/>  | <span data-ttu-id="b39a4-117">Fotográfico</span><span class="sxs-lookup"><span data-stu-id="b39a4-117">Glossy</span></span><br/> | <span data-ttu-id="b39a4-118">350</span><span class="sxs-lookup"><span data-stu-id="b39a4-118">350</span></span><br/> |
| <span data-ttu-id="b39a4-119">600</span><span class="sxs-lookup"><span data-stu-id="b39a4-119">600</span></span><br/>  | <span data-ttu-id="b39a4-120">Obligación</span><span class="sxs-lookup"><span data-stu-id="b39a4-120">Bond</span></span><br/>   | <span data-ttu-id="b39a4-121">330</span><span class="sxs-lookup"><span data-stu-id="b39a4-121">330</span></span><br/> |
| <span data-ttu-id="b39a4-122">600</span><span class="sxs-lookup"><span data-stu-id="b39a4-122">600</span></span><br/>  | <span data-ttu-id="b39a4-123">Fotográfico</span><span class="sxs-lookup"><span data-stu-id="b39a4-123">Glossy</span></span><br/> | <span data-ttu-id="b39a4-124">180</span><span class="sxs-lookup"><span data-stu-id="b39a4-124">180</span></span><br/> |
| <span data-ttu-id="b39a4-125">1200</span><span class="sxs-lookup"><span data-stu-id="b39a4-125">1200</span></span><br/> | <span data-ttu-id="b39a4-126">Obligación</span><span class="sxs-lookup"><span data-stu-id="b39a4-126">Bond</span></span><br/>   | <span data-ttu-id="b39a4-127">250</span><span class="sxs-lookup"><span data-stu-id="b39a4-127">250</span></span><br/> |
| <span data-ttu-id="b39a4-128">1200</span><span class="sxs-lookup"><span data-stu-id="b39a4-128">1200</span></span><br/> | <span data-ttu-id="b39a4-129">Fotográfico</span><span class="sxs-lookup"><span data-stu-id="b39a4-129">Glossy</span></span><br/> | <span data-ttu-id="b39a4-130">100</span><span class="sxs-lookup"><span data-stu-id="b39a4-130">100</span></span><br/> |



 

<span data-ttu-id="b39a4-131">En este ejemplo, el proveedor de PrintCapabilities debe usar el elemento PrintTicket proporcionado para seleccionar la entrada adecuada de la tabla interna e informar como el valor de la propiedad SpotDiameter.</span><span class="sxs-lookup"><span data-stu-id="b39a4-131">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="b39a4-132">Este proceso se repite para cada propiedad de varios valores (para cada propiedad cuyo valor depende de la configuración).</span><span class="sxs-lookup"><span data-stu-id="b39a4-132">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="b39a4-133">En la sección [esquema de PrintCapabilities y construcción de documentos](printcapabilities-schema-and-document-construction.md) se describen los demás pasos implicados en la creación de una instantánea de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b39a4-133">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="b39a4-134">Para crear una instantánea del documento de PrintCapabilities predeterminado, proporcione un PrintTicket predeterminado (en lugar de un PrintTicket arbitrario) al método que crea los documentos de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b39a4-134">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b39a4-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b39a4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b39a4-136">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="b39a4-136">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




