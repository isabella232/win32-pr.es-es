---
description: 'Más información acerca de: miembros de API'
title: Miembros de API
TOCTitle: Api members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api_members(v=EXCHG.10)
ms:contentKeyID: 55100778
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e1debc551dc644d71568772761cb14500d2fd546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423591"
---
# <a name="api-members"></a>Miembros de API

Incluir miembros protegidos  
Incluir miembros heredados  

Versiones administradas de la API de ESENT. Esta clase contiene métodos estáticos que corresponden a la API ESENT no administrada. Estos métodos producen excepciones cuando se devuelven errores. Métodos auxiliares para la API de ESENT. Estos encapsulan JetMakeKey. Métodos solo internos de la API. Métodos auxiliares para la API de ESENT. Estos realizan la conversión de datos para JetMakeKey. Métodos auxiliares para la API de ESENT. Estos métodos tratan con los metadatos de la base de datos. Métodos auxiliares para la API de ESENT. No se trata de versiones de interoperabilidad de la API, sino que encapsulan usos muy comunes de las funciones. Miembros de API marcados como obsoletos. Métodos auxiliares para la API de ESENT. No se trata de versiones de interoperabilidad de la API, sino que encapsulan usos muy comunes de las funciones. Métodos auxiliares para la API de ESENT. Estos realizan la conversión de datos para establecer columnas.

El tipo de [API](./api-class.md) expone los siguientes miembros.

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
<td><a href="dn292138(v=exchg.10).md">DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Deserializa un objeto de una columna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292115(v=exchg.10).md">DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Deserializa un objeto de una columna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292114(v=exchg.10).md">EscrowUpdate</a></td>
<td>Realizar la adición atómica en una columna. La columna debe ser de tipo <a href="hh577895(v=exchg.10).md">Long</a>. Esta función permite que varias sesiones actualicen el mismo registro simultáneamente sin conflictos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292099(v=exchg.10).md">GetBookmark</a></td>
<td>Recupera el marcador del registro asociado a la entrada de índice en la posición actual de un cursor. Este marcador se puede usar para volver a colocar el cursor en el mismo registro mediante JetGotoBookmark.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292098(v=exchg.10).md">GetColumnDictionary</a></td>
<td>Crea un diccionario que asigna nombres de columna a los identificadores de columna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292101(v=exchg.10).md">GetTableColumnid</a></td>
<td>Obtiene el columnid de la columna especificada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292090(v=exchg.10).md">GetTableColumns (JET_SESID, JET_TABLEID)</a></td>
<td>Recorre en iteración todas las columnas de la tabla y devuelve información sobre cada una de ellas.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292089(v=exchg.10).md">GetTableColumns (JET_SESID, JET_DBID, cadena)</a></td>
<td>Recorre en iteración todas las columnas de la tabla y devuelve información sobre cada una de ellas.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292093(v=exchg.10).md">GetTableIndexes (JET_SESID, JET_TABLEID)</a></td>
<td>Recorre en iteración todos los índices de la tabla y devuelve información sobre cada uno de ellos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292092(v=exchg.10).md">GetTableIndexes (JET_SESID, JET_DBID, cadena)</a></td>
<td>Recorre en iteración todos los índices de la tabla y devuelve información sobre cada uno de ellos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292095(v=exchg.10).md">GetTableNames</a></td>
<td>Devuelve los nombres de las tablas de la base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292094(v=exchg.10).md">IntersectIndexes</a></td>
<td>Intersecte un grupo de intervalos de índice y devuelva los marcadores de los registros que se encuentran en todos los intervalos de índice. Vea también <a href="dn292212(v=exchg.10).md">JetIntersectIndexes (JET_SESID, [], Int32, JET_RECORDLIST, IntersectIndexesGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292097(v=exchg.10).md">JetAddColumn</a></td>
<td>Agregue una nueva columna a una tabla existente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292096(v=exchg.10).md">JetAttachDatabase</a></td>
<td>Adjunta un archivo de base de datos para su uso con una instancia de base de datos. Para usar la base de datos, deberá abrirse posteriormente con <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292100(v=exchg.10).md">JetAttachDatabase2</a></td>
<td>Adjunta un archivo de base de datos para su uso con una instancia de base de datos. Para usar la base de datos, deberá abrirse posteriormente con <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292102(v=exchg.10).md">JetBackupInstance</a></td>
<td>Realiza una copia de seguridad de secuencias de una instancia, incluidas todas las bases de datos adjuntas, en un directorio. Con varios métodos de copia de seguridad admitidos por el motor de, esta es la función más sencilla y encapsulada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance</a></td>
<td>Inicia una copia de seguridad externa mientras el motor y la base de datos están en línea y activos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292103(v=exchg.10).md">JetBeginSession</a></td>
<td>Inicializar una nueva sesión ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292105(v=exchg.10).md">JetBeginTransaction</a></td>
<td>Hace que una sesión escriba una transacción o cree un nuevo punto de retorno en una transacción existente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292106(v=exchg.10).md">JetBeginTransaction2</a></td>
<td>Hace que una sesión escriba una transacción o cree un nuevo punto de retorno en una transacción existente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292107(v=exchg.10).md">JetCloseDatabase</a></td>
<td>Cierra un archivo de base de datos que se abrió previamente con <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID, cadena, cadena, JET_DBID, OpenDatabaseGrbit)</a> o creado con <a href="dn292118(v=exchg.10).md">JetCreateDatabase (JET_SESID, cadena, cadena, JET_DBID, CreateDatabaseGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292108(v=exchg.10).md">JetCloseFileInstance</a></td>
<td>Cierra un archivo que se abrió con JetOpenFileInstance una vez extraídos los datos de ese archivo mediante JetReadFileInstance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292109(v=exchg.10).md">JetCloseTable</a></td>
<td>Cierre una tabla abierta.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292110(v=exchg.10).md">JetCommitTransaction</a></td>
<td>Confirma los cambios realizados en el estado de la base de datos durante el punto de almacenamiento actual y los migra al punto de almacenamiento anterior. Si se confirma el punto de almacenamiento más externo, los cambios realizados durante ese punto de almacenamiento se confirmarán en el estado de la base de datos y la sesión finalizará la transacción.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292112(v=exchg.10).md">JetCompact</a></td>
<td>Realiza una copia de una base de datos existente. La copia se compacta con un estado óptimo para su uso. Los datos de los datos copiados se empaquetarán de acuerdo con las medidas elegidas para los índices en la creación de índices. De esta manera, los datos comprimidos se pueden almacenar de la forma más densa posible. Como alternativa, los datos compactos pueden reservar espacio para las inserciones de índice o el crecimiento de registros posteriores.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292113(v=exchg.10).md">JetComputeStats</a></td>
<td>Recorre cada índice de una tabla para calcular exactamente el número de entradas de un índice y el número de claves distintas de un índice. Esta información, junto con el número de páginas de base de datos asignadas para un índice y la hora actual del cálculo, se almacena en los metadatos de índice de la base de datos. Estos datos se pueden recuperar posteriormente con operaciones de información.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292118(v=exchg.10).md">JetCreateDatabase</a></td>
<td>Crea y adjunta un archivo de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292120(v=exchg.10).md">JetCreateDatabase2</a></td>
<td>Crea y adjunta un archivo de base de datos con un tamaño máximo de base de datos especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292121(v=exchg.10).md">JetCreateIndex</a></td>
<td>Crea un índice sobre los datos en una base de datos ESE. Un índice se puede usar para buscar datos específicos rápidamente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292123(v=exchg.10).md">JetCreateIndex2</a></td>
<td>Crea índices sobre los datos de una base de datos ESE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292122(v=exchg.10).md">JetCreateInstance</a></td>
<td>Asigna una nueva instancia del motor de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292126(v=exchg.10).md">JetCreateInstance2</a></td>
<td>Asignar una nueva instancia del motor de base de datos para su uso en un único proceso, con un nombre para mostrar especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292127(v=exchg.10).md">JetCreateTable</a></td>
<td>Cree una tabla vacía. La tabla recién creada se abre exclusivamente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3</a></td>
<td>Crea una tabla, agrega columnas e índices en esa tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292130(v=exchg.10).md">JetDefragment</a></td>
<td>Inicia y detiene las tareas de desfragmentación de bases de datos que mejora la organización de datos en una base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292145(v=exchg.10).md">JetDefragment2</a></td>
<td>Inicia y detiene las tareas de desfragmentación de bases de datos que mejora la organización de datos en una base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292131(v=exchg.10).md">JetDelete</a></td>
<td>Elimina el registro actual de una tabla de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292133(v=exchg.10).md">JetDeleteColumn</a></td>
<td>Elimina una columna de una tabla de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292132(v=exchg.10).md">JetDeleteColumn2</a></td>
<td>Elimina una columna de una tabla de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292135(v=exchg.10).md">JetDeleteIndex</a></td>
<td>Elimina un índice de una tabla de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292134(v=exchg.10).md">JetDeleteTable</a></td>
<td>Elimina una tabla de una base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292139(v=exchg.10).md">JetDetachDatabase</a></td>
<td>Libera un archivo de base de datos que se adjuntó previamente a una sesión de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292136(v=exchg.10).md">JetDetachDatabase2</a></td>
<td>Libera un archivo de base de datos que se adjuntó previamente a una sesión de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292137(v=exchg.10).md">JetDupCursor</a></td>
<td>Duplica un cursor abierto y devuelve un identificador al cursor duplicado. Si el cursor que se duplicó era un cursor de solo lectura, el cursor duplicado también es un cursor de solo lectura. Cualquier estado relacionado con la creación de una clave de búsqueda o la actualización de un registro no se copia en el cursor duplicado. Además, la ubicación del cursor original no se duplica en el cursor duplicado. El cursor duplicado siempre se abre en el índice clúster y su ubicación siempre está en la primera fila de la tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292140(v=exchg.10).md">JetDupSession</a></td>
<td>Inicializa una nueva sesión de ESE en la misma instancia que el sesid especificado.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292142(v=exchg.10).md">JetEndExternalBackupInstance</a></td>
<td>Finaliza una sesión de copia de seguridad externa. Esta API es la última API en una serie de API a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292143(v=exchg.10).md">JetEndExternalBackupInstance2</a></td>
<td>Finaliza una sesión de copia de seguridad externa. Esta API es la última API en una serie de API a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292144(v=exchg.10).md">JetEndSession</a></td>
<td>Finaliza una sesión.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292148(v=exchg.10).md">JetEnumerateColumns</a></td>
<td>Recupera eficazmente un conjunto de columnas y sus valores del registro actual de un cursor o del búfer de copia de ese cursor. Las columnas y los valores recuperados se pueden restringir por una lista de identificadores de columna, números de itagSequence y otras características. Esta API de recuperación de columnas es única, ya que devuelve información en memoria asignada dinámicamente que se obtiene mediante una devolución de llamada compatible con realloc proporcionada por el usuario. Esta nueva flexibilidad permite la recuperación eficaz de datos de columna con características específicas (como el tamaño y la multiplicidad) que son desconocidas para el autor de la llamada. Esto elimina la necesidad de usar los modos de detección de JetRetrieveColumn para determinar esas características a fin de configurar una llamada final a JetRetrieveColumn que recupere correctamente los datos deseados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292150(v=exchg.10).md">JetEscrowUpdate</a></td>
<td>Realiza una operación de suma atómica en una columna. Esta función permite que varias sesiones actualicen el mismo registro simultáneamente sin conflictos. Vea también <a href="dn292114(v=exchg.10).md">EscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292147(v=exchg.10).md">JetFreeBuffer</a></td>
<td>Libera memoria asignada por una llamada del motor de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292154(v=exchg.10).md">JetGetAttachInfoInstance</a></td>
<td>Se usa durante una copia de seguridad iniciada por <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)</a> para consultar a una instancia los nombres de los archivos de base de datos que deben formar parte del conjunto de archivos de copia de seguridad. Solo se tendrán en cuenta las bases de datos que están asociadas actualmente a la instancia mediante <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> . Estos archivos se pueden abrir posteriormente con <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> y leer mediante <a href="dn332987(v=exchg.10).md">JetReadFileInstance (JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292149(v=exchg.10).md">JetGetBookmark</a></td>
<td>Recupera el marcador del registro asociado a la entrada de índice en la posición actual de un cursor. Este marcador se puede usar para volver a colocar el cursor en el mismo registro mediante <a href="dn292200(v=exchg.10).md">JetGotoBookmark (JET_SESID, JET_TABLEID, [], Int32)</a>. El marcador no tendrá más de <a href="dn351215(v=exchg.10).md">BookmarkMost</a> bytes. Vea también <a href="dn292099(v=exchg.10).md">GetBookmark (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292158(v=exchg.10).md">JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena, JET_COLUMNBASE)</a></td>
<td>Recupera información sobre una columna de una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292151(v=exchg.10).md">JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena, JET_COLUMNDEF)</a></td>
<td>Recupera información sobre una columna de la tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292152(v=exchg.10).md">JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena, JET_COLUMNLIST)</a></td>
<td>Recupera información acerca de todas las columnas de una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292153(v=exchg.10).md">JetGetCurrentIndex</a></td>
<td>Ddetermines el nombre del índice actual de un cursor determinado. Este nombre también se usa para volver a seleccionar más adelante dicho índice como el índice actual mediante <a href="dn334011(v=exchg.10).md">JetSetCurrentIndex (JET_SESID, JET_TABLEID, cadena)</a>. También se puede usar para detectar las propiedades de ese índice mediante JetGetTableIndexInfo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292155(v=exchg.10).md">JetGetCursorInfo</a></td>
<td>Determinar si una actualización del registro actual de un cursor producirá un conflicto de escritura, según el estado actual de actualización del registro. Es posible que se devuelva un conflicto de escritura en última instancia, incluso si JetGetCursorInfo devuelve un valor correcto. debido a que otra sesión puede actualizar el registro antes de que la sesión actual pueda actualizar el mismo registro.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292159(v=exchg.10).md">JetGetDatabaseFileInfo (cadena, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Recupera cierta información sobre la base de datos dada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292161(v=exchg.10).md">JetGetDatabaseFileInfo (String, Int32, JET_DbInfo)</a></td>
<td>Recupera cierta información sobre la base de datos dada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292160(v=exchg.10).md">JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)</a></td>
<td>Recupera cierta información sobre la base de datos dada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292162(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID, JET_DBID, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Recupera cierta información sobre la base de datos dada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292164(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID, JET_DBID, Int32, JET_DbInfo)</a></td>
<td>Recupera cierta información sobre la base de datos dada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292167(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID, JET_DBID, cadena, JET_DbInfo)</a></td>
<td>Recupera cierta información sobre la base de datos dada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292168(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, JET_INDEXLIST)</a></td>
<td><strong>Obsoleto.</strong> Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292172(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292166(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292171(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, Int32, JET_IdxInfo)</a></td>
<td>Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292169(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, cadena, JET_IdxInfo)</a></td>
<td>Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292173(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</a></td>
<td>Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292170(v=exchg.10).md">JetGetInstanceInfo</a></td>
<td>Recupera información sobre las instancias de que se están ejecutando.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292175(v=exchg.10).md">JetGetLock</a></td>
<td>Reserve explícitamente la capacidad de actualizar una fila, un bloqueo de escritura o impedir explícitamente que una fila se actualice en cualquier otra sesión, bloqueo de lectura. Normalmente, los bloqueos de escritura de filas se adquieren implícitamente como resultado de la actualización de filas. Normalmente, los bloqueos de lectura no son necesarios debido a las versiones de registros. Sin embargo, en algunos casos, una transacción puede desear bloquear explícitamente una fila para aplicar la serialización o asegurarse de que una operación posterior se realizará correctamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292174(v=exchg.10).md">JetGetLogInfoInstance</a></td>
<td>Se usa durante una copia de seguridad iniciada por <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)</a> para consultar a una instancia los nombres de los archivos de revisión de la base de datos y los archivos de registro que deben formar parte del conjunto de archivos de copia de seguridad. Estos archivos se pueden abrir posteriormente con <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> y leer mediante <a href="dn332987(v=exchg.10).md">JetReadFileInstance (JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292177(v=exchg.10).md">JetGetLS</a></td>
<td>Permite que la aplicación recupere el identificador de contexto conocido como almacenamiento local que está asociado a un cursor o la tabla asociada a ese cursor. Este identificador de contexto se debe haber establecido previamente mediante <a href="dn334015(v=exchg.10).md">JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)</a>. JetGetLS también se puede usar para capturar simultáneamente el identificador de contexto actual para un cursor o una tabla y restablecer ese identificador de contexto.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292179(v=exchg.10).md">JetGetObjectInfo (JET_SESID, JET_DBID, JET_OBJECTLIST)</a></td>
<td>Recupera información acerca de los objetos de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292178(v=exchg.10).md">JetGetObjectInfo (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)</a></td>
<td>Recupera información acerca de los objetos de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292181(v=exchg.10).md">JetGetRecordPosition</a></td>
<td>Devuelve la posición fraccionaria del registro actual en el índice actual en forma de estructura de <a href="dn335256(v=exchg.10).md">JET_RECPOS</a> . Vea también <a href="dn292207(v=exchg.10).md">JetGotoPosition (JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292180(v=exchg.10).md">JetGetSecondaryIndexBookmark</a></td>
<td>Recupera un marcador especial para la entrada de índice secundario en la posición actual de un cursor. Este marcador se puede usar para volver a colocar eficazmente ese cursor en la misma entrada de índice mediante JetGotoSecondaryIndexBookmark. Esto es muy útil cuando se cambia la posición en un índice secundario que contiene claves duplicadas o que contiene varias entradas de índice para el mismo registro.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292182(v=exchg.10).md">JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</a></td>
<td>Obtiene las opciones de configuración de la base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292185(v=exchg.10).md">JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)</a></td>
<td>Obtiene las opciones de configuración de la base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292186(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</a></td>
<td>Recupera información sobre una columna de la tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292187(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID, JET_TABLEID, cadena, JET_COLUMNDEF)</a></td>
<td>Recupera información sobre una columna de la tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292189(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID, JET_TABLEID, cadena, JET_COLUMNLIST)</a></td>
<td>Recupera información acerca de todas las columnas de la tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292191(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, cadena, JET_INDEXLIST)</a></td>
<td><strong>Obsoleto.</strong> Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292190(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, cadena, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292196(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, cadena, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292193(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</a></td>
<td>Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292192(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, cadena, cadena, JET_IdxInfo)</a></td>
<td>Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292195(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</a></td>
<td>Recupera información acerca de los índices de una tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a></td>
<td>Recupera varios fragmentos de información sobre una tabla de una base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a></td>
<td>Recupera varios fragmentos de información sobre una tabla de una base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a></td>
<td>Recupera varios fragmentos de información sobre una tabla de una base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a></td>
<td>Recupera varios fragmentos de información sobre una tabla de una base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, cadena, JET_TblInfo)</a></td>
<td>Recupera varios fragmentos de información sobre una tabla de una base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292199(v=exchg.10).md">JetGetTruncateLogInfoInstance</a></td>
<td>Se usa durante una copia de seguridad iniciada por <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)</a> para consultar a una instancia los nombres de los archivos de registro de transacciones que se pueden eliminar de forma segura después de que la copia de seguridad se haya completado correctamente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292203(v=exchg.10).md">JetGetVersion</a></td>
<td>Recupera la versión del motor de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292200(v=exchg.10).md">JetGotoBookmark</a></td>
<td>Coloca un cursor en una entrada de índice para el registro asociado al marcador especificado. El marcador se puede usar con cualquier índice definido en una tabla. El marcador de un registro se puede recuperar mediante <a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292207(v=exchg.10).md">JetGotoPosition</a></td>
<td>Mueve un cursor a una nueva ubicación que es una fracción del camino a través del índice actual. Vea también <a href="dn292181(v=exchg.10).md">JetGetRecordPosition (JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark</a></td>
<td>Coloca un cursor en una entrada de índice que está asociada al marcador de índice secundario especificado. El marcador de índice secundario debe usarse con el mismo índice en la misma tabla desde la que se recuperó originalmente. El marcador de índice secundario de una entrada de índice se puede recuperar mediante <a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, [], Int32, [], Int32, GotoSecondaryIndexBookmarkGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292206(v=exchg.10).md">JetGrowDatabase</a></td>
<td>Extiende el tamaño de una base de datos que está abierta actualmente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292208(v=exchg.10).md">JetIdle</a></td>
<td>Realiza tareas de limpieza inactiva o comprueba el estado del almacén de versiones en ESE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292209(v=exchg.10).md">JetIndexRecordCount</a></td>
<td>Cuenta el número de entradas en el índice actual desde la posición actual hacia delante. La posición actual se incluye en el recuento. El recuento puede ser mayor que el número total de registros de la tabla si el índice actual está sobre una columna de varios valores y las instancias de la columna tienen varios valores. Si la tabla está vacía, se devolverá 0 para el recuento.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292210(v=exchg.10).md">JetInit</a></td>
<td>Inicialice el motor de base de datos ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292214(v=exchg.10).md">JetInit2</a></td>
<td>Inicialice el motor de base de datos ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292212(v=exchg.10).md">JetIntersectIndexes</a></td>
<td>Calcula la intersección entre varios conjuntos de entradas de índice de distintos índices secundarios en la misma tabla. Esta operación es útil para buscar el conjunto de registros de una tabla que coinciden con dos o más criterios que se pueden expresar mediante intervalos de índice. Vea también <a href="dn292094(v=exchg.10).md">IntersectIndexes (JET_SESID, [])</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292216(v=exchg.10).md">JetMakeKey</a></td>
<td>Construye claves de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292218(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)</a></td>
<td>Desplazarse por un índice. Se puede colocar el cursor al principio o al final del índice y moverse hacia atrás y hacia delante un número especificado de entradas de índice. Vea también <a href="dn334150(v=exchg.10).md">TryMoveFirst (JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast (JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext (JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a></td>
<td>Desplazarse por un índice. Se puede colocar el cursor al principio o al final del índice y moverse hacia atrás y hacia delante un número especificado de entradas de índice. Vea también <a href="dn334150(v=exchg.10).md">TryMoveFirst (JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast (JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext (JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292219(v=exchg.10).md">JetOpenDatabase</a></td>
<td>Abre una base de datos adjuntada previamente con <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a>para su uso con una sesión de base de datos. Se puede llamar a esta función varias veces para la misma base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292230(v=exchg.10).md">JetOpenFileInstance</a></td>
<td>Abre una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones de una instancia activa con el fin de realizar una copia de seguridad aproximada de streaming. Posteriormente, los datos de estos archivos se pueden leer a través del controlador devuelto mediante JetReadFileInstance. El identificador devuelto debe cerrarse mediante JetCloseFileInstance. Se debe haber iniciado previamente una copia de seguridad externa de la instancia mediante JetBeginExternalBackupInstance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292234(v=exchg.10).md">JetOpenTable</a></td>
<td>Abre un cursor en una tabla creada anteriormente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292231(v=exchg.10).md">JetOpenTempTable</a></td>
<td>Crea una tabla temporal con un índice único. Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex. Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil. También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial. Vea también <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292232(v=exchg.10).md">JetOpenTempTable2</a></td>
<td>Crea una tabla temporal con un índice único. Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex. Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil. También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial. Vea también <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292233(v=exchg.10).md">JetOpenTempTable3</a></td>
<td>Crea una tabla temporal con un índice único. Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex. Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil. También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial. Vea también <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332998(v=exchg.10).md">JetOSSnapshotFreeze</a></td>
<td>Inicia una instantánea. Mientras la instantánea está en curso, no se puede llevar a cabo ninguna actividad de escritura en disco por parte del motor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn292235(v=exchg.10).md">JetOSSnapshotPrepare</a></td>
<td>Comienza los preparativos para una sesión de instantánea. Una sesión de instantáneas es un breve intervalo de tiempo en el que el motor no emite ninguna e/s de escritura en el disco, de modo que el motor puede participar en una sesión de instantáneas de volumen (cuando está controlada por un escritor de instantáneas).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332986(v=exchg.10).md">JetOSSnapshotThaw</a></td>
<td>Notifica al motor de que puede reanudar las operaciones de e/s normales después de un período de inmovilización y una instantánea correcta.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332988(v=exchg.10).md">JetPrepareUpdate</a></td>
<td>Preparar un cursor para la actualización.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332987(v=exchg.10).md">JetReadFileInstance</a></td>
<td>Recupera el contenido de un archivo abierto con <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332989(v=exchg.10).md">JetRegisterCallback</a></td>
<td>Permite a la aplicación configurar el motor de base de datos para emitir notificaciones a la aplicación para eventos concretos. Estas notificaciones están asociadas a una tabla específica y permanecen en vigor solo hasta que se cierra la instancia que contiene la tabla mediante <a href="dn334020(v=exchg.10).md">JetTerm (JET_INSTANCE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332990(v=exchg.10).md">JetRenameColumn</a></td>
<td>Cambia el nombre de una columna existente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332993(v=exchg.10).md">JetRenameTable</a></td>
<td>Cambia el nombre de una tabla existente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332991(v=exchg.10).md">JetResetSessionContext</a></td>
<td>Desasocia una sesión del subproceso actual. Debe usarse junto con <a href="dn334027(v=exchg.10).md">JetSetSessionContext (JET_SESID, IntPtr)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332994(v=exchg.10).md">JetResetTableSequential</a></td>
<td>Notifica al motor de base de datos que la aplicación ya no está examinando el índice completo en el que está situado el cursor. Esta llamada invierte una notificación enviada por <a href="dn334018(v=exchg.10).md">JetSetTableSequential (JET_SESID, JET_TABLEID, SetTableSequentialGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332992(v=exchg.10).md">JetRestoreInstance</a></td>
<td>Restaura y recupera una copia de seguridad de streaming de una instancia de, incluidas todas las bases de datos adjuntas. Está diseñado para trabajar con una copia de seguridad creada con la función <a href="dn292102(v=exchg.10).md">JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)</a> . Esta es la función de restauración más sencilla y encapsulada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332995(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor. Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor. Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual. Además de recuperar el valor de la columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn332997(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor. Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor. Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual. Además de recuperar el valor de la columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334004(v=exchg.10).md">JetRetrieveColumns</a></td>
<td>Recupera varios valores de columna del registro actual en una sola operación. Una matriz de estructuras JET_RETRIEVECOLUMN se utiliza para describir el conjunto de valores de columna que se va a recuperar y para describir los búferes de salida de cada valor de columna que se va a recuperar.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334002(v=exchg.10).md">JetRetrieveKey</a></td>
<td>Recupera la clave de la entrada de índice en la posición actual de un cursor. Vea también <a href="dn334085(v=exchg.10).md">RetrieveKey (JET_SESID, JET_TABLEID, RetrieveKeyGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334001(v=exchg.10).md">JetRollback</a></td>
<td>Deshace los cambios realizados en el estado de la base de datos y vuelve al último punto de almacenamiento. JetRollback también cerrará los cursores abiertos durante el punto de almacenamiento. Si el punto de almacenamiento más externo se deshace, la sesión finalizará la transacción.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334003(v=exchg.10).md">JetSeek</a></td>
<td>Coloca de forma eficaz un cursor en una entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada. Una clave de búsqueda se debe haber construido previamente mediante <a href="dn292216(v=exchg.10).md">JetMakeKey (JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>. Vea también <a href="dn334145(v=exchg.10).md">TrySeek (JET_SESID, JET_TABLEID, SeekGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334009(v=exchg.10).md">JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, SetColumnGrbit, JET_SETINFO)</a></td>
<td>La función JetSetColumn modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual. Puede sobrescribir un valor existente, agregar un nuevo valor a una secuencia de valores en una columna con varios valores, quitar un valor de una secuencia de valores de una columna con varios valores o actualizar todo o parte de un valor Long (una columna de tipo <a href="hh577895(v=exchg.10).md">LongText</a> o <a href="hh577895(v=exchg.10).md">LongBinary</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334008(v=exchg.10).md">JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, SetColumnGrbit, JET_SETINFO)</a></td>
<td>La función JetSetColumn modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual. Puede sobrescribir un valor existente, agregar un nuevo valor a una secuencia de valores en una columna con varios valores, quitar un valor de una secuencia de valores de una columna con varios valores o actualizar todo o parte de un valor Long (una columna de tipo <a href="hh577895(v=exchg.10).md">LongText</a> o <a href="hh577895(v=exchg.10).md">LongBinary</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334010(v=exchg.10).md">JetSetColumnDefaultValue</a></td>
<td>Cambia el valor predeterminado de una columna existente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334006(v=exchg.10).md">JetSetColumns</a></td>
<td>Permite que una aplicación establezca varios valores de columna en una sola operación. Una matriz de estructuras <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a> se utiliza para describir el conjunto de valores de columna que se va a establecer y para describir los búferes de entrada de cada valor de columna que se va a establecer.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334011(v=exchg.10).md">JetSetCurrentIndex</a></td>
<td>Establece el índice actual de un cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334005(v=exchg.10).md">JetSetCurrentIndex2</a></td>
<td>Establece el índice actual de un cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334012(v=exchg.10).md">JetSetCurrentIndex3</a></td>
<td>Establece el índice actual de un cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334013(v=exchg.10).md">JetSetCurrentIndex4</a></td>
<td>Establece el índice actual de un cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334014(v=exchg.10).md">JetSetDatabaseSize</a></td>
<td>Establece el tamaño de un archivo de base de datos no abierto.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334024(v=exchg.10).md">JetSetIndexRange</a></td>
<td>Limita temporalmente el conjunto de entradas de índice que el cursor puede recorrer usando <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a> a las que comienzan en la entrada de índice actual y terminan en la entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y los criterios enlazados especificados. Una clave de búsqueda se debe haber construido previamente mediante <a href="dn292216(v=exchg.10).md">JetMakeKey (JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>. Vea también <a href="dn334099(v=exchg.10).md">TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334015(v=exchg.10).md">JetSetLS</a></td>
<td>Permite a la aplicación asociar un identificador de contexto conocido como almacenamiento local con un cursor o la tabla asociada a ese cursor. La aplicación puede usar este identificador de contexto para almacenar datos auxiliares que están asociados a un cursor o una tabla. Posteriormente, la aplicación recibe una notificación mediante una devolución de llamada en tiempo de ejecución cuando se debe liberar el identificador de contexto. Esto hace posible asociar el estado asignado dinámicamente a un cursor o una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334027(v=exchg.10).md">JetSetSessionContext</a></td>
<td>Asocia una sesión al subproceso actual utilizando el identificador de contexto especificado. Esta asociación invalida el requisito de motor predeterminado que una transacción para una sesión determinada debe aparecer completamente en el mismo subproceso. Use <a href="dn332991(v=exchg.10).md">JetResetSessionContext (JET_SESID)</a> para quitar la asociación.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334028(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, cadena)</a></td>
<td>Establece las opciones de configuración de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334017(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String)</a></td>
<td>Establece las opciones de configuración de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334029(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)</a></td>
<td>Establece las opciones de configuración de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334018(v=exchg.10).md">JetSetTableSequential</a></td>
<td>Notifica al motor de base de datos que la aplicación está examinando el índice completo en el que está situado el cursor. Por lo tanto, los métodos que se usan para tener acceso a los datos del índice se optimizarán para que este escenario sea lo más rápido posible. Vea también <a href="dn332994(v=exchg.10).md">JetResetTableSequential (JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334032(v=exchg.10).md">JetStopBackupInstance</a></td>
<td>Impide que la actividad relacionada con la copia de seguridad de secuencias continúe en una instancia en ejecución específica, con lo que finaliza la copia de seguridad de streaming de una manera predecible.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334035(v=exchg.10).md">JetStopServiceInstance</a></td>
<td>Prepara una instancia para la terminación.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334020(v=exchg.10).md">JetTerm</a></td>
<td>Finalice una instancia creada con <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> o <a href="dn292122(v=exchg.10).md">JetCreateInstance JET_INSTANCE (cadena)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334037(v=exchg.10).md">JetTerm2</a></td>
<td>Finalice una instancia creada con <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> o <a href="dn292122(v=exchg.10).md">JetCreateInstance JET_INSTANCE (cadena)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334022(v=exchg.10).md">JetTruncateLogInstance</a></td>
<td>Se usa durante una copia de seguridad iniciada por JetBeginExternalBackup para eliminar los archivos de registro de transacciones que ya no se necesitarán una vez que la copia de seguridad actual se complete correctamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334019(v=exchg.10).md">JetUnregisterCallback</a></td>
<td>Configura el motor de base de datos para detener la emisión de notificaciones a la aplicación como se solicitó previamente a través de <a href="dn332989(v=exchg.10).md">JetRegisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334036(v=exchg.10).md">JetUpdate (JET_SESID, JET_TABLEID)</a></td>
<td>La función JetUpdate realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente. La eliminación de una fila de tabla se realiza mediante una llamada a <a href="dn292131(v=exchg.10).md">JetDelete (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334023(v=exchg.10).md">JetUpdate (JET_SESID, JET_TABLEID, [], Int32, Int32)</a></td>
<td>La función JetUpdate realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente. La eliminación de una fila de tabla se realiza mediante una llamada a <a href="dn292131(v=exchg.10).md">JetDelete (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334042(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Boolean, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334026(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, byte, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334044(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, [], MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334025(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334046(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Double, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334030(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, GUID, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334048(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Int16, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334031(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334050(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Int64, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334033(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, single, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334052(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334054(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334034(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334038(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, cadena, codificación, MakeKeyGrbit)</a></td>
<td>Construye una clave de búsqueda que puede usar <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> y <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334058(v=exchg.10).md">MoveAfterLast</a></td>
<td>Coloca el cursor después del último registro de la tabla. Un movimiento anterior posterior colocará el cursor en el último registro.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334057(v=exchg.10).md">MoveBeforeFirst</a></td>
<td>Coloca el cursor delante del primer registro de la tabla. El siguiente movimiento posterior colocará el cursor en el primer registro.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334040(v=exchg.10).md">ResetIndexRange</a></td>
<td>Quita un intervalo de índice creado con <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a> o <a href="dn334099(v=exchg.10).md">TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>. Si no hay ningún intervalo de índice presente, este método no hace nada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor. Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor. Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual. Además de recuperar el valor de la columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334045(v=exchg.10).md">RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de columna booleano del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334078(v=exchg.10).md">RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna booleano del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334047(v=exchg.10).md">RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de columna de bytes del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334074(v=exchg.10).md">RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna de bytes del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334077(v=exchg.10).md">RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de columna DateTime del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334051(v=exchg.10).md">RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna DateTime del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334053(v=exchg.10).md">RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de columna doble del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334084(v=exchg.10).md">RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna doble del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334056(v=exchg.10).md">RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de columna Float del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334092(v=exchg.10).md">RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna Float del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334093(v=exchg.10).md">RetrieveColumnAsGuid (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de columna GUID del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334061(v=exchg.10).md">RetrieveColumnAsGuid (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna GUID del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334062(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334098(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna Int16 del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334100(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334068(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna Int32 del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334066(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334091(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334067(v=exchg.10).md">RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor. Se usa la codificación Unicode.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334103(v=exchg.10).md">RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificación)</a></td>
<td>Recupera un valor de columna de cadena del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334070(v=exchg.10).md">RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificación, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna de cadena del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334069(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de columna UInt16 del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334106(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna UInt16 del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334108(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de columna UInt32 del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334073(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna UInt32 del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334072(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de columna UInt64 del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334113(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valor de columna UInt64 del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334075(v=exchg.10).md">RetrieveColumns</a></td>
<td>Recupera columnas en objetos ColumnValue.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334076(v=exchg.10).md">RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera el tamaño de un valor de columna único del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor. Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor. Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334117(v=exchg.10).md">RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</a></td>
<td>Recupera el tamaño de un valor de columna único del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor. Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor. Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334085(v=exchg.10).md">RetrieveKey</a></td>
<td>Recupera la clave de la entrada de índice en la posición actual de un cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334120(v=exchg.10).md">SerializeObjectToColumn</a></td>
<td>Escribir un formulario serializado de un objeto en una columna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334123(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, booleano)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334080(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334121(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [])</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334082(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334125(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334081(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, GUID)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334127(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334083(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334130(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334087(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, single)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334132(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334086(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334135(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334089(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], SetColumnGrbit)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334136(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, cadena, codificación)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334090(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, cadena, codificación, SetColumnGrbit)</a></td>
<td>Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334138(v=exchg.10).md">SetColumns</a></td>
<td>Establece las columnas de los objetos ColumnValue.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334139(v=exchg.10).md">TryGetLock</a></td>
<td>Reserve explícitamente la capacidad de actualizar una fila, un bloqueo de escritura o impedir explícitamente que una fila se actualice en cualquier otra sesión, bloqueo de lectura. Normalmente, los bloqueos de escritura de filas se adquieren implícitamente como resultado de la actualización de filas. Normalmente, los bloqueos de lectura no son necesarios debido a las versiones de registros. Sin embargo, en algunos casos, una transacción puede desear bloquear explícitamente una fila para aplicar la serialización o asegurarse de que una operación posterior se realizará correctamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334094(v=exchg.10).md">TryMove</a></td>
<td>Intente desplazarse por un índice. Si la navegación se realiza correctamente, este método devuelve true. Si no hay ningún registro para navegar a este método, devuelve false; se producirá una excepción para otros errores.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334150(v=exchg.10).md">TryMoveFirst</a></td>
<td>Intente moverse al primer registro de la tabla. Si la tabla está vacía, devuelve false, si se produce un error diferente, se inicia una excepción.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334140(v=exchg.10).md">TryMoveLast</a></td>
<td>Intente moverse al último registro de la tabla. Si la tabla está vacía, devuelve false, si se produce un error diferente, se inicia una excepción.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334095(v=exchg.10).md">TryMoveNext</a></td>
<td>Intente moverse al siguiente registro de la tabla. Si no hay un registro siguiente, devuelve false, si se produce un error diferente, se produce una excepción.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334144(v=exchg.10).md">TryMovePrevious</a></td>
<td>Intente moverse al registro anterior de la tabla. Si no hay un registro anterior, devolverá FALSE si se produce un error diferente al producirse una excepción.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334096(v=exchg.10).md">TryOpenTable</a></td>
<td>Intente abrir una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334145(v=exchg.10).md">TrySeek</a></td>
<td>Coloca de forma eficaz un cursor en una entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada. Una clave de búsqueda se debe haber construido previamente mediante JetMakeKey.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334099(v=exchg.10).md">TrySetIndexRange</a></td>
<td>Limita temporalmente el conjunto de entradas de índice que el cursor puede recorrer usando JetMove para que empiecen a partir de la entrada de índice actual y terminen en la entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y los criterios enlazados especificados. Una clave de búsqueda se debe haber construido previamente mediante JetMakeKey. Devuelve true si el intervalo de índice no está vacío; en caso contrario, false.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
