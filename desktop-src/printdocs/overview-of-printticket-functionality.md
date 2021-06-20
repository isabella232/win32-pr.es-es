---
description: En esta introducción a la funcionalidad PrintTicket se describe el formato para expresar la información de configuración del dispositivo y el uso de un PrintTicket.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Información general sobre la funcionalidad PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408548"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="811a0-103">Información general sobre la funcionalidad PrintTicket</span><span class="sxs-lookup"><span data-stu-id="811a0-103">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="811a0-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="811a0-104">This topic is not current.</span></span> <span data-ttu-id="811a0-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="811a0-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="811a0-106">PrintTicket usa un formato basado en XML para expresar la información de configuración del dispositivo mediante las construcciones feature/option y de parámetros de Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="811a0-106">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="811a0-107">Esto incluye todos los tipos de elementos estándar, así como las funcionalidades de extensibilidad de Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="811a0-107">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="811a0-108">Se supone que printticket es una descripción independiente de cómo se va a procesar una sola página.</span><span class="sxs-lookup"><span data-stu-id="811a0-108">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="811a0-109">Los pasos necesarios para extraer y construir este tipo de PrintTicket a partir de un formato de documento determinado no se tratan aquí.</span><span class="sxs-lookup"><span data-stu-id="811a0-109">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="811a0-110">Un PrintTicket se puede usar para obtener un documento PrintCapabilities que describa las características del dispositivo para una configuración determinada.</span><span class="sxs-lookup"><span data-stu-id="811a0-110">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="811a0-111">Como alternativa, PrintTicket se puede enviar con un conjunto de instrucciones de representación para generar una página de salida que se represente y procese según la configuración especificada en PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="811a0-111">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="811a0-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="811a0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="811a0-113">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="811a0-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



