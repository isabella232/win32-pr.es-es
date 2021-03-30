---
description: La API del administrador de trabajos de impresión proporciona una interfaz al administrador de trabajos de impresión para que las aplicaciones administren impresoras y trabajos de impresión.
ms.assetid: b6cc0c9d-9f28-4e80-b847-39c72d98bed6
title: API del administrador de trabajos de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7287b9da3ac19d2ab9c39152d5917960e465e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083022"
---
# <a name="print-spooler-api"></a><span data-ttu-id="479dd-103">API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="479dd-103">Print Spooler API</span></span>

<span data-ttu-id="479dd-104">La API del administrador de trabajos de impresión proporciona una interfaz al administrador de trabajos de impresión para que las aplicaciones administren impresoras y trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="479dd-104">The Print Spooler API provides an interface to the print spooler for applications to manage printers and print jobs.</span></span>

<span data-ttu-id="479dd-105">Una aplicación utiliza la API del administrador de trabajos de impresión como parte de su programación y no directamente por los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="479dd-105">The Print Spooler API is used by an application as part of its programming and not directly by end users.</span></span>

<span data-ttu-id="479dd-106">Esta sección contiene información acerca de los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="479dd-106">This section contains information about the following topics.</span></span>



| <span data-ttu-id="479dd-107">Tema</span><span class="sxs-lookup"><span data-stu-id="479dd-107">Topic</span></span>                                                                                             | <span data-ttu-id="479dd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="479dd-108">Description</span></span>                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="479dd-109">Referencia de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="479dd-109">Print Spooler API Reference</span></span>](printing-and-print-spooler-reference.md)<br/>                | <span data-ttu-id="479dd-110">Información detallada sobre las funciones, estructuras y otros elementos de la API del administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="479dd-110">Detailed information about the functions, structures, and other elements of the Print Spooler API.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="479dd-111">Referencia de notificación de impresión asincrónica</span><span class="sxs-lookup"><span data-stu-id="479dd-111">Asynchronous Printing Notification Reference</span></span>](asynchronous-printing-notification.md)<br/> | <span data-ttu-id="479dd-112">Descripciones de las funciones, interfaces y enumeraciones que se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes hospedados en la cola de impresión, como controladores de impresora y monitores de puerto.</span><span class="sxs-lookup"><span data-stu-id="479dd-112">Descriptions of the functions, interfaces, and enumerations that are used in asynchronous communication between applications and print-spooler-hosted components, such as printer drivers and port monitors.</span></span><br/> |
| [<span data-ttu-id="479dd-113">Referencia de instalación del controlador de impresora</span><span class="sxs-lookup"><span data-stu-id="479dd-113">Printer Driver Installation Reference</span></span>](printer-driver-installation-reference.md)<br/>     | <span data-ttu-id="479dd-114">Describe las funciones que instalan y configuran controladores de impresora en un equipo.</span><span class="sxs-lookup"><span data-stu-id="479dd-114">Describes the functions that install and configure printer drivers on a computer.</span></span><br/>                                                                                                                            |



 

<span data-ttu-id="479dd-115">En el diagrama siguiente se muestra la relación de la API del administrador de trabajos de impresión con las otras API de impresión que puede usar una aplicación Windows nativa.</span><span class="sxs-lookup"><span data-stu-id="479dd-115">The following diagram shows the relationship of the Print Spooler API to the other Print APIs that a native Windows application can use.</span></span>

![diagrama que muestra la relación de la API del administrador de trabajos de impresión con las otras API de impresión que puede usar una aplicación Windows nativa](images/print-apis-ps.png)

## <a name="related-topics"></a><span data-ttu-id="479dd-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="479dd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="479dd-118">API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="479dd-118">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="479dd-119">Print ticket API</span><span class="sxs-lookup"><span data-stu-id="479dd-119">Print Ticket API</span></span>](print-ticket-api.md)
</dt> <dt>

[<span data-ttu-id="479dd-120">API de impresión GDI</span><span class="sxs-lookup"><span data-stu-id="479dd-120">GDI Print API</span></span>](gdi-printing.md)
</dt> </dl>

 

 




