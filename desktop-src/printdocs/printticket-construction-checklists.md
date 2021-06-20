---
description: Vea cómo el autor de un cliente PrintTicket puede usar tipos de elemento para crear un PrintTicket que describa las intenciones de un dispositivo.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listas de comprobación de construcción de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76d47911d0060cc6d06604bfaeaa4abcebd3daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405478"
---
# <a name="printticket-construction-checklists"></a><span data-ttu-id="4c8e2-103">Listas de comprobación de construcción de PrintTicket</span><span class="sxs-lookup"><span data-stu-id="4c8e2-103">PrintTicket Construction Checklists</span></span>

<span data-ttu-id="4c8e2-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="4c8e2-104">This topic is not current.</span></span> <span data-ttu-id="4c8e2-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4c8e2-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4c8e2-106">En esta sección se muestra cómo el autor de un cliente PrintTicket puede usar los tipos de elementos definidos en el marco de esquema de impresión para crear un PrintTicket que describa las intenciones de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c8e2-106">This section demonstrates how the author of a PrintTicket client can use the element types defined in the Print Schema Framework to create a PrintTicket that describes intents for a device.</span></span> <span data-ttu-id="4c8e2-107">PrintTicket puede ser genérico (no vinculado a un dispositivo específico) o puede ser específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c8e2-107">The PrintTicket can be generic (not tied to a specific device), or it can be device-specific.</span></span> <span data-ttu-id="4c8e2-108">La semántica de PrintTicket se presenta con más detalle.</span><span class="sxs-lookup"><span data-stu-id="4c8e2-108">The semantics of the PrintTicket are presented in greater detail.</span></span> <span data-ttu-id="4c8e2-109">Además, esta sección contiene información general de conceptos y terminología que se tratan con más detalle en secciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c8e2-109">In addition, this section contains an overview of concepts and terminology that are covered in more depth in subsequent sections.</span></span>

<span data-ttu-id="4c8e2-110">Hay dos enfoques fundamentalmente diferentes para construir un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4c8e2-110">There are two fundamentally different approaches to constructing a PrintTicket.</span></span> <span data-ttu-id="4c8e2-111">Se puede usar cualquier enfoque.</span><span class="sxs-lookup"><span data-stu-id="4c8e2-111">Either approach can be used.</span></span>

-   <span data-ttu-id="4c8e2-112">Para dirigir PrintTicket a un dispositivo desconocido o genérico, [cree un PrintTicket genérico.](creating-a-generic-printticket.md)</span><span class="sxs-lookup"><span data-stu-id="4c8e2-112">Target the PrintTicket to an unknown or generic device by [Creating a Generic PrintTicket](creating-a-generic-printticket.md).</span></span>

    <span data-ttu-id="4c8e2-113">Si el objetivo principal es conservar la intención del usuario final, es posible que quiera seguir este enfoque mediante la construcción y el almacenamiento de un printTicket genérico no validado con el documento.</span><span class="sxs-lookup"><span data-stu-id="4c8e2-113">If your primary objective is to preserve the end user's intent, you might want to take this approach, by constructing and storing an unvalidated generic PrintTicket with the document.</span></span>

-   <span data-ttu-id="4c8e2-114">Para dirigir PrintTicket a un dispositivo específico, cree [un Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="4c8e2-114">Target the PrintTicket to a specific device, by [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span>

    <span data-ttu-id="4c8e2-115">Si está más interesado en aprovechar todas las características que ofrece un dispositivo determinado, puede que quiera seguir este enfoque mediante la construcción de un PrintTicket para el dispositivo específico y el almacenamiento del PrintTicket validado con el documento.</span><span class="sxs-lookup"><span data-stu-id="4c8e2-115">If you are more interested in taking advantage of all of the features offered by a particular device, you might want to take this approach, by constructing a PrintTicket for the specific device and storing the validated PrintTicket with the document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c8e2-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c8e2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c8e2-117">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4c8e2-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



