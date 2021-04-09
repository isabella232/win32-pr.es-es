---
description: El objeto WIA es el punto de entrada para todas las funciones de scripting de adquisición de imágenes de Windows (WIA).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: WIA (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154377"
---
# <a name="wia-object"></a><span data-ttu-id="3c430-103">WIA (objeto)</span><span class="sxs-lookup"><span data-stu-id="3c430-103">Wia object</span></span>

<span data-ttu-id="3c430-104">El objeto **WIA** es el punto de entrada para todas las funciones de scripting de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="3c430-104">The **Wia** object is the entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="3c430-105">Cualquier aplicación que use el modelo de scripting de WIA debe crear un objeto [**SafeWia**](-wia-safewia.md) o **WIA** .</span><span class="sxs-lookup"><span data-stu-id="3c430-105">Any application that uses the WIA scripting model must create a [**SafeWia**](-wia-safewia.md) or **Wia** object.</span></span> <span data-ttu-id="3c430-106">Use ese objeto para enumerar y crear dispositivos y recibir notificaciones de eventos de hardware.</span><span class="sxs-lookup"><span data-stu-id="3c430-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

> [!Note]  
> <span data-ttu-id="3c430-107">Este objeto no es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="3c430-107">This object is not safe for scripting.</span></span> <span data-ttu-id="3c430-108">Para obtener una versión de este objeto segura para el scripting, vea [**SafeWia**](-wia-safewia.md).</span><span class="sxs-lookup"><span data-stu-id="3c430-108">For a version of this object that is safe for scripting, see [**SafeWia**](-wia-safewia.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="3c430-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3c430-109">Members</span></span>

<span data-ttu-id="3c430-110">El objeto **WIA** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3c430-110">The **Wia** object has these types of members:</span></span>

-   [<span data-ttu-id="3c430-111">Eventos</span><span class="sxs-lookup"><span data-stu-id="3c430-111">Events</span></span>](#events)
-   [<span data-ttu-id="3c430-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c430-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3c430-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c430-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="3c430-114">Events</span><span class="sxs-lookup"><span data-stu-id="3c430-114">Events</span></span>

<span data-ttu-id="3c430-115">El objeto **WIA** tiene estos eventos.</span><span class="sxs-lookup"><span data-stu-id="3c430-115">The **Wia** object has these events.</span></span>



| <span data-ttu-id="3c430-116">Evento</span><span class="sxs-lookup"><span data-stu-id="3c430-116">Event</span></span>                                                                 | <span data-ttu-id="3c430-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c430-117">Description</span></span>                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="3c430-118">**OnDeviceConnected**</span><span class="sxs-lookup"><span data-stu-id="3c430-118">**OnDeviceConnected**</span></span>](-wia--iwiaevents-ondeviceconnected.md)       | <span data-ttu-id="3c430-119">Evento que tiene lugar cuando se conecta un nuevo dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="3c430-119">Event that occurs when a new WIA hardware device is connected.</span></span><br/>    |
| [<span data-ttu-id="3c430-120">**OnDeviceDisconnected**</span><span class="sxs-lookup"><span data-stu-id="3c430-120">**OnDeviceDisconnected**</span></span>](-wia--iwiaevents-ondevicedisconnected.md) | <span data-ttu-id="3c430-121">Evento que tiene lugar cuando se desconecta un dispositivo de hardware WIA nuevo.</span><span class="sxs-lookup"><span data-stu-id="3c430-121">Event that occurs when a new WIA hardware device is disconnected.</span></span><br/> |
| [<span data-ttu-id="3c430-122">**OnTransferComplete**</span><span class="sxs-lookup"><span data-stu-id="3c430-122">**OnTransferComplete**</span></span>](-wia--iwiaevents-ontransfercomplete.md)     | <span data-ttu-id="3c430-123">Evento que tiene lugar cuando se completa una transferencia de datos correctamente.</span><span class="sxs-lookup"><span data-stu-id="3c430-123">Event that occurs when a data transfer is completed successfully.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="3c430-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c430-124">Methods</span></span>

<span data-ttu-id="3c430-125">El objeto **WIA** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3c430-125">The **Wia** object has these methods.</span></span>



| <span data-ttu-id="3c430-126">Método</span><span class="sxs-lookup"><span data-stu-id="3c430-126">Method</span></span>                             | <span data-ttu-id="3c430-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c430-127">Description</span></span>                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c430-128">**A**</span><span class="sxs-lookup"><span data-stu-id="3c430-128">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="3c430-129">El método [**Create**](-wia-iwia-create.md) del objeto **WIA** establece una conexión con el dispositivo WIA especificado y devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c430-129">The [**Create**](-wia-iwia-create.md) method of the **Wia** object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3c430-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c430-130">Properties</span></span>

<span data-ttu-id="3c430-131">El objeto **WIA** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3c430-131">The **Wia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3c430-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3c430-132">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3c430-133">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="3c430-133">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3c430-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c430-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3c430-135"><a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c430-135"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c430-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3c430-136">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c430-137">Colección de objetos <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> que representa todos los dispositivos instalados en el equipo.</span><span class="sxs-lookup"><span data-stu-id="3c430-137">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="3c430-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3c430-138">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c430-139">Esta colección está basada en 0.</span><span class="sxs-lookup"><span data-stu-id="3c430-139">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3c430-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c430-140">Requirements</span></span>



| <span data-ttu-id="3c430-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c430-141">Requirement</span></span> | <span data-ttu-id="3c430-142">Value</span><span class="sxs-lookup"><span data-stu-id="3c430-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c430-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c430-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3c430-144">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3c430-144">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c430-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c430-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3c430-146">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c430-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3c430-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c430-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c430-148"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3c430-148"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="3c430-149">IID</span><span class="sxs-lookup"><span data-stu-id="3c430-149">IID</span></span><br/>                      | <span data-ttu-id="3c430-150">WIA de CLSID \_</span><span class="sxs-lookup"><span data-stu-id="3c430-150">CLSID\_Wia</span></span><br/>                                                                                         |



 

 




