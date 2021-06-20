---
description: Obtenga información sobre algunas de las funcionalidades y la información que el documento PrintCapabilities no pretende proporcionar.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Qué no es un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcd5dbedf6ee3a7e2713bd3591b182c606cfb0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409898"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="afb99-103">Qué no es un documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="afb99-103">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="afb99-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="afb99-104">This topic is not current.</span></span> <span data-ttu-id="afb99-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="afb99-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="afb99-106">Merece la pena enumerar parte de la funcionalidad y la información que el documento PrintCapabilities no pretende proporcionar.</span><span class="sxs-lookup"><span data-stu-id="afb99-106">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="afb99-107">Un documento PrintCapabilities:</span><span class="sxs-lookup"><span data-stu-id="afb99-107">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="afb99-108">No representa datos multivalor (dependientes de la configuración).</span><span class="sxs-lookup"><span data-stu-id="afb99-108">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="afb99-109">Cada documento PrintCapabilities se construye para una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="afb99-109">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="afb99-110">Ninguna propiedad o ScoredProperty en el documento puede tener un valor que dependa de la configuración determinada.</span><span class="sxs-lookup"><span data-stu-id="afb99-110">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="afb99-111">En la versión inicial del esquema, el proveedor PrintCapabilities debe procesar la entrada PrintTicket y crear un documento PrintCapabilities que contenga los valores property adecuados para la configuración especificada en PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="afb99-111">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="afb99-112">No contiene información de restricción.</span><span class="sxs-lookup"><span data-stu-id="afb99-112">Does not contain constraint information.</span></span>

    <span data-ttu-id="afb99-113">El documento PrintCapabilities no indica qué configuraciones se permiten y cuáles no.</span><span class="sxs-lookup"><span data-stu-id="afb99-113">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="afb99-114">En la versión inicial del esquema, el proveedor PrintCapabilities debe almacenar toda la información necesaria para validar las configuraciones, proporcionar un método que valide la entrada PrintTicket y devolver un PrintTicket corregido en caso de que el PrintTicket especificado infrinja una o varias restricciones.</span><span class="sxs-lookup"><span data-stu-id="afb99-114">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="afb99-115">No contiene información dinámica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="afb99-115">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="afb99-116">Hay demasiada sobrecarga implicada en la construcción del documento PrintCapabilities para que se utilice para contener información de estado que cambia rápidamente, como los niveles de entrada de lápiz, el papel restante en cada bandeja o el estado de la entrada de papel.</span><span class="sxs-lookup"><span data-stu-id="afb99-116">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afb99-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="afb99-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afb99-118">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="afb99-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



