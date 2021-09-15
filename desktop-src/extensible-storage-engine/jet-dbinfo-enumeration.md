---
description: 'Más información sobre: enumeración JET_DbInfo datos'
title: JET_DbInfo enumeración
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39c6c3175c08e4f7644ad4f0b41137e12e84f71d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465625"
---
# <a name="jet_dbinfo-enumeration"></a>JET_DbInfo enumeración

Niveles de información para recuperar la información de la base de datos.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nombre del miembro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Nombre de archivo</td>
<td>Devuelve la ruta de acceso al archivo de base de datos (cadena).</td>
</tr>
<tr class="even">
<td></td>
<td>LCID</td>
<td>Devuelve el identificador de configuración regional (LCID) asociado a esta base de datos (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Opciones</td>
<td>Devuelve un <a href="hh579532(v=exchg.10).md">objeto OpenDatabaseGrbit.</a> Esto indica si la base de datos se abre en modo exclusivo. Si la base de datos está en modo exclusivo, se devolverá <a href="hh579532(v=exchg.10).md">Exclusive;</a> de lo contrario, se devolverá cero. No se devuelven otras opciones de bits grbit de base de datos para JetAttachDatabase y JetOpenDatabase.</td>
</tr>
<tr class="even">
<td></td>
<td>Transacciones</td>
<td>Devuelve un número uno mayor que el nivel máximo en el que se pueden anidar las transacciones. Si se llama a <a href="dn292105(v=exchg.10).md">JetBeginTransaction(JET_SESID)</a> (de forma anidada, es decir, en la misma sesión, sin confirmación ni reversión) tantas veces como este valor, en la última llamada se devolverá <a href="hh564840(v=exchg.10).md">TransTooDeep</a> (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Versión</td>
<td>Devuelve la versión principal del motor de base de datos (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>Tamaño</td>
<td>Devuelve el archivo de la base de datos, en páginas (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceOwned</td>
<td>Devuelve el espacio de propiedad de la base de datos, en páginas (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>Espacio disponible</td>
<td>Devuelve el espacio disponible en la base de datos, en páginas (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Varios</td>
<td>Devuelve un <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> objeto .</td>
</tr>
<tr class="even">
<td></td>
<td>DBInUse</td>
<td>Devuelve un valor booleano que indica si la base de datos está asociada (booleano).</td>
</tr>
<tr class="odd">
<td></td>
<td>PageSize</td>
<td>Devuelve el tamaño de página de la base de datos (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>FileType</td>
<td>Devuelve el tipo de la base de datos (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
