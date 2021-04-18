---
description: El objeto SafeWia es un \# punto de entrada &0034; Safe para scripting&\# 0034; para todas las funciones de scripting de adquisición de imágenes de Windows (WIA).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Objeto SafeWia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715184"
---
# <a name="safewia-object"></a><span data-ttu-id="c2bc4-103">Objeto SafeWia</span><span class="sxs-lookup"><span data-stu-id="c2bc4-103">SafeWia object</span></span>

<span data-ttu-id="c2bc4-104">El objeto **SafeWia** es un punto de entrada "Safe for scripting" para todas las funciones de scripting de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="c2bc4-104">The **SafeWia** object is a "safe for scripting" entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="c2bc4-105">Cualquier aplicación que use el modelo de scripting de WIA debe crear un objeto **SafeWia** o [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="c2bc4-105">Any application that uses the WIA scripting model must create a **SafeWia** or [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="c2bc4-106">Use ese objeto para enumerar y crear dispositivos y recibir notificaciones de eventos de hardware.</span><span class="sxs-lookup"><span data-stu-id="c2bc4-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

## <a name="members"></a><span data-ttu-id="c2bc4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2bc4-107">Members</span></span>

<span data-ttu-id="c2bc4-108">El objeto **SafeWia** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c2bc4-108">The **SafeWia** object has these types of members:</span></span>

-   [<span data-ttu-id="c2bc4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2bc4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c2bc4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2bc4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c2bc4-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2bc4-111">Methods</span></span>

<span data-ttu-id="c2bc4-112">El objeto **SafeWia** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c2bc4-112">The **SafeWia** object has these methods.</span></span>



| <span data-ttu-id="c2bc4-113">Método</span><span class="sxs-lookup"><span data-stu-id="c2bc4-113">Method</span></span>                             | <span data-ttu-id="c2bc4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2bc4-114">Description</span></span>                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2bc4-115">**A**</span><span class="sxs-lookup"><span data-stu-id="c2bc4-115">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="c2bc4-116">El método [**Create**](-wia-iwia-create.md) del objeto [**WIA**](-wia-wia.md) establece una conexión con el dispositivo WIA especificado y devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2bc4-116">The [**Create**](-wia-iwia-create.md) method of the [**Wia**](-wia-wia.md) object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c2bc4-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2bc4-117">Properties</span></span>

<span data-ttu-id="c2bc4-118">El objeto **SafeWia** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2bc4-118">The **SafeWia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c2bc4-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2bc4-119">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c2bc4-120">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="c2bc4-120">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c2bc4-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2bc4-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c2bc4-122"><a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2bc4-122"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c2bc4-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2bc4-123">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c2bc4-124">Colección de objetos <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> que representa todos los dispositivos instalados en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c2bc4-124">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="c2bc4-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c2bc4-125">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c2bc4-126">Esta colección está basada en 0.</span><span class="sxs-lookup"><span data-stu-id="c2bc4-126">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c2bc4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2bc4-127">Requirements</span></span>



| <span data-ttu-id="c2bc4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2bc4-128">Requirement</span></span> | <span data-ttu-id="c2bc4-129">Value</span><span class="sxs-lookup"><span data-stu-id="c2bc4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2bc4-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2bc4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c2bc4-131">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c2bc4-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2bc4-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2bc4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c2bc4-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2bc4-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c2bc4-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2bc4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2bc4-135"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c2bc4-135"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="c2bc4-136">IID</span><span class="sxs-lookup"><span data-stu-id="c2bc4-136">IID</span></span><br/>                      | <span data-ttu-id="c2bc4-137">CLSID \_ SafeWia</span><span class="sxs-lookup"><span data-stu-id="c2bc4-137">CLSID\_SafeWia</span></span><br/>                                                                                     |



## <a name="see-also"></a><span data-ttu-id="c2bc4-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2bc4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2bc4-139">**WIA**</span><span class="sxs-lookup"><span data-stu-id="c2bc4-139">**Wia**</span></span>](-wia-wia.md)
</dt> </dl>

 

 




