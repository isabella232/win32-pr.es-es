---
title: Información general de la entrada del servicio de nombres
description: La entrada servicio de nombres consta de tres secciones distintas.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676267"
---
# <a name="an-overview-of-the-name-service-entry"></a><span data-ttu-id="06dee-103">Información general de la entrada del servicio de nombres</span><span class="sxs-lookup"><span data-stu-id="06dee-103">An Overview of the Name Service Entry</span></span>

<span data-ttu-id="06dee-104">La entrada servicio de nombres consta de tres secciones distintas.</span><span class="sxs-lookup"><span data-stu-id="06dee-104">The name service entry consists of three distinct sections.</span></span> <span data-ttu-id="06dee-105">La primera sección es para las interfaces (UUID + versión), la segunda contiene el objeto UUID y la tercera sección es para los identificadores de enlace.</span><span class="sxs-lookup"><span data-stu-id="06dee-105">The first section is for interfaces (UUID + version), the second section contains the object UUIDs, and the third section is for binding handles.</span></span> <span data-ttu-id="06dee-106">Proporcione un nombre para la entrada que sirva como una manera de identificarla.</span><span class="sxs-lookup"><span data-stu-id="06dee-106">You provide a name for the entry that will serve as a way to identify it.</span></span>

<span data-ttu-id="06dee-107">Al llamar a [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), el servidor especifica el nombre de la entrada en la que se va a colocar la información exportada.</span><span class="sxs-lookup"><span data-stu-id="06dee-107">When calling [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), the server specifies the name of the entry in which to place the exported information.</span></span> <span data-ttu-id="06dee-108">Esta nueva interfaz exportada se agrega a continuación a la sección interfaz de la entrada servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="06dee-108">This newly exported interface is then added to the interface section of the name service entry.</span></span> <span data-ttu-id="06dee-109">También se conservan las interfaces que ya están presentes en la entrada del servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="06dee-109">Any interfaces that are already present in the name service entry remain as well.</span></span> <span data-ttu-id="06dee-110">Este mismo proceso se sigue para los UUID de objeto y los identificadores de enlace.</span><span class="sxs-lookup"><span data-stu-id="06dee-110">This same process is followed for object UUIDs and binding handles.</span></span>

<span data-ttu-id="06dee-111">El cliente llama a [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (o [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) para buscar un identificador de enlace adecuado.</span><span class="sxs-lookup"><span data-stu-id="06dee-111">The client calls [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (or [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) to search for an appropriate binding handle.</span></span> <span data-ttu-id="06dee-112">Se extraen el nombre de la entrada, el identificador de interfaz y el UUID de un objeto.</span><span class="sxs-lookup"><span data-stu-id="06dee-112">The entry name, interface handle, and an object UUID are extracted.</span></span> <span data-ttu-id="06dee-113">Estos restringen las entradas de las que se devuelven los identificadores de enlace.</span><span class="sxs-lookup"><span data-stu-id="06dee-113">These restrict the entries from which binding handles are returned.</span></span> <span data-ttu-id="06dee-114">Si una entrada coincide con los criterios de búsqueda, todos los identificadores de enlace de esa entrada se devuelven desde [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span><span class="sxs-lookup"><span data-stu-id="06dee-114">If an entry matches the search criteria, all the binding handles in that entry are returned from [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span>

 

 




