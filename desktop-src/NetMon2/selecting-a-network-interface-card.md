---
description: Monitor de red proporciona tres funciones para seleccionar una tarjeta de interfaz de red (NIC). Estas funciones proporcionan tres maneras de enumerar un conjunto de NIC y seleccionar el que desea usar. En la tabla siguiente se enumeran estas funciones.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Seleccionar una tarjeta de interfaz de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156037"
---
# <a name="selecting-a-network-interface-card"></a><span data-ttu-id="4b73c-105">Seleccionar una tarjeta de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="4b73c-105">Selecting a Network Interface Card</span></span>

<span data-ttu-id="4b73c-106">Monitor de red proporciona tres funciones para seleccionar una tarjeta de interfaz de red (NIC).</span><span class="sxs-lookup"><span data-stu-id="4b73c-106">Network Monitor provides three functions for selecting a network interface card (NIC).</span></span> <span data-ttu-id="4b73c-107">Estas funciones proporcionan tres maneras de enumerar un conjunto de NIC y seleccionar el que desea usar.</span><span class="sxs-lookup"><span data-stu-id="4b73c-107">These functions provide three ways to enumerate a set of NICs and select the one you want to use.</span></span> <span data-ttu-id="4b73c-108">En la tabla siguiente se enumeran estas funciones.</span><span class="sxs-lookup"><span data-stu-id="4b73c-108">The following table lists these functions.</span></span>



| <span data-ttu-id="4b73c-109">Función</span><span class="sxs-lookup"><span data-stu-id="4b73c-109">Function</span></span>                                                 | <span data-ttu-id="4b73c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b73c-110">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b73c-111">**GetNPPBlobFromUI**</span><span class="sxs-lookup"><span data-stu-id="4b73c-111">**GetNPPBlobFromUI**</span></span>](getnppblobfromui.md)             | <span data-ttu-id="4b73c-112">Usa la interfaz de usuario de Monitor de red para mostrar las NIC registradas y devuelve el BLOB NPP que representa la NIC en la que está interesado.</span><span class="sxs-lookup"><span data-stu-id="4b73c-112">Uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you are interested in.</span></span>           |
| [<span data-ttu-id="4b73c-113">**GetNPPBlobTable**</span><span class="sxs-lookup"><span data-stu-id="4b73c-113">**GetNPPBlobTable**</span></span>](getnppblobtable.md)               | <span data-ttu-id="4b73c-114">Devuelve una tabla de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="4b73c-114">Returns a BLOB table.</span></span> <span data-ttu-id="4b73c-115">La aplicación debe enumerar la tabla y seleccionar un BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="4b73c-115">The application must enumerate the table and select an NPP BLOB.</span></span>                                                       |
| [<span data-ttu-id="4b73c-116">**SelectNPPBlobFromTable**</span><span class="sxs-lookup"><span data-stu-id="4b73c-116">**SelectNPPBlobFromTable**</span></span>](selectnppblobfromtable.md) | <span data-ttu-id="4b73c-117">Usa la interfaz Monitor de red para mostrar los blobs NPP proporcionados y devuelve el BLOB NPP que representa la NIC en la que está interesado.</span><span class="sxs-lookup"><span data-stu-id="4b73c-117">Uses the Network Monitor interface to display the supplied NPP BLOBs and returns the NPP BLOB that represents the NIC you are interested in.</span></span> |



 

<span data-ttu-id="4b73c-118">Cada NIC se representa mediante un objeto binario grande (BLOB) de NPP.</span><span class="sxs-lookup"><span data-stu-id="4b73c-118">Each NIC is represented by an NPP binary large object (BLOB).</span></span> <span data-ttu-id="4b73c-119">Estas funciones pueden devolver un solo BLOB NPP de los registrados en el equipo, un único BLOB NPP de una tabla BLOB NPP suministrada, o una tabla de blobs NPP que el llamador debe usar para seleccionar un BLOB específico.</span><span class="sxs-lookup"><span data-stu-id="4b73c-119">These functions can return a single NPP BLOB from those registered on the computer, a single NPP BLOB from a supplied NPP BLOB table, or a table of NPP BLOBs that the caller must then use to select a specific BLOB.</span></span> <span data-ttu-id="4b73c-120">En los dos primeros casos, al seleccionar entre las NIC registradas o desde una tabla BLOB de NPP suministrada, la interfaz de usuario de Monitor de red muestra las NIC que puede seleccionar.</span><span class="sxs-lookup"><span data-stu-id="4b73c-120">In the first two cases, when selecting from the registered NICs or from a supplied NPP BLOB table, the Network Monitor UI displays the NICs you can select.</span></span>

> [!Note]  
> <span data-ttu-id="4b73c-121">Monitor de red usa una característica denominada buscador de NPP para enumerar las NIC registradas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="4b73c-121">Network Monitor uses a feature called the NPP Finder to enumerate the NICs registered on the local computer.</span></span> <span data-ttu-id="4b73c-122">El buscador de NPP es un componente de Npptools.dll.</span><span class="sxs-lookup"><span data-stu-id="4b73c-122">The NPP Finder is a component of Npptools.dll.</span></span>

 



| <span data-ttu-id="4b73c-123">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="4b73c-123">For information about</span></span>                            | <span data-ttu-id="4b73c-124">Vea</span><span class="sxs-lookup"><span data-stu-id="4b73c-124">See</span></span>                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b73c-125">Selección de una NIC registrada en el equipo local</span><span class="sxs-lookup"><span data-stu-id="4b73c-125">Selecting a NIC registered on the local computer</span></span> | [<span data-ttu-id="4b73c-126">Selección de una NIC registrada</span><span class="sxs-lookup"><span data-stu-id="4b73c-126">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="4b73c-127">Selección de una NIC de una tabla BLOB de NPP proporcionada</span><span class="sxs-lookup"><span data-stu-id="4b73c-127">Selecting a NIC from a supplied NPP BLOB table</span></span>   | [<span data-ttu-id="4b73c-128">Selección de una NIC de una tabla BLOB de NPP proporcionada</span><span class="sxs-lookup"><span data-stu-id="4b73c-128">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| <span data-ttu-id="4b73c-129">Recuperación de una tabla BLOB de NPP</span><span class="sxs-lookup"><span data-stu-id="4b73c-129">Retrieving an NPP BLOB table</span></span>                     | [<span data-ttu-id="4b73c-130">Selección de una NIC de una tabla BLOB NPP devuelta</span><span class="sxs-lookup"><span data-stu-id="4b73c-130">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



