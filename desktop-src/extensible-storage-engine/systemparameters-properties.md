---
description: 'Más información acerca de: propiedades de SystemParameters'
title: Propiedades de SystemParameters
TOCTitle: SystemParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55104035
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 12e18b6c045758c8e9fd7ffb91f728c78dcf2e24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571735"
---
# <a name="systemparameters-properties"></a>Propiedades de SystemParameters

Incluir miembros protegidos  
Incluir miembros heredados  

El tipo [SystemParameters](./systemparameters-class.md) expone los siguientes miembros.

## <a name="properties"></a>Propiedades

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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351215(v=exchg.10).md">BookmarkMost</a></td>
<td>Obtiene el tamaño máximo de un marcador. <a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351214(v=exchg.10).md">CacheSize</a></td>
<td>Obtiene o establece el tamaño de la memoria caché de la base de datos en páginas. De forma predeterminada, la memoria caché de base de datos ajustará automáticamente su tamaño y, si se establece esta propiedad en un valor distinto de cero, la memoria caché se ajustará al tamaño de destino.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></td>
<td>Obtiene o establece el tamaño máximo de la memoria caché de páginas de base de datos. El tamaño está en páginas de base de datos. Si este parámetro se deja en su valor predeterminado, el tamaño máximo de la memoria caché se establecerá en el tamaño de la memoria física cuando se llame a JetInit.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></td>
<td>Obtiene o establece el tamaño mínimo de la memoria caché de páginas de base de datos, en páginas de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></td>
<td>Obtiene el número máximo de componentes en una clave de ordenación o de índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351218(v=exchg.10).md">Configuración</a></td>
<td>Obtiene o establece un valor que especifica los valores predeterminados para todo el conjunto de parámetros del sistema. Cuando este parámetro se establece en una configuración específica, se restablecen los valores predeterminados de todos los valores de los parámetros del sistema para esa configuración. Si se establece la configuración para una instancia específica de, los parámetros globales del sistema no se restablecerán a sus valores predeterminados. Configuración pequeña (0): el motor de base de datos está optimizado para el uso de memoria. Configuración heredada (1): el motor de base de datos tiene sus valores predeterminados tradicionales. Compatible con Windows Vista y up. Se omite en Windows XP y Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></td>
<td>Obtiene o establece el tamaño de las páginas de base de datos, en bytes.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></td>
<td>Obtiene o establece un valor que indica si el motor de base de datos acepta o rechaza los cambios en un subconjunto de los parámetros del sistema. Este parámetro se usa junto con la <a href="dn351218(v=exchg.10).md">configuración</a> para evitar que algunos parámetros del sistema se establezcan fuera de los valores predeterminados de la configuración seleccionada. Compatible con Windows Vista y up. Se omite en Windows XP y Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351152(v=exchg.10).md">EnableFileCache</a></td>
<td>Obtiene o establece un valor que indica si el motor de base de datos debe utilizar la memoria caché de archivos del sistema operativo para todos los archivos administrados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351220(v=exchg.10).md">EnableViewCache</a></td>
<td>Obtiene o establece un valor que indica si el motor de base de datos debe utilizar e/s de archivos asignados en memoria para los archivos de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></td>
<td>Obtiene o establece el nivel de detalle de los mensajes de registro de eventos que el motor de base de datos emite al registro de eventos. Los números más altos producirán mensajes de registro de eventos más detallados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351154(v=exchg.10).md">ExceptionAction</a></td>
<td>Obtiene o establece la codificación de valores que se debe hacer con las excepciones generadas en JET.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351227(v=exchg.10).md">HungIOActions</a></td>
<td>Obtiene o establece el conjunto de acciones que deben realizarse en IOs que aparecen bloqueados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></td>
<td>Obtiene o establece el umbral de lo que se considera una e/s bloqueada en la que se debe actuar.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351156(v=exchg.10).md">KeyMost</a></td>
<td>Obtiene el tamaño máximo de la clave. Esto depende de la versión de esent y del tamaño de página de la base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></td>
<td>Obtiene o establece la compatibilidad con versiones anteriores de las convenciones de nomenclatura de los archivos de las versiones anteriores del motor de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></td>
<td>Obtiene el tamaño de fragmentos de LV. Esto depende del tamaño de página de la base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351230(v=exchg.10).md">MaxInstances</a></td>
<td>Obtiene o establece el número máximo de instancias que se pueden crear.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></td>
<td>Obtiene o establece la cantidad más pequeña de datos que se debe comprimir con la compresión Xpress.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></td>
<td>Este parámetro controla el número de operaciones de e/s de archivos de base de datos que se pueden poner en cola por disco en el sistema operativo host al mismo tiempo. Un valor mayor para este parámetro puede ayudar significativamente al rendimiento de una aplicación de base de datos grande.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></td>
<td>Obtiene o establece el nombre descriptivo para esta instancia del proceso.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></td>
<td>Obtiene o establece el umbral en el que la caché de páginas de base de datos comienza a expulsar páginas de la memoria caché para dejar espacio a las páginas que no están almacenadas en caché. Cuando el número de búferes de página en la memoria caché cae por debajo de este umbral, se iniciará un proceso en segundo plano para reponer ese grupo de búferes disponibles. Este umbral siempre es relativo al tamaño máximo de la memoria caché establecido por JET_paramCacheSizeMax. Este umbral también debe ser siempre inferior al umbral de detención establecido por JET_paramStopFlushThreshold. El alto de distancia del umbral de inicio determinará el tiempo de respuesta que debe tener la caché de páginas de base de datos para generar los búferes disponibles antes de que la aplicación los necesite. Un umbral de inicio alto proporcionará al proceso en segundo plano más tiempo para reaccionar. Sin embargo, un umbral de inicio alto implica un umbral de detención mayor y reduce el tamaño efectivo de la caché de páginas de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></td>
<td>Obtiene o establece el umbral en el que la caché de páginas de base de datos termina la expulsión de las páginas de la memoria caché para dejar espacio a las páginas que no están almacenadas en caché. Cuando el número de búferes de página de la memoria caché supera este umbral, se detiene el proceso en segundo plano que se inició para reponer el grupo de búferes disponibles. Este umbral siempre es relativo al tamaño máximo de la memoria caché establecido por JET_paramCacheSizeMax. Este umbral también debe ser siempre mayor que el umbral de inicio establecido por JET_paramStartFlushThreshold. La distancia entre el umbral de inicio y el umbral de detención afecta a la eficacia con la que el proceso en segundo plano vacía las páginas de la base de datos. Una brecha más grande hará que sea más probable que se combinen las escrituras en páginas vecinas. Sin embargo, un umbral de detención alta reducirá el tamaño efectivo de la caché de páginas de base de datos.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[SystemParameters (clase)](./systemparameters-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
