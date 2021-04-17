---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listas de comprobación de construcción de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105697986"
---
# <a name="printticket-construction-checklists"></a><span data-ttu-id="6517e-104">Listas de comprobación de construcción de PrintTicket</span><span class="sxs-lookup"><span data-stu-id="6517e-104">PrintTicket Construction Checklists</span></span>

<span data-ttu-id="6517e-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="6517e-105">This topic is not current.</span></span> <span data-ttu-id="6517e-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6517e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6517e-107">En esta sección se muestra cómo el autor de un cliente PrintTicket puede usar los tipos de elemento definidos en el marco de trabajo del esquema de impresión para crear un PrintTicket que describa los intentos de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6517e-107">This section demonstrates how the author of a PrintTicket client can use the element types defined in the Print Schema Framework to create a PrintTicket that describes intents for a device.</span></span> <span data-ttu-id="6517e-108">El PrintTicket puede ser genérico (no vinculado a un dispositivo específico) o puede ser específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6517e-108">The PrintTicket can be generic (not tied to a specific device), or it can be device-specific.</span></span> <span data-ttu-id="6517e-109">La semántica del PrintTicket se presenta con mayor detalle.</span><span class="sxs-lookup"><span data-stu-id="6517e-109">The semantics of the PrintTicket are presented in greater detail.</span></span> <span data-ttu-id="6517e-110">Además, esta sección contiene información general sobre los conceptos y la terminología que se describen con más detalle en secciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6517e-110">In addition, this section contains an overview of concepts and terminology that are covered in more depth in subsequent sections.</span></span>

<span data-ttu-id="6517e-111">Hay dos enfoques fundamentalmente diferentes para construir un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6517e-111">There are two fundamentally different approaches to constructing a PrintTicket.</span></span> <span data-ttu-id="6517e-112">Se puede usar cualquiera de estos enfoques.</span><span class="sxs-lookup"><span data-stu-id="6517e-112">Either approach can be used.</span></span>

-   <span data-ttu-id="6517e-113">Destine el PrintTicket a un dispositivo genérico o desconocido mediante la [creación de un PrintTicket genérico](creating-a-generic-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="6517e-113">Target the PrintTicket to an unknown or generic device by [Creating a Generic PrintTicket](creating-a-generic-printticket.md).</span></span>

    <span data-ttu-id="6517e-114">Si el objetivo principal es conservar la intención del usuario final, es posible que quiera tomar este enfoque mediante la construcción y el almacenamiento de un PrintTicket genérico no validado con el documento.</span><span class="sxs-lookup"><span data-stu-id="6517e-114">If your primary objective is to preserve the end user's intent, you might want to take this approach, by constructing and storing an unvalidated generic PrintTicket with the document.</span></span>

-   <span data-ttu-id="6517e-115">Establecer como destino el PrintTicket en un dispositivo específico mediante la [creación de un Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="6517e-115">Target the PrintTicket to a specific device, by [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span>

    <span data-ttu-id="6517e-116">Si está más interesado en sacar provecho de todas las características que ofrece un dispositivo determinado, puede tomar este enfoque mediante la construcción de un PrintTicket para el dispositivo específico y el almacenamiento del PrintTicket validado con el documento.</span><span class="sxs-lookup"><span data-stu-id="6517e-116">If you are more interested in taking advantage of all of the features offered by a particular device, you might want to take this approach, by constructing a PrintTicket for the specific device and storing the validated PrintTicket with the document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6517e-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6517e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6517e-118">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="6517e-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



