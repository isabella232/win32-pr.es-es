---
description: El escritor de documentos XPS de Microsoft (MXDW) es un controlador de impresión en un archivo que permite a una aplicación Windows crear archivos de documento de XML Paper Specification (XPS) en versiones de Windows a partir de Windows XP con Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Escritor de documentos XPS de Microsoft (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697691"
---
# <a name="microsoft-xps-document-writer-mxdw"></a><span data-ttu-id="0e20f-103">Escritor de documentos XPS de Microsoft (MXDW)</span><span class="sxs-lookup"><span data-stu-id="0e20f-103">Microsoft XPS Document Writer (MXDW)</span></span>

<span data-ttu-id="0e20f-104">El escritor de documentos XPS de Microsoft (MXDW) es un controlador de impresión en un archivo que permite a una aplicación Windows crear archivos de documento de XML Paper Specification (XPS) en versiones de Windows a partir de Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="0e20f-104">The Microsoft XPS Document Writer (MXDW) is a print-to-file driver that enables a Windows application to create XML Paper Specification (XPS) document files on versions of Windows starting with Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="0e20f-105">El uso de MXDW permite a una aplicación Windows guardar su contenido como un documento XPS sin cambiar el código de programa de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e20f-105">Using the MXDW makes it possible for a Windows application to save its content as an XPS document without changing any of the application's program code.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="0e20f-106">Cuándo usar</span><span class="sxs-lookup"><span data-stu-id="0e20f-106">When to Use</span></span>

<span data-ttu-id="0e20f-107">Como usuario, debería seleccionar MXDW cuando desee crear un documento XPS desde una aplicación de Windows que no tenga la opción de guardar su contenido como un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="0e20f-107">As a user, you would select the MXDW when you want to create an XPS document from a Windows application that does not have the option to save its content as an XPS document.</span></span>

<span data-ttu-id="0e20f-108">Como desarrollador de aplicaciones, recomendaría MXDW a los usuarios que quieren crear documentos XPS cuando la aplicación no ofrece la opción de guardar como un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="0e20f-108">As an application developer, you would recommend the MXDW to users who want to create XPS documents when your application does not offer the option to save as an XPS document.</span></span> <span data-ttu-id="0e20f-109">Para obtener más información sobre la especificación de papel XML y los documentos XPS, consulte [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) y [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="0e20f-109">For more information on the XML Paper Specification and XPS documents, see [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) and [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

<span data-ttu-id="0e20f-110">MXDW se instala automáticamente en Windows Vista y versiones posteriores de Windows y se puede descargar e instalar en Windows XP con SP2 y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0e20f-110">The MXDW is installed automatically on Windows Vista and later versions of Windows and can be downloaded and installed on Windows XP with SP2 and Windows Server 2003.</span></span>

## <a name="installation"></a><span data-ttu-id="0e20f-111">Instalación</span><span class="sxs-lookup"><span data-stu-id="0e20f-111">Installation</span></span>

<span data-ttu-id="0e20f-112">En Windows Vista y versiones posteriores de Windows, el MXDW se instala automáticamente cuando se instala el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0e20f-112">On Windows Vista and later versions of Windows, the MXDW is installed automatically when the operating system is installed.</span></span>

<span data-ttu-id="0e20f-113">**Windows XP con SP2 y Windows Server 2003**: Descargue e instale .net Framework 3,0 o XPS Essential Pack desde el centro de [descarga de Microsoft](https://www.microsoft.com/downloads/en/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="0e20f-113">**Windows XP with SP2 and Windows Server 2003**: Download and install either .Net Framework 3.0 or the XPS Essential Pack from the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx).</span></span>

## <a name="how-to-use"></a><span data-ttu-id="0e20f-114">Cómo se usa</span><span class="sxs-lookup"><span data-stu-id="0e20f-114">How to Use</span></span>

<span data-ttu-id="0e20f-115">Una vez instalado, MXDW aparece como una cola de impresión disponible en el cuadro de diálogo Imprimir presentado por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e20f-115">When installed, the MXDW appears as an available print queue in the Print dialog box presented by an application.</span></span> <span data-ttu-id="0e20f-116">Cuando se selecciona MXDW como impresora, se solicita al usuario el nombre de archivo que se va a crear como documento XPS que captura la salida de impresión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e20f-116">When the MXDW is selected as the printer, the user is prompted for the file name to create as the XPS Document that captures the print output of the application.</span></span>

<span data-ttu-id="0e20f-117">La siguiente imagen muestra el MXDW que se selecciona como impresora en el cuadro de diálogo de impresión común de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0e20f-117">The following image shows the MXDW being selected as the printer in the Windows Vista common print dialog box.</span></span>

![imagen del cuadro de diálogo Imprimir que muestra la selección del escritor de documentos XPS de Microsoft (mxdw)](images/choosingmxdwinvista.gif)

<span data-ttu-id="0e20f-119">Los desarrolladores de aplicaciones pueden personalizar el resultado de MXDW con los [valores de configuración de MXDW](mxdw-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0e20f-119">Application developers can customize the output of MXDW using the [MXDW configuration settings](mxdw-configuration-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e20f-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e20f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e20f-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="0e20f-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="0e20f-122">Especificaciones de XPS y descargas de licencias</span><span class="sxs-lookup"><span data-stu-id="0e20f-122">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

<span data-ttu-id="0e20f-123">[Herramienta de cumplimiento de isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e20f-123">[isXPS Conformance Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0e20f-124">Opciones de configuración de MXDW</span><span class="sxs-lookup"><span data-stu-id="0e20f-124">MXDW configuration settings</span></span>](mxdw-configuration-settings.md)
</dt> </dl>

 

 
