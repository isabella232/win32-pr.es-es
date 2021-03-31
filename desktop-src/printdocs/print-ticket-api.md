---
description: Print ticket API proporciona permite a las aplicaciones administrar y convertir vales de impresión.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: Print ticket API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104083596"
---
# <a name="print-ticket-api"></a><span data-ttu-id="8fd6d-103">Print ticket API</span><span class="sxs-lookup"><span data-stu-id="8fd6d-103">Print Ticket API</span></span>

<span data-ttu-id="8fd6d-104">Print ticket API proporciona permite a las aplicaciones administrar y convertir vales de impresión.</span><span class="sxs-lookup"><span data-stu-id="8fd6d-104">The Print Ticket API provides enables applications to manage and convert print tickets.</span></span>

<span data-ttu-id="8fd6d-105">Una solicitud de impresión es un componente de documento XPS que contiene la configuración de impresora preferida para una página de un documento o para un documento completo, o para un trabajo de impresión que contiene uno o varios documentos.</span><span class="sxs-lookup"><span data-stu-id="8fd6d-105">A print ticket is an XPS document component that contains the preferred printer settings for a page in a document, or for an entire document, or for a print job that contains one or more documents.</span></span> <span data-ttu-id="8fd6d-106">Tenga en cuenta que los vales de impresión solo se encuentran en los documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="8fd6d-106">Note that print tickets are only found in XPS documents.</span></span>

<span data-ttu-id="8fd6d-107">Para que la impresora pueda usar el vale de impresión, la solicitud de impresión debe validarse con las características de la impresora, que se definen en las capacidades de impresión de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8fd6d-107">Before the printer can use the print ticket, the print ticket must be validated against the printer's characteristics, which are defined in the printer's Print Capabilities.</span></span> <span data-ttu-id="8fd6d-108">La aplicación realiza esa validación mediante una llamada a la API Print ticket.</span><span class="sxs-lookup"><span data-stu-id="8fd6d-108">The application performs that validation by calling the Print Ticket API.</span></span>

<span data-ttu-id="8fd6d-109">El PrintTicket y PrintCapabilities se describen mediante el uso de elementos del esquema de impresión, que se define mediante la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8fd6d-109">The PrintTicket and PrintCapabilities are described by using elements of the Print Schema, which is defined by the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8fd6d-110">Este tema contiene información sobre los siguientes elementos de la API:</span><span class="sxs-lookup"><span data-stu-id="8fd6d-110">This topic contains information about the following API elements:</span></span>

-   [<span data-ttu-id="8fd6d-111">Funciones de la API Print ticket</span><span class="sxs-lookup"><span data-stu-id="8fd6d-111">Print Ticket API Functions</span></span>](print-ticket-api-functions.md)
-   [<span data-ttu-id="8fd6d-112">Print ticket API (enumeraciones)</span><span class="sxs-lookup"><span data-stu-id="8fd6d-112">Print Ticket API Enumerations</span></span>](print-ticket-api-enumerations.md)

<span data-ttu-id="8fd6d-113">En el diagrama siguiente se muestra la relación de la API de la solicitud de impresión con las otras API de impresión que puede usar una aplicación Windows nativa.</span><span class="sxs-lookup"><span data-stu-id="8fd6d-113">The following diagram shows the relationship of the Print Ticket API to the other Print APIs that a native Windows application can use.</span></span>

![un diagrama que muestra la relación de la API de la solicitud de impresión con las otras API de impresión que puede usar una aplicación Windows nativa](images/print-apis-pt.png)

## <a name="related-topics"></a><span data-ttu-id="8fd6d-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8fd6d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fd6d-116">API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="8fd6d-116">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="8fd6d-117">API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8fd6d-117">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="8fd6d-118">API de impresión GDI</span><span class="sxs-lookup"><span data-stu-id="8fd6d-118">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="8fd6d-119">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="8fd6d-119">Print Schema Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[<span data-ttu-id="8fd6d-120">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="8fd6d-120">XML Paper Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



