---
title: Documento como instantánea de propiedades
description: Revise el documento PrintCapabilities como una instantánea de las propiedades. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399c82211c268a72ad2b67082c144c64e46a879
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118650"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a><span data-ttu-id="042b3-105">Documento PrintCapabilities como instantánea de propiedades</span><span class="sxs-lookup"><span data-stu-id="042b3-105">PrintCapabilities Document as a Snapshot of Properties</span></span>

<span data-ttu-id="042b3-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="042b3-106">This topic is not current.</span></span> <span data-ttu-id="042b3-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="042b3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="042b3-108">El dispositivo descrito por PrintCapabilities puede tener propiedades que dependen del estado o la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="042b3-108">The device described by the PrintCapabilities might have properties that depend on the state or configuration of the device.</span></span> <span data-ttu-id="042b3-109">Aunque PrintCapabilities representa el espacio de configuración completo de un dispositivo, el proveedor PrintCapabilities genera una instancia dependiente de la configuración de PrintCapabilities denominada documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="042b3-109">While the PrintCapabilities represents the full configuration space of a device, the PrintCapabilities provider produces a configuration-dependent instance of the PrintCapabilities called the PrintCapabilities document.</span></span> <span data-ttu-id="042b3-110">Este documento PrintCapabilities dependiente de la configuración evita cargar el esquema PrintCapabilities con la complejidad de representar datos de varios valores.</span><span class="sxs-lookup"><span data-stu-id="042b3-110">This configuration-dependent PrintCapabilities document avoids burdening the PrintCapabilities Schema with the complexity of representing multivalued data.</span></span> <span data-ttu-id="042b3-111">Lo que es más importante, para liberar a un consumidor del documento PrintCapabilities de la carga de extraer el valor adecuado de una representación de datos de varios valores, todas las instancias property y ScoredProperty de un documento PrintCapabilities deben tener un solo valor.</span><span class="sxs-lookup"><span data-stu-id="042b3-111">More importantly, to relieve a consumer of the PrintCapabilities document from the burden of extracting the appropriate value from a multivalued data representation, all Property and ScoredProperty instances in a PrintCapabilities document are required to be single-valued.</span></span> <span data-ttu-id="042b3-112">En otras palabras, cada instancia de Property y ScoredProperty de un documento PrintCapabilities debe tener un valor fijo, relativo a la configuración de entrada.</span><span class="sxs-lookup"><span data-stu-id="042b3-112">In other words, each Property and ScoredProperty instance in a PrintCapabilities document must have a fixed Value, relative to the input configuration.</span></span> <span data-ttu-id="042b3-113">Cada documento PrintCapabilities se puede pensar en como una instantánea de las propiedades del dispositivo cuando el dispositivo está en un estado determinado.</span><span class="sxs-lookup"><span data-stu-id="042b3-113">Each PrintCapabilities document can be thought of as a snapshot of the properties of the device when the device is in a particular state.</span></span> <span data-ttu-id="042b3-114">Por lo tanto, antes de que se pueda construir un documento PrintCapabilities, se debe proporcionar la configuración que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="042b3-114">Consequently, before a PrintCapabilities document can be constructed, the configuration to be used must be provided.</span></span>

## <a name="related-topics"></a><span data-ttu-id="042b3-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="042b3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="042b3-116">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="042b3-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



