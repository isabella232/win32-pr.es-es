---
description: La API de impresión de GDI proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API de impresión GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276780"
---
# <a name="gdi-print-api"></a><span data-ttu-id="74a84-103">API de impresión GDI</span><span class="sxs-lookup"><span data-stu-id="74a84-103">GDI Print API</span></span>

<span data-ttu-id="74a84-104">La API de impresión de GDI proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74a84-104">The GDI Print API provides applications with a device-independent printing interface.</span></span> <span data-ttu-id="74a84-105">Use esta interfaz si la aplicación usa GDI para representar texto y gráficos.</span><span class="sxs-lookup"><span data-stu-id="74a84-105">Use this interface if the application uses GDI to render text and graphics.</span></span>

<span data-ttu-id="74a84-106">Si escribe aplicaciones para Windows Vista o versiones posteriores de Windows, considere la posibilidad de usar la [API de documentos XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) y la [API de impresión XPS](xps-printing.md) para usar las interfaces de gráficos de mayor rendimiento admitidas por los controladores de impresión XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="74a84-106">If you write applications for Windows Vista or later versions of Windows, consider using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and the [XPS Print API](xps-printing.md) to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span>

<span data-ttu-id="74a84-107">En esta sección se proporciona información sobre los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="74a84-107">This section provides information about the following topics.</span></span>



| <span data-ttu-id="74a84-108">Tema</span><span class="sxs-lookup"><span data-stu-id="74a84-108">Topic</span></span>                                                                                             | <span data-ttu-id="74a84-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="74a84-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74a84-110">Acerca de la API de impresión GDI</span><span class="sxs-lookup"><span data-stu-id="74a84-110">About the GDI Print API</span></span>](about-the-gdi-print-api.md)<br/>                                 | <span data-ttu-id="74a84-111">Información general sobre la funcionalidad de impresión de GDI.</span><span class="sxs-lookup"><span data-stu-id="74a84-111">An overview of the GDI printing functionality.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="74a84-112">Uso de la API de impresión de GDI</span><span class="sxs-lookup"><span data-stu-id="74a84-112">Using the GDI Print API</span></span>](using-the-printing-functions.md)<br/>                            | <span data-ttu-id="74a84-113">Información sobre el uso de la API de impresión de GDI en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="74a84-113">Information about using the GDI Print API in an application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="74a84-114">Referencia de la API de impresión de GDI</span><span class="sxs-lookup"><span data-stu-id="74a84-114">GDI Print API Reference</span></span>](gdi-print-api-reference.md)<br/>                                 | <span data-ttu-id="74a84-115">Descripciones detalladas de las funciones, estructuras y otros elementos de la API de impresión de GDI.</span><span class="sxs-lookup"><span data-stu-id="74a84-115">Detailed descriptions of the functions, structures, and other elements of the GDI Print API.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="74a84-116">Convertidor de documentos XPS de Microsoft (MXDC)</span><span class="sxs-lookup"><span data-stu-id="74a84-116">Microsoft XPS Document Converter (MXDC)</span></span>](microsoft-xps-document-converter--mxdc-.md)<br/> | <span data-ttu-id="74a84-117">El [convertidor de documentos XPS de Microsoft (MXDC)](microsoft-xps-document-converter--mxdc-.md) es un componente que permite a las aplicaciones usar la API de impresión de GDI con impresoras que tienen un controlador de impresión XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="74a84-117">The [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) is a component that enables applications to use the GDI Print API with printers that have an XPSDrv Print Driver.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="74a84-118">Escritor de documentos XPS de Microsoft (MXDW)</span><span class="sxs-lookup"><span data-stu-id="74a84-118">Microsoft XPS Document Writer (MXDW)</span></span>](microsoft-xps-document-writer.md)<br/>              | <span data-ttu-id="74a84-119">El [escritor de documentos XPS de Microsoft (MXDW)](microsoft-xps-document-writer.md) proporciona a las aplicaciones la funcionalidad "guardar como XPS" o "exportar a XPS".</span><span class="sxs-lookup"><span data-stu-id="74a84-119">The [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) provides applications with "save as XPS" or "export to XPS" functionality.</span></span> <span data-ttu-id="74a84-120">Las aplicaciones que no crean de forma nativa el contenido de un documento XPS pueden usar MXDW para crear archivos de documento XPS sin usar la [API de documentos XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74a84-120">Applications that do not natively create XPS document content can use the MXDW to create XPS document files without using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="74a84-121">La API de documento XPS, sin embargo, proporciona una aplicación con la capacidad de usar las interfaces de gráficos de mayor rendimiento que son compatibles con los controladores de impresión XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="74a84-121">The XPS Document API, however, provides an application with the ability to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span><br/> |



 

<span data-ttu-id="74a84-122">En el diagrama siguiente se muestra la relación de la API de impresión de GDI con las otras API de impresión que puede usar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="74a84-122">The following diagram shows the relationship of the GDI Print API to the other print APIs that an application can use.</span></span>

![diagrama que muestra la relación de la API de impresión de GDI con las otras API de impresión que puede usar una aplicación Win32.](images/print-apis-gdi.png)

## <a name="related-topics"></a><span data-ttu-id="74a84-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74a84-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74a84-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="74a84-125">**AddJob**</span></span>](addjob.md)
</dt> <dt>

<span data-ttu-id="74a84-126">[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74a84-126">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="74a84-127">API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="74a84-127">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="74a84-128">API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="74a84-128">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="74a84-129">Print ticket API</span><span class="sxs-lookup"><span data-stu-id="74a84-129">Print Ticket API</span></span>](print-ticket-api.md)
</dt> </dl>

 

