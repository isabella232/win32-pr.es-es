---
description: Los terceros pueden crear aplicaciones que consultan los datos en el índice mediante programación y pueden extender la búsqueda de Windows para indizar los datos de los formatos de archivo y los almacenes de datos personalizados.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Guía del desarrollador de Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497086"
---
# <a name="windows-search-developers-guide"></a><span data-ttu-id="3971a-103">Guía del desarrollador de Windows Search</span><span class="sxs-lookup"><span data-stu-id="3971a-103">Windows Search Developer's Guide</span></span>

<span data-ttu-id="3971a-104">Los terceros pueden crear aplicaciones que consultan los datos en el índice mediante programación y pueden extender la búsqueda de Windows para indizar los datos de los formatos de archivo y los almacenes de datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="3971a-104">Third parties can create applications that query the index for data programmatically and can extend Windows Search to index data from custom file formats and data stores.</span></span> <span data-ttu-id="3971a-105">Para crear aplicaciones de Windows Search, los desarrolladores de terceros deben implementar primero un almacén de datos de Shell para lograr una experiencia de usuario razonable.</span><span class="sxs-lookup"><span data-stu-id="3971a-105">To create Windows Search applications, third-party developers must first implement a Shell data store to a achieve a reasonable user experience.</span></span> <span data-ttu-id="3971a-106">Para obtener más información, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3971a-106">For more information, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="3971a-107">También debe descargar el [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) de las bibliotecas de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="3971a-107">You must also download the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for the Windows Search libraries.</span></span> <span data-ttu-id="3971a-108">Los [ejemplos del SDK de Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contienen ejemplos de código útiles y un ensamblado de interoperabilidad para desarrollar con código administrado.</span><span class="sxs-lookup"><span data-stu-id="3971a-108">The [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contains useful code samples and an interopability assembly for developing with managed code.</span></span> <span data-ttu-id="3971a-109">Para obtener más información sobre el uso de los ejemplos de código, vea [ejemplos de código de Windows Search](-search-3x-wds-sampleentry.md).</span><span class="sxs-lookup"><span data-stu-id="3971a-109">For more information on using the code samples, see [Windows Search Code Samples](-search-3x-wds-sampleentry.md).</span></span>

<span data-ttu-id="3971a-110">Esta sección está organizada de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3971a-110">This section is organized as follows:</span></span>

- [<span data-ttu-id="3971a-111">Administración del índice</span><span class="sxs-lookup"><span data-stu-id="3971a-111">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
- [<span data-ttu-id="3971a-112">Consulta del índice mediante programación</span><span class="sxs-lookup"><span data-stu-id="3971a-112">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
- [<span data-ttu-id="3971a-113">Extender el índice</span><span class="sxs-lookup"><span data-stu-id="3971a-113">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
- [<span data-ttu-id="3971a-114">Extensión de recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="3971a-114">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a><span data-ttu-id="3971a-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3971a-115">Additional Resources</span></span>

- <span data-ttu-id="3971a-116">Para ver los paneles de mensajes de preguntas y debate admitidos por la comunidad en tecnologías de búsqueda, vea [Foro de MSDN: desarrollo de Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="3971a-116">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
- <span data-ttu-id="3971a-117">Para descargar los ejemplos de código de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="3971a-117">To download the Search Code Samples:</span></span>
  - [<span data-ttu-id="3971a-118">Ejemplos de Windows Search</span><span class="sxs-lookup"><span data-stu-id="3971a-118">Windows Search Samples</span></span>](-search-samples-ovw.md)
- <span data-ttu-id="3971a-119">Para descargar el Windows SDK:</span><span class="sxs-lookup"><span data-stu-id="3971a-119">To download the Windows SDK:</span></span>
  - <span data-ttu-id="3971a-120">Para Windows 10: [SDK de Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="3971a-120">For Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>
  - <span data-ttu-id="3971a-121">Para Windows 7: [Windows SDK para Windows 7 y .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="3971a-121">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3971a-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3971a-122">Related topics</span></span>

[<span data-ttu-id="3971a-123">Información general sobre Windows Search</span><span class="sxs-lookup"><span data-stu-id="3971a-123">Windows Search Overview</span></span>](-search-3x-wds-overview.md)

[<span data-ttu-id="3971a-124">Referencia de Windows Search</span><span class="sxs-lookup"><span data-stu-id="3971a-124">Windows Search Reference</span></span>](-search-reference-entry-page.md)

[<span data-ttu-id="3971a-125">Ejemplos de código de Windows Search</span><span class="sxs-lookup"><span data-stu-id="3971a-125">Windows Search Code Samples</span></span>](-search-samples-ovw.md)

[<span data-ttu-id="3971a-126">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="3971a-126">Federated Search in Windows</span></span>](-search-federated-search-overview.md)

[<span data-ttu-id="3971a-127">Tecnologías de búsqueda relacionadas</span><span class="sxs-lookup"><span data-stu-id="3971a-127">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)

[<span data-ttu-id="3971a-128">Glosario de búsqueda de Windows</span><span class="sxs-lookup"><span data-stu-id="3971a-128">Windows Search Glossary</span></span>](search-glossary.md)
