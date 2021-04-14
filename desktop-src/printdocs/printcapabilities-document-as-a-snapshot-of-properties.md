---
title: Documento como una instantánea de propiedades
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73fc190ed8c259e64fdd60cc291c6ae5b58f80
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424151"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a><span data-ttu-id="91934-104">Documento de PrintCapabilities como una instantánea de propiedades</span><span class="sxs-lookup"><span data-stu-id="91934-104">PrintCapabilities Document as a Snapshot of Properties</span></span>

<span data-ttu-id="91934-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="91934-105">This topic is not current.</span></span> <span data-ttu-id="91934-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="91934-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="91934-107">El dispositivo descrito por la PrintCapabilities puede tener propiedades que dependen del estado o la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91934-107">The device described by the PrintCapabilities might have properties that depend on the state or configuration of the device.</span></span> <span data-ttu-id="91934-108">Mientras que la PrintCapabilities representa el espacio de configuración completo de un dispositivo, el proveedor de PrintCapabilities genera una instancia dependiente de la configuración de la PrintCapabilities denominada documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="91934-108">While the PrintCapabilities represents the full configuration space of a device, the PrintCapabilities provider produces a configuration-dependent instance of the PrintCapabilities called the PrintCapabilities document.</span></span> <span data-ttu-id="91934-109">Este documento de PrintCapabilities dependiente de la configuración evita sobrecargar el esquema de PrintCapabilities con la complejidad de representar datos de varios valores.</span><span class="sxs-lookup"><span data-stu-id="91934-109">This configuration-dependent PrintCapabilities document avoids burdening the PrintCapabilities Schema with the complexity of representing multivalued data.</span></span> <span data-ttu-id="91934-110">Lo que es más importante, para liberar a un consumidor del documento de PrintCapabilities de la carga de extraer el valor adecuado de una representación de datos con varios valores, todas las instancias de Property y ScoredProperty de un documento de PrintCapabilities deben ser de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="91934-110">More importantly, to relieve a consumer of the PrintCapabilities document from the burden of extracting the appropriate value from a multivalued data representation, all Property and ScoredProperty instances in a PrintCapabilities document are required to be single-valued.</span></span> <span data-ttu-id="91934-111">En otras palabras, cada propiedad y la instancia de ScoredProperty de un documento de PrintCapabilities deben tener un valor fijo, con respecto a la configuración de entrada.</span><span class="sxs-lookup"><span data-stu-id="91934-111">In other words, each Property and ScoredProperty instance in a PrintCapabilities document must have a fixed Value, relative to the input configuration.</span></span> <span data-ttu-id="91934-112">Cada documento de PrintCapabilities se puede considerar como una instantánea de las propiedades del dispositivo cuando el dispositivo se encuentra en un estado determinado.</span><span class="sxs-lookup"><span data-stu-id="91934-112">Each PrintCapabilities document can be thought of as a snapshot of the properties of the device when the device is in a particular state.</span></span> <span data-ttu-id="91934-113">Por consiguiente, antes de que se pueda construir un documento de PrintCapabilities, se debe proporcionar la configuración que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="91934-113">Consequently, before a PrintCapabilities document can be constructed, the configuration to be used must be provided.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91934-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91934-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91934-115">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="91934-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



