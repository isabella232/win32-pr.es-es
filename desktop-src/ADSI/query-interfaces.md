---
title: Interfaces de consulta
description: Se pueden usar tres tipos de interfaces ADSI para realizar búsquedas en el directorio. El entorno de la aplicación y otros requisitos pueden indicar qué interfaz se utiliza.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Interfaces de consulta ADSI
- Consultas ADSI, interfaces de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903032"
---
# <a name="query-interfaces"></a><span data-ttu-id="db1eb-106">Interfaces de consulta</span><span class="sxs-lookup"><span data-stu-id="db1eb-106">Query Interfaces</span></span>

<span data-ttu-id="db1eb-107">Se pueden usar tres tipos de interfaces ADSI para realizar búsquedas en el directorio.</span><span class="sxs-lookup"><span data-stu-id="db1eb-107">Three types of ADSI interfaces can be used to perform directory searches.</span></span> <span data-ttu-id="db1eb-108">El entorno de la aplicación y otros requisitos pueden indicar qué interfaz se utiliza.</span><span class="sxs-lookup"><span data-stu-id="db1eb-108">The application environment and other requirements may indicate which interface is used.</span></span>

-   <span data-ttu-id="db1eb-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="db1eb-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="db1eb-110">**IDirectorySearch** es una interfaz com básica que solo está disponible para los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="db1eb-110">**IDirectorySearch** is a basic COM interface only available to C/C++ programmers.</span></span> <span data-ttu-id="db1eb-111">Para obtener más información, consulte [búsqueda con la interfaz IDirectorySearch](searching-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="db1eb-111">For more information, see [Searching With the IDirectorySearch Interface](searching-with-idirectorysearch.md).</span></span>
-   <span data-ttu-id="db1eb-112">ADO.</span><span class="sxs-lookup"><span data-stu-id="db1eb-112">ADO.</span></span> <span data-ttu-id="db1eb-113">Las interfaces de objetos de datos ActiveX (ADO) son interfaces de automatización que utilizan OLE DB.</span><span class="sxs-lookup"><span data-stu-id="db1eb-113">The ActiveX Data Object (ADO) interfaces are Automation interfaces that use OLE DB.</span></span> <span data-ttu-id="db1eb-114">Utilice ADO para las consultas dentro de las aplicaciones que se basan en la automatización.</span><span class="sxs-lookup"><span data-stu-id="db1eb-114">Use ADO for queries within applications that rely on Automation.</span></span> <span data-ttu-id="db1eb-115">Entre ellas se incluyen Visual Basic aplicaciones, Active Server páginas, etc.</span><span class="sxs-lookup"><span data-stu-id="db1eb-115">These include Visual Basic applications, Active Server Pages, and so on.</span></span> <span data-ttu-id="db1eb-116">Para obtener más información, vea [Buscar con objetos de datos ActiveX](searching-with-activex-data-objects-ado.md).</span><span class="sxs-lookup"><span data-stu-id="db1eb-116">For more information, see [Searching with ActiveX Data Objects](searching-with-activex-data-objects-ado.md).</span></span>
-   <span data-ttu-id="db1eb-117">OLE DB.</span><span class="sxs-lookup"><span data-stu-id="db1eb-117">OLE DB.</span></span> <span data-ttu-id="db1eb-118">OLE DB es un conjunto de interfaces de C/C++ que se usan para consultar bases de datos.</span><span class="sxs-lookup"><span data-stu-id="db1eb-118">OLE DB is a set of C/C++ interfaces used to query databases.</span></span> <span data-ttu-id="db1eb-119">Al admitir estas interfaces, los proveedores ADSI pueden implementar características avanzadas de OLE DB, como consultas distribuidas con otros proveedores de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="db1eb-119">By supporting these interfaces, ADSI providers can implement advanced OLE DB features, such as distributed queries with other OLE DB providers.</span></span> <span data-ttu-id="db1eb-120">Para obtener más información, vea [Buscar con OLE DB](searching-with-ole-db.md).</span><span class="sxs-lookup"><span data-stu-id="db1eb-120">For more information, see [Searching with OLE DB](searching-with-ole-db.md).</span></span>

 

 




