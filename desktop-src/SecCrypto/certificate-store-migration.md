---
description: Durante una actualización del equipo o una migración de equipo a equipo, se migrarán los certificados de determinados almacenes de certificados.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migración del almacén de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de694fc24433ce8db039dd677f52935da70cbf07d0a719b0871bd1e8f4b2d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771101"
---
# <a name="certificate-store-migration"></a>Migración del almacén de certificados

Durante una actualización del equipo o una migración de equipo a equipo, se migrarán los certificados de determinados almacenes de certificados. En la tabla siguiente se enumeran los almacenes de certificados que se migran de forma predeterminada. Para el almacén de solicitudes automáticas de Configuración (ACRS) del sistema, solo se migran las listas de confianza de certificados [](../secgloss/c-gly.md) (CL). Para todos los demás almacenes enumerados a continuación, solo se migran los certificados.

<table>
<thead>
<tr class="header">
<th>Sistema o usuario</th>
<th>Tienda</th>
<th>Ubicación de almacenamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>${ROWSPAN8}$System${REMOVE}$<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Raíz</strong> \ <strong>Certificados</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>My</strong> \ <strong>Certificados</strong><br/></td>

</tr>
<tr class="odd">
<td>REQUEST</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Solicitud</strong> \ <strong>Certificados</strong><br/></td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificados</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificados</strong><br/></td>

</tr>
<tr class="even">
<td>No permitida.</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>No permitido</strong> \ <strong>Certificados</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>CA</strong> \ <strong>Certificados</strong><br/></td>

</tr>
<tr class="even">
<td>Acrs</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>CL</strong><br/></td>

</tr>
<tr class="odd">
<td rowspan="7">User${REMOVE}$<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Raíz</strong> \ <strong>Certificados</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td>file: \\ %APPDATA%\Microsoft\SystemCertificates\My\Certificates</td>

</tr>
<tr class="odd">
<td>REQUEST</td>
<td>file: \\ %APPDATA%\Microsoft\SystemCertificates\Request\Certificates</td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificados</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificados</strong><br/></td>

</tr>
<tr class="even">
<td>No permitida.</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>No permitido</strong> \ <strong>Certificados</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>CA</strong> \ <strong>Certificados</strong><br/></td>

</tr>
</tbody>
</table>



 

Otros almacenes de certificados creados por aplicaciones no se migran de forma predeterminada. Las aplicaciones que crean sus propios almacenes son responsables de la migración de los almacenes que crean. Para crear almacenes, se recomienda definir una clave del Registro en la configuración de la aplicación y crear un almacén dentro de la configuración del Registro mediante el proveedor de **\_ almacén CERT STORE \_ PROV \_ REG.** Para obtener más información sobre cómo migrar la configuración de la aplicación, vea el tema *How to Create a Custom .xml File* en la guía Using USMT 3.0 (Uso de *USMT 3.0)* [Herramienta de migración de estado de usuario 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx). (Es posible que este recurso no esté disponible en algunos idiomas y países o regiones).

 

 
