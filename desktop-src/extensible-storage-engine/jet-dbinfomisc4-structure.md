---
description: 'Más información acerca de: estructura de JET_DBINFOMISC4'
title: Estructura de JET_DBINFOMISC4
TOCTitle: JET_DBINFOMISC4 Structure
ms:assetid: 63f446bc-98b7-4a60-9575-d6b4757fb0fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269269(v=EXCHG.10)
ms:contentKeyID: 32765571
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
ms.openlocfilehash: 1e2242b1e419c4834a2a1843165e1c9a2ad1f2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686537"
---
# <a name="jet_dbinfomisc4-structure"></a>Estructura de JET_DBINFOMISC4


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_dbinfomisc4-structure"></a>Estructura de JET_DBINFOMISC4

La estructura **JET_DBINFOMISC4** contiene información diversa sobre una base de datos. Esta es la información contenida en el encabezado de la base de datos.

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
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
      JET_BKINFO bkinfoCopyPrev;
      JET_BKINFO bkinfoDiffPrev;
    } JET_DBINFOMISC4;
```

### <a name="members"></a>Miembros

**ulVersion**

Versión nativa del motor de base de datos que creó la base de datos. Vea [JetGetVersion](./jetgetversion-function.md) para recuperar la versión nativa del motor de base de datos actual.

**ulUpdate**

Realiza un seguimiento de las actualizaciones de formato de base de datos incrementales que son compatibles con versiones anteriores

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
<td><p>0x620, 0</p></td>
<td><p>Formato original de la versión beta del sistema operativo (4/22/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 1</p></td>
<td><p>Agregue columnas en el catálogo para la indización condicional y OLD (5/29/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Agregue la marca fLocalizedText en IDB (6/5/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Agregue SPLIT_BUFFER a las páginas raíz del árbol de espacio (10/30/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Revertir revisión para que ESE97 siga siendo compatible con el avance (1/28/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Agregue nuevas columnas etiquetadas al catálogo ( &quot; CallbackData &quot; y &quot; CallbackDependencies &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 4</p></td>
<td><p>Compatibilidad con SLV: signSLV, fSLVExists en el encabezado dB (5/5/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 5</p></td>
<td><p>Nuevo árbol de espacio SLV (5/29/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 6</p></td>
<td><p>Mapa de espacio SLV (10/12/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 7</p></td>
<td><p>IDXSEG de 4 bytes (12/10/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 8</p></td>
<td><p>Nuevo formato de columna de plantilla (1/25/99).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 9</p></td>
<td><p>Columnas de plantilla ordenadas (6/24/99).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, A</p></td>
<td><p>Base de código combinado (3/26/2003).</p></td>
</tr>
<tr class="even">
<td><p>0x620, B</p></td>
<td><p>Nuevo formato de suma de comprobación (1/08/2004).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, C</p></td>
<td><p>Mayor longitud de clave máxima en 1000/2000 bytes para páginas de 4/8 KB (1/15/2004).</p></td>
</tr>
<tr class="even">
<td><p>0x620, D</p></td>
<td><p>Sugerencias de espacio de catálogo, space_header. V2 (7/15/2007).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, E</p></td>
<td><p>Agregue un nuevo formato de nodo/extensión a Space Manager y úselo para grupos de espacio reservados (8/9/2007).</p></td>
</tr>
<tr class="even">
<td><p>0x620, F</p></td>
<td><p>Compresión para valores Long intrínsecos (10/30/2007).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 10</p></td>
<td><p>Compresión para valores Long separados (12/05/2007).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 11</p></td>
<td><p>Nuevo tamaño de fragmento de LV para páginas grandes (12/29/2007).</p></td>
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
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_dbstateJustCreated<br />
1</p></td>
<td><p>Se acaba de crear la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateDirtyShutdown<br />
2</p></td>
<td><p>La base de datos requiere que se ejecute la recuperación de hardware o software para que se pueda usar o mover. No debe intentar trasladar las bases de datos en este estado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateCleanShutdown<br />
3</p></td>
<td><p>La base de datos está en un estado limpio. La base de datos se puede adjuntar sin ningún archivo de registro.</p></td>
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

Es NULL si la base de datos está en un estado sucio. Esta es la posición del registro que se usó cuando la base de datos se realizó por última vez en un estado de cierre correcto.

**logtimeConsistent**

Es NULL si la base de datos está en un estado sucio. Esta es la hora a la que la base de datos se realizó por última vez en un estado de cierre correcto.

**logtimeAttach**

La hora a la que se adjuntó la base de datos por última vez con [JetAttachDatabase](./jetattachdatabase-function.md).

**lgposAttach**

La posición del registro que se usó la última vez que se adjuntó la base de datos con [JetAttachDatabase](./jetattachdatabase-function.md).

**logtimeDetach**

La hora a la que la base de datos se desconectó por última vez con [JetDetachDatabase](./jetdetachdatabase-function.md).

**lgposDetach**

La posición del registro que se usó la última vez que la base de datos se desasoció con [JetDetachDatabase](./jetdetachdatabase-function.md).

**signLog**

Es compatible con la infraestructura de ESE y no se puede usar en el código.

**bkinfoFullPrev**

Es compatible con la infraestructura de ESE y no se puede usar en el código.

**bkinfoIncPrev**

Es compatible con la infraestructura de ESE y no se puede usar en el código.

**bkinfoFullCur**

Es compatible con la infraestructura de ESE y no se puede usar en el código.

**fShadowingDisabled**

Es compatible con la infraestructura de ESE y no se puede usar en el código.

**fUpgradeDb**

Es compatible con la infraestructura de ESE y no se puede usar en el código.

**dwMajorVersion**

Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos. Se utiliza para actualizar los índices.

**dwMinorVersion**

Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos. Se utiliza para actualizar los índices.

**dwBuildNumber**

Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos. Se utiliza para actualizar los índices.

**lSPNumber**

Representa los números de versión de Windows NT cuando se actualizaron los índices de las bases de datos. Se utiliza para actualizar los índices.

**cbPageSize**

Tamaño de página de base de datos. 0 significa que el tamaño de página es 4 KB.

Este valor se recupera solo si JET_DbInfoMisc se pasó a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).

**genMinRequired**

Representa la generación de registro mínima necesaria para reproducir los registros. Esto se utiliza normalmente como la generación de puntos de control.

**genMaxRequired**

Representa la generación de registro máxima necesaria para reproducir los registros.

**logtimeGenMaxCreate**

Representa la fecha y hora de creación del archivo de registro genMax.

**ulRepairCount**

Número de veces que se ha llamado a una reparación en esta base de datos.

**logtimeRepair**

Representa la fecha y hora en que se ejecutó la última reparación.

**ulRepairCountOld**

El número de veces que la reparación se ha ejecutado en esta base de datos antes de la última desfragmentación.

**ulECCFixSuccess**

Número de veces que se corrigió un error de un bit y resultó en una buena página.

**logtimeECCFixSuccess**

Representa la fecha y hora en que se corrigió el último error de bit y resultó en una buena página.

**ulECCFixSuccessOld**

Representa el número de veces que se corrigió un error de un bit y resultó en una buena página antes de la última reparación.

**ulECCFixFail**

Número de veces que se corrigió un error de un bit y resultó en una página incorrecta.

**logtimeECCFixFail**

Representa la fecha y hora en que se corrigió el último error de bit y resultó en una página incorrecta.

**ulECCFixFailOld**

Número de veces que se corrigió un error de un bit y resultó en una página incorrecta antes de la última reparación.

**ulBadChecksum**

Número de veces que se ha encontrado un error de ECC/checksum que no se pudo corregir.

**logtimeBadChecksum**

Representa la fecha y hora en que se encontró el último error de ECC o suma de comprobación que no se pudo corregir.

**ulBadChecksumOld**

Número de veces que se ha encontrado un error de ECC/checksum no corregible antes de la última reparación.

**genCommitted**

Número máximo de generaciones de registro confirmadas en la base de datos. Normalmente, la generación de registros actual.

**bkinfoCopyPrev**

Última copia de seguridad correcta de la copia.

**bkinfoDiffPrev**

La última copia de seguridad diferencial correcta. Este valor se restablece cuando se establece bkinfoFullPrev.

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
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
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
