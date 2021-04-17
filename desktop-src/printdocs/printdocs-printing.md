---
description: Windows proporciona a las aplicaciones un conjunto completo de funciones que permiten la impresión en varios dispositivos, como impresoras láser, trazadores vectoriales, impresoras de tramas y equipos de fax.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Impresión (documentos e impresión)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716339"
---
# <a name="printing-documents-and-printing"></a><span data-ttu-id="480cd-103">Impresión (documentos e impresión)</span><span class="sxs-lookup"><span data-stu-id="480cd-103">Printing (Documents and Printing)</span></span>

<span data-ttu-id="480cd-104">Windows proporciona a las aplicaciones un conjunto completo de funciones que permiten la impresión en varios dispositivos, como impresoras láser, trazadores vectoriales, impresoras de tramas y equipos de fax.</span><span class="sxs-lookup"><span data-stu-id="480cd-104">Windows provides applications with a complete set of functions that allow printing to various devices, such as laser printers, vector plotters, raster printers, and fax machines.</span></span>

## <a name="desktop-app-printing"></a><span data-ttu-id="480cd-105">Impresión de aplicaciones de escritorio</span><span class="sxs-lookup"><span data-stu-id="480cd-105">Desktop App Printing</span></span>

<span data-ttu-id="480cd-106">Los programadores de Windows pueden seleccionar entre varias tecnologías diferentes para imprimir desde su aplicación.</span><span class="sxs-lookup"><span data-stu-id="480cd-106">Windows programmers can select from several different technologies to print from their application.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="480cd-107">Technology</span><span class="sxs-lookup"><span data-stu-id="480cd-107">Technology</span></span></th>
<th><span data-ttu-id="480cd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="480cd-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="480cd-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a></span><span class="sxs-lookup"><span data-stu-id="480cd-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a></span></span><br/></td>
<td><span data-ttu-id="480cd-110">Proporciona una interfaz que permite a una aplicación tener acceso al paquete de documentos de impresión y administrarlo.</span><span class="sxs-lookup"><span data-stu-id="480cd-110">Provides an interface that allows an application to access and manage the print document package.</span></span> <span data-ttu-id="480cd-111">Esta API está disponible con Windows 8 y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="480cd-111">This API is available with Windows 8 and later versions of Windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="480cd-112"><a href="print-spooler-api.md">API del administrador de trabajos de impresión</a></span><span class="sxs-lookup"><span data-stu-id="480cd-112"><a href="print-spooler-api.md">Print Spooler API</a></span></span><br/></td>
<td><span data-ttu-id="480cd-113">Proporciona una interfaz al administrador de trabajos de impresión para que las aplicaciones puedan administrar impresoras y trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="480cd-113">Provides an interface to the print spooler so that applications can manage printers and print jobs.</span></span><br/> <span data-ttu-id="480cd-114">Las aplicaciones usan la <a href="print-spooler-api.md">API del administrador de trabajos de impresión</a> para iniciar, detener, controlar y configurar los trabajos de impresión administrados por el administrador de trabajos de impresión, tanto si usan la API de impresión de paquetes de <a href="/windows/desktop/printdocs/tailored-app-printing-api">documentos</a> como la API de <a href="gdi-printing.md">impresión de GDI</a> para imprimir el contenido.</span><span class="sxs-lookup"><span data-stu-id="480cd-114">Applications use the <a href="print-spooler-api.md">Print Spooler API</a> to start, stop, control, and configure print jobs managed by the print spooler whether they use the <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a> or the <a href="gdi-printing.md">GDI Print API</a> to print the content.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="480cd-115"><a href="print-ticket-api.md">Print ticket API</a></span><span class="sxs-lookup"><span data-stu-id="480cd-115"><a href="print-ticket-api.md">Print Ticket API</a></span></span><br/></td>
<td><span data-ttu-id="480cd-116">Proporciona a las aplicaciones funciones para administrar y convertir los vales de impresión.</span><span class="sxs-lookup"><span data-stu-id="480cd-116">Provides applications with functions to manage and convert print tickets.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="480cd-117"><a href="gdi-printing.md">API de impresión GDI</a></span><span class="sxs-lookup"><span data-stu-id="480cd-117"><a href="gdi-printing.md">GDI Print API</a></span></span><br/></td>
<td><span data-ttu-id="480cd-118">Proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="480cd-118">Provides applications with a device-independent printing interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="480cd-119">Los desarrolladores que escriben aplicaciones para Windows Vista y versiones posteriores de Windows deben considerar el uso de la <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de documentos XPS</a> en su aplicación.</span><span class="sxs-lookup"><span data-stu-id="480cd-119">Developers who are writing applications for Windows Vista and later versions of Windows should consider using the <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS Document API</a> in their application.</span></span>
</blockquote>
<br/> <span data-ttu-id="480cd-120">La <a href="gdi-printing.md">API de impresión de GDI</a> es adecuada para las aplicaciones que se deben ejecutar en Windows XP y versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="480cd-120">The <a href="gdi-printing.md">GDI Print API</a> is suitable for applications that must run on Windows XP and earlier versions of Windows.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="480cd-121">En la ilustración siguiente se proporciona una vista de alto nivel de cómo se relacionan las diferentes API de impresión.</span><span class="sxs-lookup"><span data-stu-id="480cd-121">The following illustration provides a high-level view of how the different printing APIs are related.</span></span>

![un diagrama que muestra cómo una aplicación nativa de Windows puede usar las API de impresión](images/print-apis.png)

 

<span data-ttu-id="480cd-123">En la [API de impresión de paquetes de documentos](./tailored-app-printing-api.md)de esta sección se describen las interfaces de impresión de paquetes y de vista previa de impresión que se pueden usar con Windows 8 y versiones posteriores del escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="480cd-123">The [Print Document Package API](./tailored-app-printing-api.md)s in this section describe the print document package and print preview interfaces that you can use with Windows 8 and later versions of Windows desktop.</span></span>

<span data-ttu-id="480cd-124">Para obtener más información sobre la impresión desde aplicaciones de la tienda Windows escritas en JavaScript y HTML, consulta [impresión (aplicaciones de la tienda Windows con JavaScript y HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="480cd-124">For more info about printing from Windows Store apps that are written in JavaScript and HTML, see [Printing (Windows Store apps using JavaScript and HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span></span> <span data-ttu-id="480cd-125">Para obtener más información sobre la impresión desde aplicaciones de la tienda Windows escritas en C#, Microsoft Visual Basic o C++ y XAML, consulta [impresión (aplicaciones de la tienda Windows con C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="480cd-125">For more info about printing from Windows Store apps that are written in C#, Microsoft Visual Basic, or C++ and XAML, see [Printing (Windows Store apps using C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span></span>

> [!Note]  
> <span data-ttu-id="480cd-126">Vea [Win32 y com para aplicaciones de la tienda Windows (impresión y documentos)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) para ver la lista de las API de impresión de aplicaciones de escritorio que también se pueden usar en aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="480cd-126">See [Win32 and COM for Windows Store apps (printing and documents)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) for the list of the Desktop App Printing APIs that can also be used in Windows Store apps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="480cd-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="480cd-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="480cd-128">[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="480cd-128">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="480cd-129">Comunicaciones de impresora bidireccional (centro de desarrollo de hardware)</span><span class="sxs-lookup"><span data-stu-id="480cd-129">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

