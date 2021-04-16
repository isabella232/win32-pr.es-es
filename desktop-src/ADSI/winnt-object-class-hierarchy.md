---
title: Jerarquía de clases de objeto Winnt
description: La jerarquía de clases de objeto WinNT se inicia desde el objeto de espacio de nombres.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- Editor de servicios de WinNT ADSI, jerarquía de clases de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531834"
---
# <a name="winnt-object-class-hierarchy"></a><span data-ttu-id="4ccf8-104">Jerarquía de clases de objeto Winnt</span><span class="sxs-lookup"><span data-stu-id="4ccf8-104">WinNT Object Class Hierarchy</span></span>

<span data-ttu-id="4ccf8-105">La jerarquía de clases de objeto WinNT se inicia desde el objeto de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-105">The WinNT object class hierarchy starts from the Namespace object.</span></span>



| <span data-ttu-id="4ccf8-106">Object (clase)</span><span class="sxs-lookup"><span data-stu-id="4ccf8-106">Object class</span></span>                   | <span data-ttu-id="4ccf8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ccf8-107">Description</span></span>                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4ccf8-108">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4ccf8-108">Namespace</span></span><br/>           | <span data-ttu-id="4ccf8-109">Contenedor de objetos de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-109">Top-level object container.</span></span><br/>                                            |
| <span data-ttu-id="4ccf8-110">Domain</span><span class="sxs-lookup"><span data-stu-id="4ccf8-110">Domain</span></span><br/>              | <span data-ttu-id="4ccf8-111">Dominio de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-111">The Windows NT domain.</span></span><br/>                                                 |
| <span data-ttu-id="4ccf8-112">User (Usuario)</span><span class="sxs-lookup"><span data-stu-id="4ccf8-112">User</span></span><br/>                | <span data-ttu-id="4ccf8-113">Cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-113">User account.</span></span><br/>                                                          |
| <span data-ttu-id="4ccf8-114">Grupo</span><span class="sxs-lookup"><span data-stu-id="4ccf8-114">Group</span></span><br/>               | <span data-ttu-id="4ccf8-115">Cuenta de grupo para administrar derechos de acceso.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-115">Group account for managing access rights.</span></span><br/>                              |
| <span data-ttu-id="4ccf8-116">UserGroupCollection</span><span class="sxs-lookup"><span data-stu-id="4ccf8-116">UserGroupCollection</span></span><br/> | <span data-ttu-id="4ccf8-117">Conjunto de grupos de usuarios que implementan [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span><span class="sxs-lookup"><span data-stu-id="4ccf8-117">A set of user groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/>  |
| <span data-ttu-id="4ccf8-118">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="4ccf8-118">GroupCollection</span></span><br/>     | <span data-ttu-id="4ccf8-119">Un conjunto de otros grupos que implementan [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span><span class="sxs-lookup"><span data-stu-id="4ccf8-119">A set of other groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/> |
| <span data-ttu-id="4ccf8-120">Computer</span><span class="sxs-lookup"><span data-stu-id="4ccf8-120">Computer</span></span><br/>            | <span data-ttu-id="4ccf8-121">Windows NT 4,0 Server o Workstation.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-121">Windows NT 4.0 server or workstation.</span></span><br/>                                  |
| <span data-ttu-id="4ccf8-122">PrintJob</span><span class="sxs-lookup"><span data-stu-id="4ccf8-122">PrintJob</span></span><br/>            | <span data-ttu-id="4ccf8-123">Trabajo de impresión en la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-123">Print job in the print queue.</span></span><br/>                                          |
| <span data-ttu-id="4ccf8-124">PrintJobsCollection</span><span class="sxs-lookup"><span data-stu-id="4ccf8-124">PrintJobsCollection</span></span><br/> | <span data-ttu-id="4ccf8-125">Un conjunto de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-125">A set of print jobs.</span></span><br/>                                                   |
| <span data-ttu-id="4ccf8-126">PrintQueue</span><span class="sxs-lookup"><span data-stu-id="4ccf8-126">PrintQueue</span></span><br/>          | <span data-ttu-id="4ccf8-127">Cola de impresión en un administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-127">Print queue on a printer spooler.</span></span><br/>                                      |
| <span data-ttu-id="4ccf8-128">Servicio</span><span class="sxs-lookup"><span data-stu-id="4ccf8-128">Service</span></span><br/>             | <span data-ttu-id="4ccf8-129">Aplicación que se ejecuta como un servicio.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-129">Application running as a service.</span></span><br/>                                      |
| <span data-ttu-id="4ccf8-130">FileService</span><span class="sxs-lookup"><span data-stu-id="4ccf8-130">FileService</span></span><br/>         | <span data-ttu-id="4ccf8-131">Servicios que acceden al sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-131">Services accessing file system.</span></span><br/>                                        |
| <span data-ttu-id="4ccf8-132">FileShare</span><span class="sxs-lookup"><span data-stu-id="4ccf8-132">FileShare</span></span><br/>           | <span data-ttu-id="4ccf8-133">Punto de recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-133">File share point.</span></span><br/>                                                      |
| <span data-ttu-id="4ccf8-134">Recurso</span><span class="sxs-lookup"><span data-stu-id="4ccf8-134">Resource</span></span><br/>            | <span data-ttu-id="4ccf8-135">Un recurso en el servicio.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-135">A resource in the service.</span></span><br/>                                             |
| <span data-ttu-id="4ccf8-136">Sesión</span><span class="sxs-lookup"><span data-stu-id="4ccf8-136">Session</span></span><br/>             | <span data-ttu-id="4ccf8-137">Una conexión de servicio de archivos activa.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-137">An active file service connection.</span></span><br/>                                     |
| <span data-ttu-id="4ccf8-138">User (Usuario)</span><span class="sxs-lookup"><span data-stu-id="4ccf8-138">User</span></span><br/>                | <span data-ttu-id="4ccf8-139">Cuenta de usuario local.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-139">Local user account.</span></span><br/>                                                    |
| <span data-ttu-id="4ccf8-140">Grupo</span><span class="sxs-lookup"><span data-stu-id="4ccf8-140">Group</span></span><br/>               | <span data-ttu-id="4ccf8-141">Grupo local.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-141">Local group.</span></span><br/>                                                           |
| <span data-ttu-id="4ccf8-142">UserCollection</span><span class="sxs-lookup"><span data-stu-id="4ccf8-142">UserCollection</span></span><br/>      | <span data-ttu-id="4ccf8-143">Colección de usuarios locales.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-143">Collection of local users.</span></span><br/>                                             |
| <span data-ttu-id="4ccf8-144">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="4ccf8-144">GroupCollection</span></span><br/>     | <span data-ttu-id="4ccf8-145">Colección de grupos locales.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-145">Collection of local groups.</span></span><br/>                                            |
| <span data-ttu-id="4ccf8-146">Schema</span><span class="sxs-lookup"><span data-stu-id="4ccf8-146">Schema</span></span><br/>              | <span data-ttu-id="4ccf8-147">Contenedor de esquemas de Winnt.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-147">WinNT Schema container.</span></span><br/>                                                |
| <span data-ttu-id="4ccf8-148">Clase</span><span class="sxs-lookup"><span data-stu-id="4ccf8-148">Class</span></span><br/>               | <span data-ttu-id="4ccf8-149">Definición de clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-149">Schema class definition.</span></span><br/>                                               |
| <span data-ttu-id="4ccf8-150">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4ccf8-150">Property</span></span><br/>            | <span data-ttu-id="4ccf8-151">Definición de atributo de esquema.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-151">Schema attribute definition.</span></span><br/>                                           |
| <span data-ttu-id="4ccf8-152">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ccf8-152">Syntax</span></span><br/>              | <span data-ttu-id="4ccf8-153">Sintaxis de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="4ccf8-153">Syntax of a property.</span></span><br/>                                                  |



 

 

 





