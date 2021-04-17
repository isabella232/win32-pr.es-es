---
description: El objeto DeviceInfo proporciona acceso a las propiedades de un dispositivo de hardware de adquisición de imágenes de Windows (WIA).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Objeto DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659885"
---
# <a name="deviceinfo-object"></a><span data-ttu-id="c8b16-103">Objeto DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="c8b16-103">DeviceInfo object</span></span>

<span data-ttu-id="c8b16-104">El objeto **DeviceInfo** proporciona acceso a las propiedades de un dispositivo de hardware de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="c8b16-104">The **DeviceInfo** object provides access to the properties of a Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="c8b16-105">También, a través de su método [**Create**](-wia-iwiadeviceinfo-create.md) , proporciona una forma para que la aplicación o el script se conecten al dispositivo y obtengan un objeto de [**elemento**](-wia-item.md) que represente el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8b16-105">It also, through its [**Create**](-wia-iwiadeviceinfo-create.md) method, provides a way for the application or script to connect to the device and obtain an [**Item**](-wia-item.md) object that represents the device.</span></span> <span data-ttu-id="c8b16-106">Use el método [**Devices**](-wia-iwia-devices.md) para obtener una colección de objetos **DeviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="c8b16-106">Use the [**Devices**](-wia-iwia-devices.md) method to obtain a collection of **DeviceInfo** objects.</span></span>

## <a name="members"></a><span data-ttu-id="c8b16-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c8b16-107">Members</span></span>

<span data-ttu-id="c8b16-108">El objeto **DeviceInfo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c8b16-108">The **DeviceInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="c8b16-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8b16-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c8b16-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8b16-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c8b16-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8b16-111">Methods</span></span>

<span data-ttu-id="c8b16-112">El objeto **DeviceInfo** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c8b16-112">The **DeviceInfo** object has these methods.</span></span>



| <span data-ttu-id="c8b16-113">Método</span><span class="sxs-lookup"><span data-stu-id="c8b16-113">Method</span></span>                                                 | <span data-ttu-id="c8b16-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8b16-114">Description</span></span>                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8b16-115">**A**</span><span class="sxs-lookup"><span data-stu-id="c8b16-115">**Create**</span></span>](-wia-iwiadeviceinfo-create.md)           | <span data-ttu-id="c8b16-116">El método [**Create**](-wia-iwiadeviceinfo-create.md) del objeto **DeviceInfo** establece una conexión con el dispositivo WIA especificado por el objeto **DeviceInfo** y devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8b16-116">The [**Create**](-wia-iwiadeviceinfo-create.md) method of the **DeviceInfo** object makes a connection to the WIA device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |
| [<span data-ttu-id="c8b16-117">**GetPropById**</span><span class="sxs-lookup"><span data-stu-id="c8b16-117">**GetPropById**</span></span>](-wia-iwiadeviceinfo-getpropbyid.md) | <span data-ttu-id="c8b16-118">El método [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) del objeto **DEVICEINFO** usa el identificador de una propiedad de dispositivo para devolver su valor.</span><span class="sxs-lookup"><span data-stu-id="c8b16-118">The [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) method of the **DeviceInfo** object uses a device property's ID to return its value.</span></span><br/>                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="c8b16-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8b16-119">Properties</span></span>

<span data-ttu-id="c8b16-120">El objeto **DeviceInfo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c8b16-120">The **DeviceInfo** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c8b16-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8b16-121">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c8b16-122">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="c8b16-122">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c8b16-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8b16-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c8b16-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Sesión</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8b16-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8b16-125">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-126">Recupera el identificador del dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="c8b16-126">Retrieves the ID of the WIA hardware device.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c8b16-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Le</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8b16-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Manufacturer</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8b16-128">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-129">Recupera el nombre del fabricante de este dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="c8b16-129">Retrieves the name of the manufacturer of this hardware device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c8b16-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8b16-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8b16-131">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-132">El nombre del dispositivo de hardware WIA tal como aparece en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8b16-132">The name of the WIA hardware device as it appears in the UI.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c8b16-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8b16-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8b16-134">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-135">Recupera el puerto al que está conectado el dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="c8b16-135">Retrieves the port to which the WIA hardware device is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c8b16-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Tipo</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8b16-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Type</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8b16-137">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-138">Recupera el tipo de dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="c8b16-138">Retrieves the type of WIA hardware device.</span></span> <span data-ttu-id="c8b16-139">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="c8b16-139">Possible values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="c8b16-140">DigitalCamera</span><span class="sxs-lookup"><span data-stu-id="c8b16-140">DigitalCamera</span></span></li>
<li><span data-ttu-id="c8b16-141">Escáner</span><span class="sxs-lookup"><span data-stu-id="c8b16-141">Scanner</span></span></li>
<li><span data-ttu-id="c8b16-142">StreamingVideo</span><span class="sxs-lookup"><span data-stu-id="c8b16-142">StreamingVideo</span></span></li>
<li><span data-ttu-id="c8b16-143">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="c8b16-143">Default</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c8b16-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8b16-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8b16-145">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c8b16-146">Recupera el ID. de clase de la interfaz de usuario proporcionada por el fabricante para este dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="c8b16-146">Retrieves the class id of the manufacturer-provided user interface for this WIA hardware device.</span></span> <span data-ttu-id="c8b16-147">El valor es una representación de cadena de un GUID.</span><span class="sxs-lookup"><span data-stu-id="c8b16-147">The value is a string representation of a GUID.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c8b16-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8b16-148">Requirements</span></span>



| <span data-ttu-id="c8b16-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8b16-149">Requirement</span></span> | <span data-ttu-id="c8b16-150">Value</span><span class="sxs-lookup"><span data-stu-id="c8b16-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b16-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8b16-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b16-152">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c8b16-152">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8b16-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8b16-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b16-154">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8b16-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c8b16-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8b16-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8b16-156"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c8b16-156"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




