---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Qué es un documento de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e18082a5e551f3997dad8b9688d84ff2f824a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707607"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="5c293-104">Qué es un documento de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="5c293-104">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="5c293-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="5c293-105">This topic is not current.</span></span> <span data-ttu-id="5c293-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5c293-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5c293-107">Merece la pena enumerar parte de la funcionalidad y la información que el documento de PrintCapabilities no debe proporcionar.</span><span class="sxs-lookup"><span data-stu-id="5c293-107">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="5c293-108">Un documento de PrintCapabilities:</span><span class="sxs-lookup"><span data-stu-id="5c293-108">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="5c293-109">No representa datos multivalor (dependiente de la configuración).</span><span class="sxs-lookup"><span data-stu-id="5c293-109">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="5c293-110">Cada documento de PrintCapabilities se construye para una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="5c293-110">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="5c293-111">Ninguna propiedad o ScoredProperty del documento puede tener un valor que dependa de la configuración determinada.</span><span class="sxs-lookup"><span data-stu-id="5c293-111">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="5c293-112">En la versión de esquema inicial, el proveedor de PrintCapabilities debe procesar el PrintTicket de entrada y crear un documento de PrintCapabilities que contenga los valores de propiedad adecuados para la configuración especificada en el PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5c293-112">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="5c293-113">No contiene información de restricciones.</span><span class="sxs-lookup"><span data-stu-id="5c293-113">Does not contain constraint information.</span></span>

    <span data-ttu-id="5c293-114">El documento de PrintCapabilities no indica qué configuraciones están permitidas y cuáles no.</span><span class="sxs-lookup"><span data-stu-id="5c293-114">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="5c293-115">En la versión de esquema inicial, el proveedor de PrintCapabilities debe almacenar toda la información necesaria para validar las configuraciones, proporcionar un método que valide el PrintTicket de entrada y devolver un PrintTicket corregido en caso de que el PrintTicket especificado infrinja una o más restricciones.</span><span class="sxs-lookup"><span data-stu-id="5c293-115">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="5c293-116">No contiene información dinámica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c293-116">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="5c293-117">Hay demasiada sobrecarga en la creación del documento de PrintCapabilities para que se utilice para mantener la información de estado cambiante, como los niveles de tinta, el papel restante en cada bandeja o el estado del atasco de papel.</span><span class="sxs-lookup"><span data-stu-id="5c293-117">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c293-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c293-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c293-119">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5c293-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



