---
title: Objetos ADSI de WinNT
description: El proveedor ADSI WinNT implementa los siguientes objetos COM para admitir características y servicios de varias interfaces ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- AdsI del proveedor de servicios WinNT, objetos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93332a2b0501c9c7c4140d83ff7358f18ae68adc50f9f9f3b689765d947ef01c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180589"
---
# <a name="adsi-objects-of-winnt"></a>Objetos ADSI de WinNT

El proveedor ADSI WinNT implementa los siguientes objetos COM para admitir características y servicios de varias interfaces ADSI.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>AdsI (objeto)</th>
<th>Descripción</th>
<th>Interfaces admitidas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Clase</strong></td>
<td>Objeto ADSI que representa una definición de clase.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADsClass</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong></strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Equipo</strong></td>
<td>Objeto ADSI que representa un equipo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Dominio</strong></td>
<td>Objeto ADSI que representa un dominio a través de la red.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FileService</strong></td>
<td>Objeto ADSI que representa un servicio de archivos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong></strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FileShare</strong></td>
<td>Objeto ADSI que representa un recurso compartido de archivos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FPNWFileService</strong></td>
<td>Objeto ADSI que representa un servicio de archivos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWFileShare</strong></td>
<td>Objeto ADSI que representa un recurso compartido de archivos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FPNWResource</strong></td>
<td>Objeto ADSI que representa un recurso.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWResourcesCollection</strong></td>
<td>Objeto ADSI que representa una colección de recursos.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>FPNWSession</strong></td>
<td>Objeto ADSI que representa una sesión.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWSessionsCollection</strong></td>
<td>Objeto ADSI que representa una colección de sesiones.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>Grupo</strong></td>
<td>Objeto ADSI que representa un grupo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl>
<blockquote>
[!Note]<br />
GetInfo no se puede usar para grupos que contienen miembros que son entidades de seguridad wellKnown en el ámbito WinNT.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>GroupCollection</strong></td>
<td>Objeto ADSI que representa una colección de grupos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADsMembers</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong></strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>LocalGroup</strong></td>
<td>Objeto ADSI que representa un grupo local.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>LocalgroupCollection</strong></td>
<td>Objeto ADSI que representa una colección de grupos locales.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADsMembers</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong></strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Espacio de nombres</strong></td>
<td>Objeto ADSI que representa el espacio de nombres WinNT.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Printjob</strong></td>
<td>Objeto ADSI que representa un trabajo de impresión.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>PrintJobsCollection</strong></td>
<td>Objeto ADSI que representa una colección de trabajos de impresión.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>PrintQueue</strong></td>
<td>Objeto ADSI que representa una cola de impresión.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Propiedad</strong></td>
<td>Objeto ADSI que representa una definición de atributo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADsProperty</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong></strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Recurso</strong></td>
<td>Objeto ADSI que representa un recurso.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>ResourcesCollection</strong></td>
<td>Objeto ADSI que representa una colección de recursos.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Esquema</strong></td>
<td>Objeto ADSI que representa el contenedor de esquema.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Servicio</strong></td>
<td>Objeto ADSI que representa un servicio.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>De sesión</strong></td>
<td>Objeto ADSI que representa una sesión.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>SessionsCollection</strong></td>
<td>Objeto ADSI que representa una colección de sesiones.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Sintaxis</strong></td>
<td>Objeto ADSI que representa la sintaxis de un atributo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax">IADsSyntax <strong></strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>User</strong></td>
<td>Objeto ADSI que representa una cuenta de usuario.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>UserGroupCollection</strong></td>
<td>Objeto ADSI que representa una colección de grupos de usuarios.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></td>
</tr>
</tbody>
</table>



 

 

 





