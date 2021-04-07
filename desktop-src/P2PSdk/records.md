---
description: Los registros son una manera de comunicarse entre los nodos de un gráfico o los miembros de un grupo.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002476"
---
# <a name="records"></a><span data-ttu-id="52ee0-103">Registros</span><span class="sxs-lookup"><span data-stu-id="52ee0-103">Records</span></span>

<span data-ttu-id="52ee0-104">Los registros son una manera de comunicarse entre los nodos de un gráfico o los miembros de un grupo.</span><span class="sxs-lookup"><span data-stu-id="52ee0-104">Records are a way to communicate between nodes in a graph or members in a group.</span></span> <span data-ttu-id="52ee0-105">Un registro consta de las dos partes siguientes:</span><span class="sxs-lookup"><span data-stu-id="52ee0-105">A record consists of the following two parts:</span></span>

-   <span data-ttu-id="52ee0-106">Encabezado de registro</span><span class="sxs-lookup"><span data-stu-id="52ee0-106">Record header</span></span>
-   <span data-ttu-id="52ee0-107">Contenido de datos opacos específico</span><span class="sxs-lookup"><span data-stu-id="52ee0-107">Specific opaque data content</span></span>

<span data-ttu-id="52ee0-108">El encabezado contiene información sobre el registro, incluida la versión, el creador y el tipo de datos que se publican.</span><span class="sxs-lookup"><span data-stu-id="52ee0-108">The header contains information about the record, including the version, creator, and type of data being published.</span></span> <span data-ttu-id="52ee0-109">El encabezado también contiene un campo de atributos XML que permite a las aplicaciones agregar atributos de nombre y valor que describen los datos, y buscar de forma eficaz en la base de datos de registros los registros específicos que se han publicado previamente.</span><span class="sxs-lookup"><span data-stu-id="52ee0-109">The header also contains an XML attributes field that allows applications to add name-value attributes that describe the data, and to efficiently search the record database for specific records that have previously been published.</span></span> <span data-ttu-id="52ee0-110">El contenido son los datos definidos por la aplicación y es opaco para la infraestructura del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="52ee0-110">The content is the application-defined data, and is opaque to the Peer Infrastructure.</span></span>

<span data-ttu-id="52ee0-111">Cuando se publica un registro, se inunda (tanto el encabezado como los datos) en el gráfico o el grupo.</span><span class="sxs-lookup"><span data-stu-id="52ee0-111">When a record is published, it (both header and data) is flooded throughout the graph or group.</span></span> <span data-ttu-id="52ee0-112">Los pares sincronizados reciben estos datos y los almacenan en una base de datos local.</span><span class="sxs-lookup"><span data-stu-id="52ee0-112">Synchronized peers receive this data and store it in a local database.</span></span> <span data-ttu-id="52ee0-113">Los pares no sincronizados y sin conexión reciben los datos la próxima vez que se conectan y se sincronizan con el grafo o el grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="52ee0-113">Unsynchronized and offline peers receive the data the next time they connect and synchronize with the peer graph or group.</span></span>

<span data-ttu-id="52ee0-114">Para obtener información sobre cómo trabajar con registros, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="52ee0-114">For information about working with records, see the following topics:</span></span>

-   [<span data-ttu-id="52ee0-115">Dependencias de registro</span><span class="sxs-lookup"><span data-stu-id="52ee0-115">Record Dependencies</span></span>](record-dependencies.md)
-   [<span data-ttu-id="52ee0-116">Administración de registros</span><span class="sxs-lookup"><span data-stu-id="52ee0-116">Record Management</span></span>](record-management.md)
-   [<span data-ttu-id="52ee0-117">Esquema de atributo de registro</span><span class="sxs-lookup"><span data-stu-id="52ee0-117">Record Attribute Schema</span></span>](record-attribute-schema.md)
-   [<span data-ttu-id="52ee0-118">Formato de consulta de búsqueda de registros</span><span class="sxs-lookup"><span data-stu-id="52ee0-118">Record Search Query Format</span></span>](record-search-query-format.md)

 

 



