---
description: 'Más información sobre: Campos de VistaParam'
title: Campos vistaParam (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: VistaParam fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_fields(v=EXCHG.10)
ms:contentKeyID: 55104336
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 3684f6d50ba0ca107614276776e375bc90b32a0d0e3e0112dded07b6e9e5bcdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718855"
---
# <a name="vistaparam-fields"></a>Campos de VistaParam

Incluir miembros protegidos  
Incluir miembros heredados  

El [tipo VistaParam](./vistaparam-class.md) expone los miembros siguientes.

## <a name="fields"></a>Campos

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
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></td>
<td>Este parámetro controla el número de recursos de árbol B+ almacenados en caché por la instancia después de que la aplicación haya cerrado las tablas que representan. Los valores grandes para este parámetro harán que el motor de base de datos use más memoria, pero aumentará la velocidad con la que la aplicación puede abrir aleatoriamente un gran número de tablas. Esto es útil para las aplicaciones que tienen un esquema con un número muy grande de tablas.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335289(v=exchg.10).md">Configuración</a></td>
<td>Este parámetro expone varios conjuntos de valores predeterminados para todo el conjunto de parámetros del sistema. Cuando este parámetro se establece en una configuración específica, todos los valores de parámetros del sistema se restablecen a sus valores predeterminados para esa configuración. Si la configuración se establece para una instancia específica, los parámetros globales del sistema no se restablecerán a sus valores predeterminados. Configuración pequeña (0): el motor de base de datos está optimizado para su uso en memoria. Configuración heredada (1): el motor de base de datos tiene sus valores predeterminados tradicionales.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></td>
<td>Este parámetro se usa para controlar cuándo el motor de base de datos acepta o rechaza los cambios en un subconjunto de los parámetros del sistema. Este parámetro se usa junto con <a href="dn335289(v=exchg.10).md">Configuration</a> para evitar que algunos parámetros del sistema se establezcan fuera de los valores predeterminados de la configuración seleccionada.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335291(v=exchg.10).md">EnableFileCache</a></td>
<td>Habilite el uso de la caché de archivos del sistema operativo para todos los archivos administrados.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335381(v=exchg.10).md">EnableViewCache</a></td>
<td>Habilite el uso de E/S de archivos asignados a memoria para los archivos de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335292(v=exchg.10).md">KeyMost</a></td>
<td>Este parámetro de solo lectura indica la longitud máxima de clave de índice permitido que se puede seleccionar para el tamaño de página de la base de datos actual (según lo configurado <a href="hh596135(v=exchg.10).md">por DatabasePageSize</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></td>
<td>Este parámetro proporciona compatibilidad con versiones anteriores con las convenciones de nomenclatura de archivos de versiones anteriores del motor de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335294(v=exchg.10).md">TableClass10Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 10.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335385(v=exchg.10).md">TableClass11Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 11.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335387(v=exchg.10).md">TableClass12Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 12.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335388(v=exchg.10).md">TableClass13Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 13.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335295(v=exchg.10).md">TableClass14Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 14.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335390(v=exchg.10).md">TableClass15Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 15.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335297(v=exchg.10).md">TableClass1Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 1.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335389(v=exchg.10).md">TableClass2Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 2.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335296(v=exchg.10).md">TableClass3Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 3.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335395(v=exchg.10).md">TableClass4Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 4.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335401(v=exchg.10).md">TableClass5Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 5.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335298(v=exchg.10).md">TableClass6Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 6.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335402(v=exchg.10).md">TableClass7Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 7.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335299(v=exchg.10).md">TableClass8Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 8.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335404(v=exchg.10).md">TableClass9Name</a></td>
<td>Establezca el nombre asociado a la clase de tabla 9.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[VistaParam (clase)](./vistaparam-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
