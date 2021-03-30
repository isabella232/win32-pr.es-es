---
title: Objetos ADSI de Winnt
description: El proveedor ADSI WinNT implementa los siguientes objetos COM para admitir características y servicios de diversas interfaces ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- ADSI, objetos ADSI del proveedor de servicios de Winnt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d0c9e5c486d07e1e392a9f307ecd9af4509ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148743"
---
# <a name="adsi-objects-of-winnt"></a><span data-ttu-id="5c0c9-104">Objetos ADSI de Winnt</span><span class="sxs-lookup"><span data-stu-id="5c0c9-104">ADSI Objects of WinNT</span></span>

<span data-ttu-id="5c0c9-105">El proveedor ADSI WinNT implementa los siguientes objetos COM para admitir características y servicios de diversas interfaces ADSI.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-105">The ADSI WinNT provider implement the following COM objects to support features and services of various ADSI interfaces.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c0c9-106">Objeto ADSI</span><span class="sxs-lookup"><span data-stu-id="5c0c9-106">ADSI Object</span></span></th>
<th><span data-ttu-id="5c0c9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c0c9-107">Description</span></span></th>
<th><span data-ttu-id="5c0c9-108">Interfaces admitidas</span><span class="sxs-lookup"><span data-stu-id="5c0c9-108">Supported Interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c0c9-109"><strong>Clase</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-109"><strong>Class</strong></span></span></td>
<td><span data-ttu-id="5c0c9-110">Objeto ADSI que representa una definición de clase.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-110">An ADSI object that represents a class definition.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>IADsClass</strong> de iAds</a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>IADsClass</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-112"><strong>Equipo</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-112"><strong>Computer</strong></span></span></td>
<td><span data-ttu-id="5c0c9-113">Objeto ADSI que representa un equipo.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-113">An ADSI object that represents a computer.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-115"><strong>Dominio</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-115"><strong>Domain</strong></span></span></td>
<td><span data-ttu-id="5c0c9-116">Objeto ADSI que representa un dominio a través de la red.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-116">An ADSI object that represents a domain over the network.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-118"><strong>FileService</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-118"><strong>FileService</strong></span></span></td>
<td><span data-ttu-id="5c0c9-119">Objeto ADSI que representa un servicio de archivos.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-119">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-121"><strong>FileShare</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-121"><strong>FileShare</strong></span></span></td>
<td><span data-ttu-id="5c0c9-122">Objeto ADSI que representa un recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-122">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsFileShare iAds </span><span class="sxs-lookup"><span data-stu-id="5c0c9-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-124"><strong>FPNWFileService</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-124"><strong>FPNWFileService</strong></span></span></td>
<td><span data-ttu-id="5c0c9-125">Objeto ADSI que representa un servicio de archivos.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-125">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> de iAds <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-127"><strong>FPNWFileShare</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-127"><strong>FPNWFileShare</strong></span></span></td>
<td><span data-ttu-id="5c0c9-128">Objeto ADSI que representa un recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-128">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsFileShare iAds </span><span class="sxs-lookup"><span data-stu-id="5c0c9-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-130"><strong>FPNWResource</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-130"><strong>FPNWResource</strong></span></span></td>
<td><span data-ttu-id="5c0c9-131">Objeto ADSI que representa un recurso.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-131">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsResource iAds </span><span class="sxs-lookup"><span data-stu-id="5c0c9-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-133"><strong>FPNWResourcesCollection</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-133"><strong>FPNWResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="5c0c9-134">Objeto ADSI que representa una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-134">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="5c0c9-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c0c9-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-136"><strong>FPNWSession</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-136"><strong>FPNWSession</strong></span></span></td>
<td><span data-ttu-id="5c0c9-137">Objeto ADSI que representa una sesión.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-137">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsSession iAds </span><span class="sxs-lookup"><span data-stu-id="5c0c9-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-139"><strong>FPNWSessionsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-139"><strong>FPNWSessionsCollection</strong></span></span></td>
<td><span data-ttu-id="5c0c9-140">Objeto ADSI que representa una colección de sesiones.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-140">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="5c0c9-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c0c9-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-142"><strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-142"><strong>Group</strong></span></span></td>
<td><span data-ttu-id="5c0c9-143">Objeto ADSI que representa un grupo.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-143">An ADSI object that represents a group.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsGroup iAds </span><span class="sxs-lookup"><span data-stu-id="5c0c9-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl>
<blockquote>
[!Note]<br />
<span data-ttu-id="5c0c9-145">No se puede usar GetInfo para grupos que contienen miembros que son entidades de seguridad integradas en el ámbito de Winnt.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-145">GetInfo cannot be used for groups that contain members that are wellKnown security principals in the WinNT scope.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-146"><strong>GroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-146"><strong>GroupCollection</strong></span></span></td>
<td><span data-ttu-id="5c0c9-147">Objeto ADSI que representa una colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-147">An ADSI object that represents a collection of groups.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong> de iAds</a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-149"><strong>LocalGroup</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-149"><strong>LocalGroup</strong></span></span></td>
<td><span data-ttu-id="5c0c9-150">Objeto ADSI que representa un grupo local.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-150">An ADSI object that represents a local group.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsGroup iAds </span><span class="sxs-lookup"><span data-stu-id="5c0c9-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-152"><strong>LocalgroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-152"><strong>LocalgroupCollection</strong></span></span></td>
<td><span data-ttu-id="5c0c9-153">Objeto ADSI que representa una colección de grupos locales.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-153">An ADSI object that represents a collection of local groups.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong> de iAds</a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-155"><strong>Espacio de nombres</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-155"><strong>Namespace</strong></span></span></td>
<td><span data-ttu-id="5c0c9-156">Objeto ADSI que representa el espacio de nombres Winnt.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-156">An ADSI object that represents the WinNT namespace.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> de iAds de iAds </span><span class="sxs-lookup"><span data-stu-id="5c0c9-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-158"><strong>PrintJob</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-158"><strong>PrintJob</strong></span></span></td>
<td><span data-ttu-id="5c0c9-159">Objeto ADSI que representa un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-159">An ADSI object that represents a print job.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> iAds <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-161"><strong>PrintJobsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-161"><strong>PrintJobsCollection</strong></span></span></td>
<td><span data-ttu-id="5c0c9-162">Objeto ADSI que representa una colección de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-162">An ADSI object that represents a collection of print jobs.</span></span></td>
<td><span data-ttu-id="5c0c9-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c0c9-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-164"><strong>PrintQueue</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-164"><strong>PrintQueue</strong></span></span></td>
<td><span data-ttu-id="5c0c9-165">Objeto ADSI que representa una cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-165">An ADSI object that represents a print queue.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> iAds <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-167"><strong>Propiedad</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-167"><strong>Property</strong></span></span></td>
<td><span data-ttu-id="5c0c9-168">Objeto ADSI que representa una definición de atributo.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-168">An ADSI object that represents an attribute definition.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>IADsProperty</strong> de iAds</a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-170"><strong>Recurso</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-170"><strong>Resource</strong></span></span></td>
<td><span data-ttu-id="5c0c9-171">Objeto ADSI que representa un recurso.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-171">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsResource iAds </span><span class="sxs-lookup"><span data-stu-id="5c0c9-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-173"><strong>ResourcesCollection</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-173"><strong>ResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="5c0c9-174">Objeto ADSI que representa una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-174">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="5c0c9-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c0c9-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-176"><strong>Esquema</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-176"><strong>Schema</strong></span></span></td>
<td><span data-ttu-id="5c0c9-177">Objeto ADSI que representa el contenedor del esquema.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-177">An ADSI object that represents the schema container.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong> de iAds</a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-179"><strong>Servicio</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-179"><strong>Service</strong></span></span></td>
<td><span data-ttu-id="5c0c9-180">Objeto ADSI que representa un servicio.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-180">An ADSI object that represents a service.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> iAds <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-182"><strong>De sesión</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-182"><strong>Session</strong></span></span></td>
<td><span data-ttu-id="5c0c9-183">Objeto ADSI que representa una sesión.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-183">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsSession iAds </span><span class="sxs-lookup"><span data-stu-id="5c0c9-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-185"><strong>SessionsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-185"><strong>SessionsCollection</strong></span></span></td>
<td><span data-ttu-id="5c0c9-186">Objeto ADSI que representa una colección de sesiones.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-186">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="5c0c9-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c0c9-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-188"><strong>Sintaxis</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-188"><strong>Syntax</strong></span></span></td>
<td><span data-ttu-id="5c0c9-189">Objeto ADSI que representa la sintaxis de un atributo.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-189">An ADSI object that represents the syntax of an attribute.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>IADsSyntax</strong> de iAds</a></dt> </span><span class="sxs-lookup"><span data-stu-id="5c0c9-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0c9-191"><strong>User</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-191"><strong>User</strong></span></span></td>
<td><span data-ttu-id="5c0c9-192">Objeto ADSI que representa una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-192">An ADSI object that represents a user account.</span></span></td>
<td><dl> <span data-ttu-id="5c0c9-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsUser iAds </span><span class="sxs-lookup"><span data-stu-id="5c0c9-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0c9-194"><strong>UserGroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="5c0c9-194"><strong>UserGroupCollection</strong></span></span></td>
<td><span data-ttu-id="5c0c9-195">Objeto ADSI que representa una colección de grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="5c0c9-195">An ADSI object that represents a collection of user groups.</span></span></td>
<td><span data-ttu-id="5c0c9-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c0c9-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





