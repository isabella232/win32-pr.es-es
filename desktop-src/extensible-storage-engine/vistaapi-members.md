---
description: 'Más información acerca de: miembros de VistaApi'
title: Miembros de VistaApi (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: VistaApi members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaApi
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi_members(v=EXCHG.10)
ms:contentKeyID: 55104282
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2c5e4c89dcf37285634fd6fc5e53468bf98e4d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082185"
---
# <a name="vistaapi-members"></a>Miembros de VistaApi

Incluir miembros protegidos  
Incluir miembros heredados  

Las API de ESENT que se admiten por primera vez en Windows Vista.

El tipo [VistaApi](./vistaapi-class.md) expone los siguientes miembros.

## <a name="methods"></a>Métodos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335319(v=exchg.10).md">JetGetColumnInfo</a></td>
<td>Recupera información sobre una columna de una tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351258(v=exchg.10).md">JetGetInstanceMiscInfo</a></td>
<td>Recupera información sobre una instancia de.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335320(v=exchg.10).md">JetGetRecordSize</a></td>
<td>Recupera información de tamaño del registro de la ubicación deseada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351264(v=exchg.10).md">JetGetThreadStats</a></td>
<td>Recupera información de rendimiento del motor de base de datos para el subproceso actual. Se pueden usar varias llamadas para recopilar estadísticas que reflejen la actividad del motor de base de datos en este subproceso entre esas llamadas.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351265(v=exchg.10).md">JetInit3</a></td>
<td>Inicialice el motor de base de datos ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable</a></td>
<td>Crea una tabla temporal con un índice único. Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex. Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil. También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial. Vea también <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351267(v=exchg.10).md">JetOSSnapshotEnd</a></td>
<td>Notifica al motor que la sesión de instantáneas ha finalizado.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351269(v=exchg.10).md">JetOSSnapshotGetFreezeInfo</a></td>
<td>Recupera la lista de instancias y bases de datos que forman parte de la sesión de instantáneas en un momento dado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335341(v=exchg.10).md">JetOSSnapshotPrepareInstance</a></td>
<td>Selecciona una instancia específica para que forme parte de la sesión de instantáneas.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335343(v=exchg.10).md">JetOSSnapshotTruncateLog</a></td>
<td>Habilita el truncamiento del registro para todas las instancias que forman parte de la sesión de instantáneas.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351271(v=exchg.10).md">JetOSSnapshotTruncateLogInstance</a></td>
<td>Trunca el registro de una instancia especificada durante una sesión de instantánea.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase VistaApi](./vistaapi-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
