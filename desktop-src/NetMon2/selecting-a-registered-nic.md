---
description: Para seleccionar una de las NIC registradas en el equipo local, llame a la función GetNPPBlobFromUI.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Selección de una NIC registrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677639"
---
# <a name="selecting-a-registered-nic"></a><span data-ttu-id="c1613-103">Selección de una NIC registrada</span><span class="sxs-lookup"><span data-stu-id="c1613-103">Selecting a Registered NIC</span></span>

<span data-ttu-id="c1613-104">Para seleccionar una de las NIC registradas en el equipo local, llame a la función [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="c1613-104">To select one of the NICs registered on the local computer, call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span> <span data-ttu-id="c1613-105">Esta función usa la interfaz de usuario de Monitor de red para mostrar las NIC registradas y devuelve el BLOB NPP que representa la NIC seleccionada.</span><span class="sxs-lookup"><span data-stu-id="c1613-105">This function uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you select.</span></span> <span data-ttu-id="c1613-106">Puede mostrar todas las NIC registradas en el equipo local o un conjunto más pequeño de NIC filtradas.</span><span class="sxs-lookup"><span data-stu-id="c1613-106">You can display all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="c1613-107">Para filtrar las NIC que se muestran, proporcione un [*BLOB de filtro*](f.md) cuando se realice la llamada.</span><span class="sxs-lookup"><span data-stu-id="c1613-107">To filter the displayed NICs, provide a [*filter BLOB*](f.md) when the call is made.</span></span>

> [!Note]  
> <span data-ttu-id="c1613-108">Cuando se llama a la función [**GetNPPBlobFromUI**](getnppblobfromui.md) , el [*buscador de NPP*](n.md) se comunica con los archivos dll de NPP para obtener las estructuras de blobs NPP que representan las NIC registradas.</span><span class="sxs-lookup"><span data-stu-id="c1613-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the [*NPP Finder*](n.md) communicates with the NPP DLLs to obtain the NPP BLOB structures that represent the registered NICs.</span></span> <span data-ttu-id="c1613-109">Para obtener más información y un procedimiento sobre cómo usar la interfaz de usuario de Monitor de red directamente, vea el tema "seleccionar un cuadro de diálogo de red" en la ayuda en pantalla de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="c1613-109">For more information, and a procedure about how to use the Network Monitor UI directly, see the "Select a Network Dialog Box" topic in the Network Monitor online help.</span></span>

 

<span data-ttu-id="c1613-110">Cuando se llama a la función [**GetNPPBlobFromUI**](getnppblobfromui.md) , aparece el cuadro de diálogo **seleccionar una red** .</span><span class="sxs-lookup"><span data-stu-id="c1613-110">When you call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function, the **Select a network** dialog box appears.</span></span> <span data-ttu-id="c1613-111">En ella, puede ver los detalles de los NPPs registrados en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="c1613-111">From it, you can view the details of the NPPs registered on the local computer.</span></span> <span data-ttu-id="c1613-112">Esta información incluye NPPs locales y NPPs remoto.</span><span class="sxs-lookup"><span data-stu-id="c1613-112">This information includes both local NPPs and remote NPPs.</span></span> <span data-ttu-id="c1613-113">En el cuadro de diálogo, puede seleccionar una NIC específica y ver los detalles de su estructura de BLOBs NPP asociada.</span><span class="sxs-lookup"><span data-stu-id="c1613-113">From the dialog box, you can select a specific NIC and view the details of its associated NPP BLOB structure.</span></span>

<span data-ttu-id="c1613-114">En la ilustración siguiente se muestra la configuración típica de un NPP de NDIS proporcionado por Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="c1613-114">The following illustration shows typical settings of an NDIS NPP supplied by Network Monitor.</span></span>

![configuración típica de un NPP de NDIS proporcionado por el monitor de red](images/networkdb.png)

<span data-ttu-id="c1613-116">En la tabla siguiente se enumeran los temas que describen cada método de selección de NIC.</span><span class="sxs-lookup"><span data-stu-id="c1613-116">The following table lists topics that describe each NIC selection method.</span></span>



| <span data-ttu-id="c1613-117">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="c1613-117">For information about</span></span>                                                                          | <span data-ttu-id="c1613-118">Vea</span><span class="sxs-lookup"><span data-stu-id="c1613-118">See</span></span>                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1613-119">Cómo especificar un filtro que limite las NIC que se muestran en el cuadro de diálogo **seleccionar una red** .</span><span class="sxs-lookup"><span data-stu-id="c1613-119">How to specify a filter that limits the NICs displayed in the **Select a network** dialog box.</span></span> | [<span data-ttu-id="c1613-120">Especificación de un BLOB en filtro</span><span class="sxs-lookup"><span data-stu-id="c1613-120">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="c1613-121">Cómo seleccionar una NIC mediante una llamada a la función [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="c1613-121">How to select a NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>      | [<span data-ttu-id="c1613-122">Selección de una NIC mediante GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="c1613-122">Selecting a NIC using GetNPPBlobFromUI</span></span>](getnppblobfromui.md)                                       |
| <span data-ttu-id="c1613-123">Cómo seleccionar una NIC de una tabla BLOB de NPP proporcionada.</span><span class="sxs-lookup"><span data-stu-id="c1613-123">How to select a NIC from a supplied NPP BLOB table.</span></span>                                            | [<span data-ttu-id="c1613-124">Selección de una NIC de una tabla BLOB de NPP proporcionada</span><span class="sxs-lookup"><span data-stu-id="c1613-124">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



