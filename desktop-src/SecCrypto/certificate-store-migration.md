---
description: Durante la actualización de un equipo o una migración de equipo a equipo, se migrarán los certificados de determinados almacenes de certificados.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migración del almacén de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083143"
---
# <a name="certificate-store-migration"></a>Migración del almacén de certificados

Durante la actualización de un equipo o una migración de equipo a equipo, se migrarán los certificados de determinados almacenes de certificados. En la tabla siguiente se enumeran los almacenes de certificados que se migran de forma predeterminada. En el almacén configuración de la solicitud de certificados automática (ACRS) del sistema, solo se migran las [*listas de certificados de confianza*](../secgloss/c-gly.md) (CTL). En el resto de almacenes que se enumeran a continuación, solo se migran los certificados.

<table>
<thead>
<tr class="header">
<th>Sistema/usuario</th>
<th>Tienda</th>
<th>Ubicación de almacenamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$ {ROWSPAN8} $System $ {REMOVE} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Raíz</strong> \ de <strong>Certificados</strong> de<br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Mi</strong> \ <strong>Certificados</strong> de<br/></td>

</tr>
<tr class="odd">
<td>Solicite</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Solicitud</strong> \ de <strong>Certificados</strong> de<br/></td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificados</strong> de<br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificados</strong> de<br/></td>

</tr>
<tr class="even">
<td>No permitida.</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ No <strong>permitido</strong> \ <strong>Certificados</strong> de<br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Entidad de certificación</strong> \ <strong>Certificados</strong> de<br/></td>

</tr>
<tr class="even">
<td>ACR</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>CTL</strong><br/></td>

</tr>
<tr class="odd">
<td rowspan="7">Usuario $ {REMOVE} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Raíz</strong> \ de <strong>Certificados</strong> de<br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td>archivo: \\ %AppData%\Microsoft\SystemCertificates\My\Certificates</td>

</tr>
<tr class="odd">
<td>Solicite</td>
<td>archivo: \\ %AppData%\Microsoft\SystemCertificates\Request\Certificates</td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificados</strong> de<br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificados</strong> de<br/></td>

</tr>
<tr class="even">
<td>No permitida.</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ No <strong>permitido</strong> \ <strong>Certificados</strong> de<br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ de <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Entidad de certificación</strong> \ <strong>Certificados</strong> de<br/></td>

</tr>
</tbody>
</table>



 

Otros almacenes de certificados creados por aplicaciones no se migran de forma predeterminada. Las aplicaciones que crean sus propias tiendas son responsables de la migración de los almacenes que crean. Para crear almacenes, se recomienda que defina una clave del registro en la configuración de la aplicación y que cree un almacén dentro de la configuración del registro mediante el proveedor de almacenamiento de **\_ Prov. \_ \_ reg del almacén de certificados** . Para obtener más información acerca de cómo migrar la configuración de la aplicación, consulte el tema *How to Create a Custom. xml file* en la guía *using USMT 3,0* en [herramienta de migración de estado de usuario 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx). (Es posible que este recurso no esté disponible en algunos idiomas y países o regiones).

 

 
