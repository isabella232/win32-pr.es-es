---
description: En esta sección se describen las tecnologías de documentos compatibles con Microsoft Windows.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: Documentos XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625c2f04a43db9433fe125b52a4bbc08e37fb4f4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119990"
---
# <a name="xps-documents"></a><span data-ttu-id="e73d0-103">Documentos XPS</span><span class="sxs-lookup"><span data-stu-id="e73d0-103">XPS Documents</span></span>

<span data-ttu-id="e73d0-104">En esta sección se describen las tecnologías de documentos compatibles con Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e73d0-104">This section describes the document technologies that are supported by Microsoft Windows.</span></span>

-   [<span data-ttu-id="e73d0-105">Elección de una tecnología de documentos</span><span class="sxs-lookup"><span data-stu-id="e73d0-105">Choosing a Document Technology</span></span>](#choosing-a-document-technology)
-   [<span data-ttu-id="e73d0-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e73d0-106">In This Section</span></span>](#in-this-section)
-   [<span data-ttu-id="e73d0-107">Herramientas de documento XPS</span><span class="sxs-lookup"><span data-stu-id="e73d0-107">XPS Document Tools</span></span>](#xps-document-tools)
-   [<span data-ttu-id="e73d0-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e73d0-108">Related topics</span></span>](#related-topics)


## <a name="choosing-a-document-technology"></a><span data-ttu-id="e73d0-109">Elección de una tecnología de documentos</span><span class="sxs-lookup"><span data-stu-id="e73d0-109">Choosing a Document Technology</span></span>

<span data-ttu-id="e73d0-110">Microsoft proporciona varias tecnologías de documentos diferentes para admitir una variedad de aplicaciones de documentos:</span><span class="sxs-lookup"><span data-stu-id="e73d0-110">Microsoft provides several different document technologies to support a variety of document applications:</span></span>

-   <span data-ttu-id="e73d0-111">**XPS y OpenXPS**</span><span class="sxs-lookup"><span data-stu-id="e73d0-111">**XPS and OpenXPS**</span></span>

    <span data-ttu-id="e73d0-112">XPS y OpenXPS se admiten en Windows 8 versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="e73d0-112">XPS and OpenXPS are supported in Windows 8 and later versions of Windows.</span></span> <span data-ttu-id="e73d0-113">Consulte el diagrama anterior para determinar el escenario de uso correcto para XPS y OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="e73d0-113">See the preceding diagram to determine the correct usage scenario for XPS and OpenXPS.</span></span> <span data-ttu-id="e73d0-114">Para obtener más información sobre estas tecnologías de documentos, vea [Open XML Paper Specification (OpenXPS).](https://www.ecma-international.org/publications/standards/Ecma-388.htm)</span><span class="sxs-lookup"><span data-stu-id="e73d0-114">For more information about these document technologies, see [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span></span>

    <span data-ttu-id="e73d0-115">En el caso de usar OpenXPS con Windows 8 y Windows Server 2012, la compatibilidad solo se proporciona a través de [la API de documentos XPS.](documents-xps.md)</span><span class="sxs-lookup"><span data-stu-id="e73d0-115">In the case of using OpenXPS with Windows 8 and Windows Server 2012, support is only provided via the [XPS Document API](documents-xps.md)</span></span>

    <span data-ttu-id="e73d0-116">Si necesita convertir entre Microsoft XPS (MSXPS) y OpenXPS, Microsoft ha proporcionado una herramienta (XPSConverter.exe) que le permite convertir documentos con formato MSXPS al formato OpenXPS y viceversa.</span><span class="sxs-lookup"><span data-stu-id="e73d0-116">If you need to convert between Microsoft XPS (MSXPS) and OpenXPS, then Microsoft has provided a tool (XPSConverter.exe) that allows you to convert MSXPS-formatted documents to the OpenXPS format and vice versa.</span></span> <span data-ttu-id="e73d0-117">La herramienta forma parte de la Kit para controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="e73d0-117">The tool is part of the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="e73d0-118">Para descargar wdk, consulte [Cómo obtener la WDK](/windows-hardware/drivers/download-the-wdk).</span><span class="sxs-lookup"><span data-stu-id="e73d0-118">To download the WDK, see [How to get the WDK](/windows-hardware/drivers/download-the-wdk).</span></span>

    <span data-ttu-id="e73d0-119">Y para obtener más información sobre OpenXPS y Windows 8, vea [Compatibilidad con OpenXPS en Windows.](/windows-hardware/drivers/print/driver-support-for-openxps)</span><span class="sxs-lookup"><span data-stu-id="e73d0-119">And for more information about OpenXPS and Windows 8, see [OpenXPS Support in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span></span>

-   <span data-ttu-id="e73d0-120">**XPS Document API**</span><span class="sxs-lookup"><span data-stu-id="e73d0-120">**XPS Document API**</span></span>

    <span data-ttu-id="e73d0-121">XpS Document API es una API nativa de Windows que admite XPS OM.</span><span class="sxs-lookup"><span data-stu-id="e73d0-121">The XPS Document API is a native Windows API that supports the XPS OM.</span></span> <span data-ttu-id="e73d0-122">La API de documentos XPS se introdujo en Windows 7 y se puede usar en programas en modo de usuario y controladores de impresora XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="e73d0-122">The XPS Document API was introduced in Windows 7 and can be used in user-mode programs and XPSDrv printer drivers.</span></span>

    <span data-ttu-id="e73d0-123">Para obtener más información, vea XPS Document API y [XPS Digital Signature API](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="e73d0-123">For more information, see the XPS Document API, and [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

    <span data-ttu-id="e73d0-124">\*La API de documentos XPS también se admite en Windows Vista con Service Pack 2 (SP2) con la actualización de plataforma para Windows Vista y Windows Server 2008 con SP2 mediante la actualización de plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e73d0-124">\*The XPS Document API is also supported in Windows Vista with Service Pack 2 (SP2) with the Platform Update for Windows Vista and Windows Server 2008 with SP2 using the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="e73d0-125">Para obtener más información sobre la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008, vea Actualización de [plataforma para Windows Vista.](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span><span class="sxs-lookup"><span data-stu-id="e73d0-125">For more information about the Platform Update for Windows Vista or the Platform Update for Windows Server 2008, see [Platform Update for Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span></span>

-   <span data-ttu-id="e73d0-126">**.NET Framework**</span><span class="sxs-lookup"><span data-stu-id="e73d0-126">**.NET Framework**</span></span>

    <span data-ttu-id="e73d0-127">.NET Framework proporciona compatibilidad con documentos XPS para programas de código administrado en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="e73d0-127">.NET Framework provides XPS document support to user-mode, managed-code programs.</span></span>

    <span data-ttu-id="e73d0-128">.NET Framework 3.0 se admite en Windows XP con Service Pack 2 (SP2) y versiones posteriores de sistemas operativos cliente de Windows, y en Windows Server 2003 con Service Pack 2 (SP2) y versiones posteriores de sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e73d0-128">.NET Framework 3.0 is supported on Windows XP with Service Pack 2 (SP2) and later versions of Windows client operating systems, and on Windows Server 2003 with Service Pack 2 (SP2) and later versions of Windows server operating systems.</span></span>

    <span data-ttu-id="e73d0-129">.NET Framework 3.5 se admite en las versiones de Windows XP de los sistemas operativos cliente de Windows y en Windows Server 2003 y versiones posteriores de los sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e73d0-129">.NET Framework 3.5 is supported on Windows XP versions of Windows client operating systems, and on Windows Server 2003 and later versions of Windows server operating systems.</span></span>

    > [!Note]  
    > <span data-ttu-id="e73d0-130">Se recomienda el uso de .NET Framework para crear documentos XPS solo en aplicaciones cliente, no en aplicaciones de servidor a menos que la aplicación se cierre periódicamente, como lo haría si fuera una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="e73d0-130">We recommend the use of .NET Framework for creating XPS documents in client applications only, not in server applications unless the application exits periodically, as it would if it were a client application.</span></span>

     

    <span data-ttu-id="e73d0-131">Para obtener más información sobre la compatibilidad con documentos .NET Framework, [vea Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e73d0-131">For more information about document support in .NET Framework, see [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="e73d0-132">Para trabajar con documentos XPS en un programa, use la API de documentos XPS nativa o el .NET Framework; No se admite el uso simultáneo de ambos en el mismo programa.</span><span class="sxs-lookup"><span data-stu-id="e73d0-132">To work with XPS documents in a program, use either the native XPS Document API or the .NET Framework; simultaneous use of both in the same program is not supported.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="e73d0-133">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e73d0-133">In This Section</span></span>

<span data-ttu-id="e73d0-134">En esta sección se describen las tecnologías nativas de documentos de Windows compatibles con Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e73d0-134">This section describes the native Windows document technologies that are supported by Microsoft Windows.</span></span>



| <span data-ttu-id="e73d0-135">Tecnología de documentos</span><span class="sxs-lookup"><span data-stu-id="e73d0-135">Document technology</span></span>                                                                   | <span data-ttu-id="e73d0-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="e73d0-136">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e73d0-137">XPS Document API</span><span class="sxs-lookup"><span data-stu-id="e73d0-137">XPS Document API</span></span>](documents-xps.md)<br/>                   | <span data-ttu-id="e73d0-138">Proporciona un formato de confianza para el papel electrónico.</span><span class="sxs-lookup"><span data-stu-id="e73d0-138">Provides a trustworthy format for electronic paper.</span></span><br/> <span data-ttu-id="e73d0-139">La API de documentos XPS que se describe en esta sección proporciona a los programas y controladores de impresión XPSDrv acceso al contenido y los metadatos de un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="e73d0-139">The XPS Document API that is described in this section gives programs and XPSDrv print drivers access to the content and metadata of an XPS document.</span></span><br/> |
| [<span data-ttu-id="e73d0-140">XPS Digital Signature API</span><span class="sxs-lookup"><span data-stu-id="e73d0-140">XPS Digital Signature API</span></span>](xps-digital-signatures.md)<br/> | <span data-ttu-id="e73d0-141">Habilita la firma de documentos, la comprobación de la identidad del firmante y la indicación de si un documento XPS ha cambiado desde que se firmó.</span><span class="sxs-lookup"><span data-stu-id="e73d0-141">Enables document signing, verification of the signer's identity, and indication of whether an XPS document has changed since it was signed.</span></span><br/>                                                                          |
| [<span data-ttu-id="e73d0-142">Glosario de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="e73d0-142">XPS Documents Glossary</span></span>](xpsapi-glossary.md)<br/>           | <span data-ttu-id="e73d0-143">Definiciones de términos usados por [la API de documentos XPS](documents-xps.md) y la API de firma digital [XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="e73d0-143">Definitions of terms used by the [XPS Document API](documents-xps.md) and the [XPS Digital Signature API](xps-digital-signatures.md).</span></span><br/>                                                                              |



 

## <a name="xps-document-tools"></a><span data-ttu-id="e73d0-144">Herramientas de documento XPS</span><span class="sxs-lookup"><span data-stu-id="e73d0-144">XPS Document Tools</span></span>

<span data-ttu-id="e73d0-145">Las siguientes herramientas están disponibles para ayudarle a probar y solucionar problemas de archivos de documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="e73d0-145">The following tools are available to assist you with testing and troubleshooting of XPS document files.</span></span>

-   <span data-ttu-id="e73d0-146">[IsXPS](/previous-versions/aa348104(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="e73d0-146">[IsXPS](/previous-versions/aa348104(v=vs.110))</span></span>

    <span data-ttu-id="e73d0-147">Comprueba la conformidad de un archivo con el XML Paper Specification (XPS) y la especificación Convenciones de empaquetado abierto (OPC).</span><span class="sxs-lookup"><span data-stu-id="e73d0-147">Tests a file's conformity to the XML Paper Specification (XPS) and the Open Packaging Conventions (OPC) Specification.</span></span>

-   [<span data-ttu-id="e73d0-148">XpsAnalyzer</span><span class="sxs-lookup"><span data-stu-id="e73d0-148">XpsAnalyzer</span></span>](/windows-hardware/drivers/devtest/xpsanalyzer)

    <span data-ttu-id="e73d0-149">Herramienta del símbolo del sistema que analiza los archivos de documentos XPS para la compatibilidad con la especificación XPS 1.0.</span><span class="sxs-lookup"><span data-stu-id="e73d0-149">A command-prompt tool that analyzes XPS document files for compatibility with the XPS 1.0 specification.</span></span>

-   <span data-ttu-id="e73d0-150">[PTConform](/previous-versions/dd327476(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e73d0-150">[PTConform](/previous-versions/dd327476(v=msdn.10))</span></span>

    <span data-ttu-id="e73d0-151">Herramienta que comprueba la validez de los documentos PrintTicket e PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="e73d0-151">A tool that checks the validity of PrintTicket and PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e73d0-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e73d0-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e73d0-153">XPS Print API</span><span class="sxs-lookup"><span data-stu-id="e73d0-153">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[<span data-ttu-id="e73d0-154">Packaging</span><span class="sxs-lookup"><span data-stu-id="e73d0-154">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="e73d0-155">Impresión</span><span class="sxs-lookup"><span data-stu-id="e73d0-155">Printing</span></span>](./printdocs-printing.md)
</dt> <dt>
  
<span data-ttu-id="e73d0-156">[Programa de ejemplo de impresión](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="e73d0-156">[Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span></span>
</dt> </dl>

 

