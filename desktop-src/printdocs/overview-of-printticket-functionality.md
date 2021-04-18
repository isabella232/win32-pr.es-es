---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Información general sobre la funcionalidad de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a70945fcc18e08615a9674a90a023f4ee12a76e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105660019"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="3155e-104">Información general sobre la funcionalidad de PrintTicket</span><span class="sxs-lookup"><span data-stu-id="3155e-104">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="3155e-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="3155e-105">This topic is not current.</span></span> <span data-ttu-id="3155e-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3155e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3155e-107">El PrintTicket usa un formato basado en XML para expresar la información de configuración del dispositivo mediante la característica/opción y las construcciones de parámetros del marco de trabajo del esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="3155e-107">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="3155e-108">Esto incluye todos los tipos de elemento estándar, así como las capacidades de extensibilidad del marco de trabajo de esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="3155e-108">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="3155e-109">Se supone que un PrintTicket es una descripción independiente del modo en que se va a procesar una sola página.</span><span class="sxs-lookup"><span data-stu-id="3155e-109">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="3155e-110">Aquí no se explican los pasos necesarios para extraer y construir este PrintTicket a partir de un formato de documento determinado.</span><span class="sxs-lookup"><span data-stu-id="3155e-110">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="3155e-111">Un PrintTicket se puede usar para obtener un documento de PrintCapabilities que describe las características del dispositivo para una configuración determinada.</span><span class="sxs-lookup"><span data-stu-id="3155e-111">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="3155e-112">Como alternativa, se puede enviar el PrintTicket con un conjunto de instrucciones de representación para generar una página de salida representada y procesada según la configuración especificada en el PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="3155e-112">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3155e-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3155e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3155e-114">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="3155e-114">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



