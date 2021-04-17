---
description: Hay varias maneras de usar Windows Search para consultar el índice.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Consulta del índice mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659791"
---
# <a name="querying-the-index-programmatically"></a><span data-ttu-id="e21d0-103">Consulta del índice mediante programación</span><span class="sxs-lookup"><span data-stu-id="e21d0-103">Querying the Index Programmatically</span></span>

<span data-ttu-id="e21d0-104">Hay varias maneras de usar Windows Search para consultar el índice.</span><span class="sxs-lookup"><span data-stu-id="e21d0-104">There are several ways to use Windows Search to query the index.</span></span>

<span data-ttu-id="e21d0-105">En esta sección se proporciona el marco conceptual para consultar el índice mediante programación:</span><span class="sxs-lookup"><span data-stu-id="e21d0-105">This section provides the conceptual framework for querying the index programmatically:</span></span>

-   [<span data-ttu-id="e21d0-106">Uso de enfoques de SQL y AQS para consultar el índice</span><span class="sxs-lookup"><span data-stu-id="e21d0-106">Using SQL and AQS Approaches to Query the Index</span></span>](using-sql-and-aqs-to-query-the-index.md)
-   [<span data-ttu-id="e21d0-107">Consultar el índice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="e21d0-107">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [<span data-ttu-id="e21d0-108">Consultar el índice con el protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="e21d0-108">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
-   [<span data-ttu-id="e21d0-109">Consultar el índice con la sintaxis SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="e21d0-109">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
-   [<span data-ttu-id="e21d0-110">Usar la sintaxis de consulta avanzada mediante programación</span><span class="sxs-lookup"><span data-stu-id="e21d0-110">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)

> [!Note]  
> <span data-ttu-id="e21d0-111">Compatibilidad de Microsoft Windows Desktop Search (WDS) 2x heredada: en equipos que ejecutan Windows XP y versiones posteriores, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) está en desuso.</span><span class="sxs-lookup"><span data-stu-id="e21d0-111">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="e21d0-112">En su lugar, los desarrolladores deben usar [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) para obtener una cadena de conexión y analizar la consulta del usuario en lenguaje de consulta estructurado (SQL) y, a continuación, consultar la vinculación de objetos y la base de datos de incrustación (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="e21d0-112">Instead, developers should use [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string and to parse the user's query into Structured Query Language (SQL), and then query through Object Linking and Embedding Database (OLE DB).</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="e21d0-113">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e21d0-113">Additional Resources</span></span>

-   <span data-ttu-id="e21d0-114">Para obtener información sobre OLE DB, consulte [información general sobre la programación de OLE DB](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="e21d0-114">For information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx).</span></span> <span data-ttu-id="e21d0-115">Para obtener información sobre el proveedor de datos de .NET Framework para OLE DB, vea el [espacio de nombres System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).</span><span class="sxs-lookup"><span data-stu-id="e21d0-115">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).</span></span>
-   <span data-ttu-id="e21d0-116">Para obtener información adicional sobre el uso de propiedades en la consulta, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e21d0-116">For additional background on using properties in querying, see the following topics:</span></span>
    -   [<span data-ttu-id="e21d0-117">Sistema de propiedades</span><span class="sxs-lookup"><span data-stu-id="e21d0-117">Property System</span></span>](../properties/building-property-handlers.md)
    -   <span data-ttu-id="e21d0-118">[Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e21d0-118">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
-   <span data-ttu-id="e21d0-119">Para obtener información sobre cómo crear y modificar carpetas de búsqueda, vea [**ISearchFolderItemFactory (interfaz**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory)).</span><span class="sxs-lookup"><span data-stu-id="e21d0-119">For information on how to create and modify search folders, see [**ISearchFolderItemFactory Interface**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).</span></span>
-   <span data-ttu-id="e21d0-120">Para ver los paneles de mensajes de preguntas y debate admitidos por la comunidad en tecnologías de búsqueda, vea [Foro de MSDN: desarrollo de Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="e21d0-120">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
-   <span data-ttu-id="e21d0-121">Para descargar los ejemplos de código del SDK de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="e21d0-121">To download the Search SDK Code Samples:</span></span>
    -   <span data-ttu-id="e21d0-122">Para Windows 7: [ejemplos de Windows Search en github](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)</span><span class="sxs-lookup"><span data-stu-id="e21d0-122">For Windows 7: [Windows Search Samples on GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)</span></span>
    -   <span data-ttu-id="e21d0-123">Para Windows Vista: [ejemplos del SDK de Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)</span><span class="sxs-lookup"><span data-stu-id="e21d0-123">For Windows Vista: [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)</span></span>
-   <span data-ttu-id="e21d0-124">Para descargar el Windows SDK:</span><span class="sxs-lookup"><span data-stu-id="e21d0-124">To download the Windows SDK:</span></span>
    -   <span data-ttu-id="e21d0-125">Para Windows 7: [Windows SDK para Windows 7 y .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="e21d0-125">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>
    -   <span data-ttu-id="e21d0-126">En Windows Vista: [Windows SDK para Windows Vista y .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span><span class="sxs-lookup"><span data-stu-id="e21d0-126">For Windows Vista: [Windows SDK for Windows Vista and .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e21d0-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e21d0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e21d0-128">Guía de desarrollo de Windows Search</span><span class="sxs-lookup"><span data-stu-id="e21d0-128">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="e21d0-129">Administración del índice</span><span class="sxs-lookup"><span data-stu-id="e21d0-129">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="e21d0-130">Extender el índice de búsqueda de Windows</span><span class="sxs-lookup"><span data-stu-id="e21d0-130">Extending the Windows Search Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[<span data-ttu-id="e21d0-131">Extensión de recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="e21d0-131">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
