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
# <a name="adsi-objects-of-winnt"></a>Objetos ADSI de Winnt

El proveedor ADSI WinNT implementa los siguientes objetos COM para admitir características y servicios de diversas interfaces ADSI.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Objeto ADSI</th>
<th>Descripción</th>
<th>Interfaces admitidas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Clase</strong></td>
<td>Objeto ADSI que representa una definición de clase.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>IADsClass</strong> de iAds</a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Equipo</strong></td>
<td>Objeto ADSI que representa un equipo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Dominio</strong></td>
<td>Objeto ADSI que representa un dominio a través de la red.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FileService</strong></td>
<td>Objeto ADSI que representa un servicio de archivos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FileShare</strong></td>
<td>Objeto ADSI que representa un recurso compartido de archivos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsFileShare iAds </dl></td>
</tr>
<tr class="even">
<td><strong>FPNWFileService</strong></td>
<td>Objeto ADSI que representa un servicio de archivos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> de iAds <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWFileShare</strong></td>
<td>Objeto ADSI que representa un recurso compartido de archivos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsFileShare iAds </dl></td>
</tr>
<tr class="even">
<td><strong>FPNWResource</strong></td>
<td>Objeto ADSI que representa un recurso.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsResource iAds </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWResourcesCollection</strong></td>
<td>Objeto ADSI que representa una colección de recursos.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>FPNWSession</strong></td>
<td>Objeto ADSI que representa una sesión.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsSession iAds </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWSessionsCollection</strong></td>
<td>Objeto ADSI que representa una colección de sesiones.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>Grupo</strong></td>
<td>Objeto ADSI que representa un grupo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsGroup iAds </dl>
<blockquote>
[!Note]<br />
No se puede usar GetInfo para grupos que contienen miembros que son entidades de seguridad integradas en el ámbito de Winnt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>GroupCollection</strong></td>
<td>Objeto ADSI que representa una colección de grupos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong> de iAds</a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>LocalGroup</strong></td>
<td>Objeto ADSI que representa un grupo local.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsGroup iAds </dl></td>
</tr>
<tr class="odd">
<td><strong>LocalgroupCollection</strong></td>
<td>Objeto ADSI que representa una colección de grupos locales.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong> de iAds</a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Espacio de nombres</strong></td>
<td>Objeto ADSI que representa el espacio de nombres Winnt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> de iAds de iAds </dl></td>
</tr>
<tr class="odd">
<td><strong>PrintJob</strong></td>
<td>Objeto ADSI que representa un trabajo de impresión.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> iAds <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>PrintJobsCollection</strong></td>
<td>Objeto ADSI que representa una colección de trabajos de impresión.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>PrintQueue</strong></td>
<td>Objeto ADSI que representa una cola de impresión.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> iAds <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Propiedad</strong></td>
<td>Objeto ADSI que representa una definición de atributo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>IADsProperty</strong> de iAds</a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Recurso</strong></td>
<td>Objeto ADSI que representa un recurso.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsResource iAds </dl></td>
</tr>
<tr class="even">
<td><strong>ResourcesCollection</strong></td>
<td>Objeto ADSI que representa una colección de recursos.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Esquema</strong></td>
<td>Objeto ADSI que representa el contenedor del esquema.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong> de iAds</a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Servicio</strong></td>
<td>Objeto ADSI que representa un servicio.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> iAds <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>De sesión</strong></td>
<td>Objeto ADSI que representa una sesión.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsSession iAds </dl></td>
</tr>
<tr class="even">
<td><strong>SessionsCollection</strong></td>
<td>Objeto ADSI que representa una colección de sesiones.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Sintaxis</strong></td>
<td>Objeto ADSI que representa la sintaxis de un atributo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>IADsSyntax</strong> de iAds</a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>User</strong></td>
<td>Objeto ADSI que representa una cuenta de usuario.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> IADsUser iAds </dl></td>
</tr>
<tr class="odd">
<td><strong>UserGroupCollection</strong></td>
<td>Objeto ADSI que representa una colección de grupos de usuarios.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></td>
</tr>
</tbody>
</table>



 

 

 





