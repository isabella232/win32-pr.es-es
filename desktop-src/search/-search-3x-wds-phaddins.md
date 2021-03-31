---
description: En esta sección se proporciona información conceptual necesaria para la implementación, la extensión y las pruebas de los controladores de protocolo.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: Desarrollo de controladores de protocolo para Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e56c237dd4876ae05bcd7b983c4da2708f299a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808971"
---
# <a name="developing-protocol-handlers-for-windows-search"></a><span data-ttu-id="a245f-103">Desarrollo de controladores de protocolo para Windows Search</span><span class="sxs-lookup"><span data-stu-id="a245f-103">Developing Protocol Handlers for Windows Search</span></span>

<span data-ttu-id="a245f-104">En esta sección se proporciona información conceptual necesaria para la implementación, la extensión y las pruebas de los controladores de protocolo.</span><span class="sxs-lookup"><span data-stu-id="a245f-104">This section provides conceptual information necessary for the implementation, extension and testing of protocol handlers.</span></span>

-   [<span data-ttu-id="a245f-105">Descripción de los controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="a245f-105">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
-   [<span data-ttu-id="a245f-106">Notificar el índice de cambios</span><span class="sxs-lookup"><span data-stu-id="a245f-106">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
-   [<span data-ttu-id="a245f-107">Agregar iconos y menús contextuales</span><span class="sxs-lookup"><span data-stu-id="a245f-107">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
-   [<span data-ttu-id="a245f-108">Código de ejemplo: extensiones de Shell para controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="a245f-108">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
-   [<span data-ttu-id="a245f-109">Instalar y registrar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="a245f-109">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
-   [<span data-ttu-id="a245f-110">Crear un conector de búsqueda para un controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="a245f-110">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
-   [<span data-ttu-id="a245f-111">Controladores de protocolo de depuración</span><span class="sxs-lookup"><span data-stu-id="a245f-111">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a><span data-ttu-id="a245f-112">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a245f-112">Additional Resources</span></span>

<span data-ttu-id="a245f-113">Para obtener información general conceptual sobre la indexación, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a245f-113">For conceptual background on indexing, see the following topics:</span></span>

-   <span data-ttu-id="a245f-114">Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a245f-114">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="a245f-115">Para ampliar la búsqueda de Windows para indizar el contenido y las propiedades de los nuevos formatos de archivo y almacenes de datos, vea [extender el índice](-search-3x-wds-extidx-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a245f-115">To extend Windows Search to index the contents and properties of new file formats and data stores, see [Extending the Index](-search-3x-wds-extidx-overview.md).</span></span>
-   <span data-ttu-id="a245f-116">Para obtener información general del administrador de catálogos y del administrador de búsqueda de catálogos (CSM), consulte [usar el administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md) y [el administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="a245f-116">For overviews of the Catalog Manager and Catalog Search Manager (CSM), see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

<span data-ttu-id="a245f-117">Para obtener información conceptual sobre los tipos de archivo y los controladores, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a245f-117">For conceptual background on file types and handlers, see the following topics:</span></span>

-   <span data-ttu-id="a245f-118">Para extender el shell con controladores de tipo de archivo, vea [crear controladores de extensión de Shell](../shell/handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a245f-118">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](../shell/handlers.md).</span></span>
-   <span data-ttu-id="a245f-119">Para obtener información conceptual sobre los controladores de filtro, vea [desarrollar controladores de filtro](-search-ifilter-conceptual.md).</span><span class="sxs-lookup"><span data-stu-id="a245f-119">For conceptual information on filter handlers, see [Developing Filter Handlers](-search-ifilter-conceptual.md).</span></span>
-   <span data-ttu-id="a245f-120">Para obtener información sobre la creación de controladores, vea [Introducción a las asociaciones de archivo](../shell/fa-intro.md), [registro de extensiones de Shell](../shell/reg-shell-exts.md), creación de controladores de extensión de [Shell](../shell/handlers.md), [menú contextual](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))y [controladores de vista previa](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a245f-120">For information about creating handlers, see [Introduction to File Associations](../shell/fa-intro.md), [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), and [Preview Handlers](../shell/preview-handlers.md).</span></span>

<span data-ttu-id="a245f-121">Para obtener información general sobre las tecnologías relacionadas y sobre cómo implementar un almacén de datos, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a245f-121">For background on related technologies and on implementing a data store, see the following topics:</span></span>

-   <span data-ttu-id="a245f-122">Los controladores de protocolo de Windows Search usan especificaciones de diseño similares a las de SharePoint Server y, a menudo, se pueden usar indistintamente.</span><span class="sxs-lookup"><span data-stu-id="a245f-122">Windows Search protocol handlers use design specifications similar to SharePoint Server, and they can often be used interchangeably.</span></span> <span data-ttu-id="a245f-123">Para obtener más información, vea [Centro para desarrolladores de SharePoint Server](https://developer.microsoft.com/office/docs).</span><span class="sxs-lookup"><span data-stu-id="a245f-123">For more information, see [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs).</span></span>
-   <span data-ttu-id="a245f-124">En Windows 7 y versiones posteriores, el servidor de búsqueda de SharePoint 2008 y MOSS 2007 SP2 también admiten la búsqueda federada.</span><span class="sxs-lookup"><span data-stu-id="a245f-124">In Windows 7 and later, SharePoint Search Server 2008 and MOSS 2007 SP2 also support federated search.</span></span> <span data-ttu-id="a245f-125">Para obtener más información sobre la implementación de la búsqueda federada y el servidor de Search 2008 con Office SharePoint Server 2007, vea servidor de búsqueda de búsqueda [federada \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)).</span><span class="sxs-lookup"><span data-stu-id="a245f-125">For more information about federated search and Search Server 2008 deployment with Office SharePoint Server 2007, see [Federated Search \[Search Server 2008\]](/previous-versions/office/bb931109(v=office.14)).</span></span>
-   <span data-ttu-id="a245f-126">Para crear un almacén de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a245f-126">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="a245f-127">Para obtener ejemplos de código, vea las siguientes páginas del portal:</span><span class="sxs-lookup"><span data-stu-id="a245f-127">For code samples, see the following portal pages:</span></span>

-   <span data-ttu-id="a245f-128">Para ver ejemplos de código de búsqueda, consulte [ejemplos del SDK de Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="a245f-128">For Search code samples, see [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>
-   <span data-ttu-id="a245f-129">Para ver ejemplos de código de Shell, consulte [ejemplos del SDK de Shell](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a245f-129">For Shell code samples, see [Shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span></span>

 

 
