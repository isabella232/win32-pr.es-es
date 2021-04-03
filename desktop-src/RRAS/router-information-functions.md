---
title: Funciones de información del enrutador
description: Utilice las siguientes funciones para manipular encabezados y bloques de información del enrutador. Un encabezado de información se compone de metadatos y bloques de información privados. Los bloques de información son matrices de estructuras de información de varios tipos.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074991"
---
# <a name="router-information-functions"></a><span data-ttu-id="19533-105">Funciones de información del enrutador</span><span class="sxs-lookup"><span data-stu-id="19533-105">Router Information Functions</span></span>

<span data-ttu-id="19533-106">Utilice las siguientes funciones para manipular encabezados y bloques de información del enrutador.</span><span class="sxs-lookup"><span data-stu-id="19533-106">Use the following functions to manipulate router information headers and blocks.</span></span> <span data-ttu-id="19533-107">Un encabezado de información se compone de metadatos y bloques de información privados.</span><span class="sxs-lookup"><span data-stu-id="19533-107">An information header is composed of private meta-data and information blocks.</span></span> <span data-ttu-id="19533-108">Los bloques de información son matrices de [estructuras de información](router-information-structures.md) de varios [tipos](router-information-enumerations.md).</span><span class="sxs-lookup"><span data-stu-id="19533-108">Information blocks are arrays of [information structures](router-information-structures.md) of various [types](router-information-enumerations.md).</span></span>

<span data-ttu-id="19533-109">Las siguientes funciones manipulan los encabezados de información:</span><span class="sxs-lookup"><span data-stu-id="19533-109">The following functions manipulate information headers:</span></span>

-   [<span data-ttu-id="19533-110">**MprInfoCreate**</span><span class="sxs-lookup"><span data-stu-id="19533-110">**MprInfoCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [<span data-ttu-id="19533-111">**MprInfoDelete**</span><span class="sxs-lookup"><span data-stu-id="19533-111">**MprInfoDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [<span data-ttu-id="19533-112">**MprInfoDuplicate**</span><span class="sxs-lookup"><span data-stu-id="19533-112">**MprInfoDuplicate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [<span data-ttu-id="19533-113">**MprInfoRemoveAll**</span><span class="sxs-lookup"><span data-stu-id="19533-113">**MprInfoRemoveAll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

<span data-ttu-id="19533-114">Las siguientes funciones manipulan bloques de información dentro de un encabezado de información:</span><span class="sxs-lookup"><span data-stu-id="19533-114">The following functions manipulate information blocks within an information header:</span></span>

-   [<span data-ttu-id="19533-115">**MprInfoBlockAdd**</span><span class="sxs-lookup"><span data-stu-id="19533-115">**MprInfoBlockAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [<span data-ttu-id="19533-116">**MprInfoBlockFind**</span><span class="sxs-lookup"><span data-stu-id="19533-116">**MprInfoBlockFind**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [<span data-ttu-id="19533-117">**MprInfoBlockQuerySize**</span><span class="sxs-lookup"><span data-stu-id="19533-117">**MprInfoBlockQuerySize**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [<span data-ttu-id="19533-118">**MprInfoBlockRemove**</span><span class="sxs-lookup"><span data-stu-id="19533-118">**MprInfoBlockRemove**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [<span data-ttu-id="19533-119">**MprInfoBlockSet**</span><span class="sxs-lookup"><span data-stu-id="19533-119">**MprInfoBlockSet**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

<span data-ttu-id="19533-120">Muchas de las [funciones de configuración y administración del enrutador](understanding-mprinfo-functions-and-information-headers.md) usan encabezados de información.</span><span class="sxs-lookup"><span data-stu-id="19533-120">Many of the [router administration and configuration functions](understanding-mprinfo-functions-and-information-headers.md) use information headers.</span></span>

 

 




