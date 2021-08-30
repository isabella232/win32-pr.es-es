---
description: 'Más información sobre: JET_INDEXLIST miembros'
title: JET_INDEXLIST miembros
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b4ced7a9ffe60d2d8ce16c0e78574e96475f00ec5b6877a6bfea04ef2bd142e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017225"
---
# <a name="jet_indexlist-members"></a>JET_INDEXLIST miembros

Incluir miembros protegidos  
Incluir miembros heredados  

Información sobre una tabla temporal que contiene información sobre todos los índices de una tabla determinada.

El [JET_INDEXLIST](./jet-indexlist-class.md) expone los miembros siguientes.

## <a name="constructors"></a>Constructores

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></td>
<td></td>
</tr>
</tbody>
</table>


Superior

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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335125(v=exchg.10).md">columnidcColumn</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el número de columnas en la clave de índice. La columna es de tipo <a href="hh577895(v=exchg.10).md">Long.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335126(v=exchg.10).md">columnidcEntry</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el número de entradas en el índice. Este valor no es actual y solo lo actualiza &quot; Api.JetComputeStats. &quot; La columna es de tipo <a href="hh577895(v=exchg.10).md">Long.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335127(v=exchg.10).md">columnidcKey</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el número de claves únicas en el índice. Este valor no es actual y solo lo actualiza &quot; Api.JetComputeStats. &quot; La columna es de tipo <a href="hh577895(v=exchg.10).md">Long.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el tipo de columna de la columna que se va a indexar. La columna es de tipo <a href="hh577895(v=exchg.10).md">Long.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el columnid de la columna que se va a indexar. La columna es de tipo <a href="hh577895(v=exchg.10).md">Long.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el grbit que se aplica a la columna indizada. Vea <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>. La columna es de tipo <a href="hh577895(v=exchg.10).md">Text</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335168(v=exchg.10).md">columnidCp</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena la página de códigos de la columna indizada. La columna es de tipo <a href="hh577895(v=exchg.10).md">Short.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335136(v=exchg.10).md">columnidcPage</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el número de páginas del índice. Este valor no es actual y solo lo actualiza &quot; Api.JetComputeStats. &quot; La columna es de tipo <a href="hh577895(v=exchg.10).md">Long.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el grbit que se aplica a la columna indizada. Vea <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>. La columna es de tipo <a href="hh577895(v=exchg.10).md">Long.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena los bits grbits usados en el índice. Vea <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>. La columna es de tipo <a href="hh577895(v=exchg.10).md">Long.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335170(v=exchg.10).md">columnidiColumn</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el índice de esta columna en la clave de índice. La columna es de tipo <a href="hh577895(v=exchg.10).md">Long.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335138(v=exchg.10).md">columnidindexname</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el nombre del índice. La columna es de tipo <a href="hh577895(v=exchg.10).md">Text</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335171(v=exchg.10).md">columnidLangid</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena el identificador de idioma (LCID) del índice. La columna es de tipo <a href="hh577895(v=exchg.10).md">Short.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></td>
<td>Obtiene el columnid de la columna de la tabla temporal que almacena las marcas de normalización Unicode para el índice. La columna es de tipo <a href="hh577895(v=exchg.10).md">Long.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335173(v=exchg.10).md">cRecord</a></td>
<td>Obtiene el número de registros de la tabla temporal.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335174(v=exchg.10).md">tableid</a></td>
<td>Obtiene el tableid de la tabla temporal. Debe cerrarse cuando la tabla ya no sea necesaria.</td>
</tr>
</tbody>
</table>


Superior

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">Gettype</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335165(v=exchg.10).md">ToString</a></td>
<td>Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el objeto <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>. (Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_INDEXLIST clase](./jet-indexlist-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
