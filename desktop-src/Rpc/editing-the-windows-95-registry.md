---
title: Editar el registro de Windows 95
description: Puede usar regedit para modificar el registro de Windows 95 para designar un NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903788"
---
# <a name="editing-the-windows-95-registry"></a><span data-ttu-id="ff26f-103">Editar el registro de Windows 95</span><span class="sxs-lookup"><span data-stu-id="ff26f-103">Editing the Windows 95 Registry</span></span>

<span data-ttu-id="ff26f-104">Puede usar regedit para modificar el registro de Windows 95 para designar un NSP.</span><span class="sxs-lookup"><span data-stu-id="ff26f-104">You can use REGEDIT to edit the Windows 95 registry to designate an NSP.</span></span>

<span data-ttu-id="ff26f-105">**Para designar un proveedor de servicios de nombres de Microsoft Locator para Windows 95**</span><span class="sxs-lookup"><span data-stu-id="ff26f-105">**To designate a Microsoft Locator name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="ff26f-106">Seleccionar</span><span class="sxs-lookup"><span data-stu-id="ff26f-106">Select</span></span>

    <span data-ttu-id="ff26f-107">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="ff26f-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="ff26f-108">Cree una nueva clave denominada</span><span class="sxs-lookup"><span data-stu-id="ff26f-108">Create a new key called</span></span>

    <span data-ttu-id="ff26f-109">**NameService**</span><span class="sxs-lookup"><span data-stu-id="ff26f-109">**NameService**</span></span>

3.  <span data-ttu-id="ff26f-110">Con la clave **NameService** seleccionada, cree los nuevos nombres de **valorstring** y modifíquelo para que contengan los datos, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ff26f-110">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="ff26f-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff26f-111">Name</span></span>                     | <span data-ttu-id="ff26f-112">Datos</span><span class="sxs-lookup"><span data-stu-id="ff26f-112">Data</span></span>                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | <span data-ttu-id="ff26f-113">**DefaultSyntax**</span><span class="sxs-lookup"><span data-stu-id="ff26f-113">**DefaultSyntax**</span></span>        | <span data-ttu-id="ff26f-114">3</span><span class="sxs-lookup"><span data-stu-id="ff26f-114">3</span></span><br/>                                                                |
    | <span data-ttu-id="ff26f-115">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="ff26f-115">**Protocol**</span></span>             | <span data-ttu-id="ff26f-116">NP de ncacn \_</span><span class="sxs-lookup"><span data-stu-id="ff26f-116">ncacn\_np</span></span><br/>                                                        |
    | <span data-ttu-id="ff26f-117">**Punto de conexión**</span><span class="sxs-lookup"><span data-stu-id="ff26f-117">**Endpoint**</span></span>             | <span data-ttu-id="ff26f-118">\\Localizador de canalización \\</span><span class="sxs-lookup"><span data-stu-id="ff26f-118">\\pipe\\locator</span></span><br/>                                                  |
    | <span data-ttu-id="ff26f-119">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="ff26f-119">**NetworkAddress**</span></span>       | <span data-ttu-id="ff26f-120">mi Server (donde he Server es el nombre del equipo Windows NT)</span><span class="sxs-lookup"><span data-stu-id="ff26f-120">myserver (where myserver is the name of the Windows NT computer)</span></span><br/> |
    | <span data-ttu-id="ff26f-121">**ServerNetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="ff26f-121">**ServerNetworkAddress**</span></span> | <span data-ttu-id="ff26f-122">myserver</span><span class="sxs-lookup"><span data-stu-id="ff26f-122">myserver</span></span><br/>                                                         |

    

     

<span data-ttu-id="ff26f-123">Puede usar regedit para modificar el registro de Windows 95 para designar un CD de DCE.</span><span class="sxs-lookup"><span data-stu-id="ff26f-123">You can use REGEDIT to edit the Windows 95 registry to designate a DCE CDS NSP.</span></span>

<span data-ttu-id="ff26f-124">**Para designar un proveedor de servicios de nombres de CDS de DCE para Windows 95**</span><span class="sxs-lookup"><span data-stu-id="ff26f-124">**To designate a DCE CDS name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="ff26f-125">Seleccionar</span><span class="sxs-lookup"><span data-stu-id="ff26f-125">Select</span></span>

    <span data-ttu-id="ff26f-126">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="ff26f-126">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="ff26f-127">Cree una nueva clave denominada</span><span class="sxs-lookup"><span data-stu-id="ff26f-127">Create a new key called</span></span>

    <span data-ttu-id="ff26f-128">**NameService**</span><span class="sxs-lookup"><span data-stu-id="ff26f-128">**NameService**</span></span>

3.  <span data-ttu-id="ff26f-129">Con la clave **NameService** seleccionada, cree los nuevos nombres de **valorstring** y modifíquelo para que contengan los datos, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ff26f-129">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="ff26f-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff26f-130">Name</span></span>                     | <span data-ttu-id="ff26f-131">Datos</span><span class="sxs-lookup"><span data-stu-id="ff26f-131">Data</span></span>                                                             |
    |--------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="ff26f-132">**DefaultSyntax**</span><span class="sxs-lookup"><span data-stu-id="ff26f-132">**DefaultSyntax**</span></span>        | <span data-ttu-id="ff26f-133">3</span><span class="sxs-lookup"><span data-stu-id="ff26f-133">3</span></span><br/>                                                     |
    | <span data-ttu-id="ff26f-134">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="ff26f-134">**Protocol**</span></span>             | <span data-ttu-id="ff26f-135">\_TCP IP \_ ncacn</span><span class="sxs-lookup"><span data-stu-id="ff26f-135">ncacn\_ip\_tcp</span></span><br/>                                        |
    | <span data-ttu-id="ff26f-136">**Punto de conexión**</span><span class="sxs-lookup"><span data-stu-id="ff26f-136">**Endpoint**</span></span>             | <span data-ttu-id="ff26f-137">"" (una cadena vacía)</span><span class="sxs-lookup"><span data-stu-id="ff26f-137">"" (an empty string)</span></span><br/>                                  |
    | <span data-ttu-id="ff26f-138">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="ff26f-138">**NetworkAddress**</span></span>       | <span data-ttu-id="ff26f-139">mi Server (el nombre del equipo host que ejecuta NSID)</span><span class="sxs-lookup"><span data-stu-id="ff26f-139">myserver (the name of the host computer running nsid)</span></span><br/> |
    | <span data-ttu-id="ff26f-140">**ServerNetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="ff26f-140">**ServerNetworkAddress**</span></span> | <span data-ttu-id="ff26f-141">mi Server (el nombre del equipo host que ejecuta NSID)</span><span class="sxs-lookup"><span data-stu-id="ff26f-141">myserver (the name of the host computer running nsid)</span></span><br/> |

    

     

    > [!Note]  
    > <span data-ttu-id="ff26f-142">Para configurar los CD de DCE como proveedor de servicios de nombres, debe disponer del producto DCE de Digital Equipment Corporation Servicio de directorio de celdas.</span><span class="sxs-lookup"><span data-stu-id="ff26f-142">You must have the Digital Equipment Corporation DCE Cell Directory Service product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="ff26f-143">Consulte la documentación proporcionada por Digital Equipment Corporation para obtener información acerca de los CD de DCE.</span><span class="sxs-lookup"><span data-stu-id="ff26f-143">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

     

 

 





