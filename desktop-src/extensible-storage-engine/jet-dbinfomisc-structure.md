---
description: 'Más información sobre: JET_DBINFOMISC structure'
title: Estructura de JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c7684fe69cff252d75ea2cceb0872044e8a011b39e88375d6eb576cb1b5360e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118486338"
---
# <a name="jet_dbinfomisc-structure"></a>Estructura de JET_DBINFOMISC


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_dbinfomisc-structure"></a>Estructura de JET_DBINFOMISC

La **JET_DBINFOMISC** contiene información diversa sobre una base de datos. Esta es la información contenida en el encabezado de base de datos.

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
    } JET_DBINFOMISC;
```

### <a name="members"></a>Miembros

**ulVersion**

Versión nativa del motor de base de datos que creó la base de datos. Consulte [JetGetVersion para](./jetgetversion-function.md) recuperar la versión nativa del motor de base de datos actual.

**ulUpdate**

Realiza un seguimiento de las actualizaciones de formato de base de datos incrementales compatibles con versiones anteriores.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ulVersion, ulUpdate =</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x620,0</p></td>
<td><p>Formato beta del sistema operativo original (22/4/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620,1</p></td>
<td><p>Agregue columnas al catálogo para la indexación condicional y OLD (29/5/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,2</p></td>
<td><p>Agregue la marca fLocalizedText en IDB (5/6/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620,3</p></td>
<td><p>Agregue SPLIT_BUFFER a las páginas raíz del árbol de espacio (30/10/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,2</p></td>
<td><p>Revierta la revisión para que ESE97 siga siendo compatible con el avance (28/1/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620,3</p></td>
<td><p>Agregue nuevas columnas etiquetadas al catálogo ( &quot; CallbackData &quot; y &quot; CallbackDependencies &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,4</p></td>
<td><p>Compatibilidad con SLV: signSLV, fSLVExists en el encabezado db (5/5/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620,5</p></td>
<td><p>Nuevo árbol de espacio SLV (29/5/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,6</p></td>
<td><p>Mapa de espacio SLV (12/10/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620,7</p></td>
<td><p>IDXSEG de 4 bytes (10/12/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,8</p></td>
<td><p>Nuevo formato de columna de plantilla (25/1/99).</p></td>
</tr>
<tr class="even">
<td><p>0x620,9</p></td>
<td><p>Columnas de plantilla ordenadas (24/6/99).</p></td>
</tr>
<tr class="odd">
<td><p>0x623,0</p></td>
<td><p>Nuevo administrador de espacios (15/5/99).</p></td>
</tr>
</tbody>
</table>


**signDb**

Firma de la base de datos (incluida la hora de creación). Esta estructura es de 28 bytes.

**dbstate**

Este es el estado de la base de datos.

Las siguientes opciones están disponibles para este miembro.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_dbstateJustCreated<br />
1</p></td>
<td><p>La base de datos se acaba de crear.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateDirtyShutdown<br />
2</p></td>
<td><p>La base de datos requiere que se ejecute una recuperación de forma dura o flexible para poder usarse o moverse. No se debe intentar mover las bases de datos en este estado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateCleanShutdown<br />
3</p></td>
<td><p>La base de datos está en un estado limpio. La base de datos se puede adjuntar sin archivos de registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateBeingConverted<br />
4</p></td>
<td><p>La base de datos se está actualizando.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateForceDetach<br />
5</p></td>
<td><p>Interno.</p></td>
</tr>
</tbody>
</table>


**lgposConsistent**

Null si la base de datos está en un estado desdeso. Esta es la posición del registro que se usó cuando la base de datos se hizo por última vez en un estado de apagado limpio.

**logtimeConsistent**

Null si la base de datos está en un estado desdeso. Esta es la hora en que la base de datos se hizo por última vez en un estado de apagado limpio.

**logtimeAttach**

Hora en que la base de datos se agregó por última vez [con JetAttachDatabase](./jetattachdatabase-function.md).

**lgposAttach**

Posición del registro que se usó la última vez que se adjuntaba la base de datos [con JetAttachDatabase](./jetattachdatabase-function.md).

**logtimeDetach**

Hora en que la base de datos se desasocia por última vez [con JetDetachDatabase](./jetdetachdatabase-function.md).

**lgposDetach**

Posición del registro que se usó la última vez que la base de datos se desasociaba [con JetDetachDatabase](./jetdetachdatabase-function.md).

**signLog**

Admite la infraestructura ese y no se puede usar en el código.

**bkinfoFullPrev**

Admite la infraestructura ese y no se puede usar en el código.

**bkinfoIncPrev**

Admite la infraestructura ese y no se puede usar en el código.

**bkinfoFullCur**

Admite la infraestructura ese y no se puede usar en el código.

**fShadowingDisabled**

Admite la infraestructura ese y no se puede usar en el código.

**fUpgradeDb**

Admite la infraestructura ese y no se puede usar en el código.

**dwMajorVersion**

Representa los números Windows versión de NT cuando se actualizaron los índices de las bases de datos. Se usa para actualizar índices.

**dwMinorVersion**

Representa los números Windows versión de NT cuando se actualizaron los índices de las bases de datos. Se usa para actualizar índices.

**dwBuildNumber**

Representa los números Windows versión de NT cuando se actualizaron los índices de las bases de datos. Se usa para actualizar índices.

**lSPNumber**

Representa los números Windows versión de NT cuando se actualizaron los índices de las bases de datos. Se usa para actualizar índices.

**cbPageSize**

Tamaño de página de la base de datos. 0 significa que el tamaño de página es de 4 KB.

Este valor solo se recupera si JET_DbInfoMisc a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo.](./jetgetdatabasefileinfo-function.md)

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
