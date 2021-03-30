---
description: Cuando se usan las infraestructuras de gráficos del mismo nivel o de agrupación del mismo nivel, la información (registros) que empareja la publicación en un gráfico o grupo se almacena como una base de datos en cada equipo del mismo nivel.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Importación y exportación de bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48fc09259c06e6ebaf537d26c7288d0ad09c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002002"
---
# <a name="database-import-and-export"></a><span data-ttu-id="070d4-103">Importación y exportación de bases de datos</span><span class="sxs-lookup"><span data-stu-id="070d4-103">Database Import and Export</span></span>

<span data-ttu-id="070d4-104">Cuando se usan las infraestructuras de gráficos del mismo nivel o de agrupación del mismo nivel, la información (registros) que empareja la publicación en un gráfico o grupo se almacena como una base de datos en cada equipo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="070d4-104">When using the Peer Graphing or the Peer Grouping Infrastructures, the information (records) that peers publish to a graph or group is stored as a database on each peer computer.</span></span> <span data-ttu-id="070d4-105">Para migrar una aplicación de un equipo a otro, puede exportar una base de datos del mismo nivel o de agrupación del mismo nivel desde un equipo y, a continuación, importarla a otro.</span><span class="sxs-lookup"><span data-stu-id="070d4-105">To migrate an application from one computer to another computer, you can export a Peer Graphing or Peer Grouping database from one computer, and then import it to another.</span></span>

<span data-ttu-id="070d4-106">La lista siguiente identifica información importante sobre cómo trabajar con bases de datos de:</span><span class="sxs-lookup"><span data-stu-id="070d4-106">The following list identifies important information about working with databases:</span></span>

-   <span data-ttu-id="070d4-107">Solo puede importar una base de datos que tenga el mismo gráfico y el mismo identificador del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="070d4-107">You can only import a database that has the same graph and peer ID.</span></span>
-   <span data-ttu-id="070d4-108">No se puede llamar a las funciones de importación y exportación si se ha llamado a [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)o [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) .</span><span class="sxs-lookup"><span data-stu-id="070d4-108">You cannot call the import and export functions if [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), or [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) have been called.</span></span>

<span data-ttu-id="070d4-109">La **infraestructura de gráficos del mismo nivel** usa las siguientes llamadas para importar y exportar una base de datos de registros:</span><span class="sxs-lookup"><span data-stu-id="070d4-109">**Peer Graphing Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="070d4-110">**PeerGraphExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="070d4-110">**PeerGraphExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [<span data-ttu-id="070d4-111">**PeerGraphImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="070d4-111">**PeerGraphImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

<span data-ttu-id="070d4-112">La **infraestructura de agrupación del mismo nivel** usa las siguientes llamadas para importar y exportar una base de datos de registros:</span><span class="sxs-lookup"><span data-stu-id="070d4-112">**Peer Grouping Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="070d4-113">**PeerGroupExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="070d4-113">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [<span data-ttu-id="070d4-114">**PeerGroupImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="070d4-114">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



