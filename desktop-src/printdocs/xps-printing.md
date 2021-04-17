---
description: Proporciona una interfaz para el administrador de trabajos de impresión. Las aplicaciones pueden usar esta API para enviar documentos XPS a una impresora.
ms.assetid: df06ddcb-e573-461c-99a3-8f108fe2c143
title: API de impresión XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c53322a8ae6a03c3ac4bb71fc680f719999546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715778"
---
# <a name="xps-print-api"></a><span data-ttu-id="77402-104">API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="77402-104">XPS Print API</span></span>

<span data-ttu-id="77402-105">\[La API de impresión XPS no es compatible y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="77402-105">\[The XPS Print API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="77402-106">En su lugar, las aplicaciones cliente deben usar la [API Print Document Package](./tailored-app-printing-api.md) .\]</span><span class="sxs-lookup"><span data-stu-id="77402-106">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="77402-107">Proporciona una interfaz para el administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="77402-107">Provides an interface to the print spooler.</span></span> <span data-ttu-id="77402-108">Las aplicaciones pueden usar esta API para enviar documentos XPS a una impresora.</span><span class="sxs-lookup"><span data-stu-id="77402-108">Applications can use this API to send XPS documents to a printer.</span></span>

<span data-ttu-id="77402-109">Esta sección contiene información acerca de los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="77402-109">This section contains information about the following topics.</span></span>

<dl>

[<span data-ttu-id="77402-110">Acerca de la API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="77402-110">About the XPS Print API</span></span>](about-xps-print-api.md)  
[<span data-ttu-id="77402-111">Uso de la API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="77402-111">Using the XPS Print API</span></span>](using-the-xps-print-api.md)  
[<span data-ttu-id="77402-112">Referencia de la API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="77402-112">XPS Print API Reference</span></span>](xpsprint-interfaces.md)  
</dl>

<span data-ttu-id="77402-113">Las aplicaciones nativas de Windows que crean documentos XPS, como el uso de la [API de documentos XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)), pueden usar la API de impresión XPS para enviar contenido de documentos XPS a una impresora.</span><span class="sxs-lookup"><span data-stu-id="77402-113">Native Windows applications that create XPS documents, such as by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)), can use the XPS Print API to send XPS document content to a printer.</span></span>

<span data-ttu-id="77402-114">En el diagrama siguiente se muestra la relación de la API de impresión XPS con las otras API de impresión que puede usar una aplicación Windows nativa.</span><span class="sxs-lookup"><span data-stu-id="77402-114">The following diagram shows the relationship of the XPS Print API to the other Print APIs that a native Windows application can use.</span></span>

![un diagrama que muestra la relación de la API de impresión XPS con las otras API de impresión que puede usar una aplicación Windows nativa](images/print-apis-xps.png)

## <a name="related-topics"></a><span data-ttu-id="77402-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77402-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77402-117">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="77402-117">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="77402-118">API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="77402-118">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="77402-119">Print ticket API</span><span class="sxs-lookup"><span data-stu-id="77402-119">Print Ticket API</span></span>](print-ticket-api.md)
</dt> <dt>

[<span data-ttu-id="77402-120">API de impresión GDI</span><span class="sxs-lookup"><span data-stu-id="77402-120">GDI Print API</span></span>](gdi-printing.md)
</dt> </dl>

 

 
