---
description: 'Más información sobre: estructura JET_DBINFOMISC2 datos'
title: Estructura de JET_DBINFOMISC2
TOCTitle: JET_DBINFOMISC2 Structure
ms:assetid: c62e87ca-c02c-4d6f-a1e6-f80d022c6aad
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294085(v=EXCHG.10)
ms:contentKeyID: 32765700
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da04b1960581c21c29e63d69393de4ebc78dfe7a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985228"
---
# <a name="jet_dbinfomisc2-structure"></a>Estructura de JET_DBINFOMISC2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_dbinfomisc2-structure"></a>Estructura de JET_DBINFOMISC2

La **JET_DBINFOMISC2** contiene información miscelánea sobre una base de datos. Esta es la información contenida en el encabezado de la base de datos.

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
    } JET_DBINFOMISC2;
```

### <a name="members"></a>Miembros

**ulVersion**

Versión nativa del motor de base de datos que creó la base de datos. Consulte [JetGetVersion para](./jetgetversion-function.md) recuperar la versión nativa del motor de base de datos actual.

**ulUpdate**

Realiza un seguimiento de las actualizaciones de formato de base de datos incrementales compatibles con versiones anteriores.


| <p>ulVersion, ulUpdate =</p> | <p>Significado</p> | 
|------------------------------|----------------|
| <p>0x620,0</p> | <p>Formato Beta del sistema operativo original (22/4/97).</p> | 
| <p>0x620,1</p> | <p>Agregue columnas en el catálogo para la indexación condicional y OLD (29/5/97).</p> | 
| <p>0x620,2</p> | <p>Agregue la marca fLocalizedText en IDB (5/6/97).</p> | 
| <p>0x620,3</p> | <p>Agregue SPLIT_BUFFER a las páginas raíz del árbol de espacio (30/10/97).</p> | 
| <p>0x620,2</p> | <p>Revierta la revisión para que ESE97 siga siendo compatible con el futuro (28/1/98).</p> | 
| <p>0x620,3</p> | <p>Agregar nuevas columnas etiquetadas al catálogo ("CallbackData" y "CallbackDependencies").</p> | 
| <p>0x620,4</p> | <p>Compatibilidad con SLV: signSLV, fSLVExists en el encabezado db (5/5/98).</p> | 
| <p>0x620,5</p> | <p>Nuevo árbol de espacio SLV (29/5/98).</p> | 
| <p>0x620,6</p> | <p>Mapa de espacio SLV (12/10/98).</p> | 
| <p>0x620,7</p> | <p>IDXSEG de 4 bytes (12/10/98).</p> | 
| <p>0x620,8</p> | <p>Nuevo formato de columna de plantilla (25/1/99).</p> | 
| <p>0x620,9</p> | <p>Columnas de plantilla ordenadas (24/6/99).</p> | 
| <p>0x620,A</p> | <p>Base de código combinado (26/3/2003).</p> | 
| <p>0x620,B</p> | <p>Nuevo formato de suma de comprobación (08/1/2004).</p> | 
| <p>0x620,C</p> | <p>Se ha aumentado la longitud máxima de clave a 1000/2000 bytes para páginas de 4/8 kb (1/15/2004).</p> | 
| <p>0x620,D</p> | <p>Sugerencias de espacio de catálogo, space_header.v2 (15/7/2007).</p> | 
| <p>0x620,E</p> | <p>Agregue el nuevo formato de nodo o extensión al administrador de espacios y úselo para grupos reservados de espacio (9/8/2007).</p> | 
| <p>0x620,F</p> | <p>Compresión para valores long intrínsecos (30/10/2007).</p> | 
| <p>0x620,10</p> | <p>Compresión para valores largos separados (12/05/2007).</p> | 
| <p>0x620,11</p> | <p>Nuevo tamaño de fragmento de LV para páginas grandes (29/12/2007).</p> | 



**signDb**

Firma de la base de datos (incluida la hora de creación). Esta estructura es de 28 bytes.

**dbstate**

Este es el estado de la base de datos.

Las siguientes opciones están disponibles para este miembro.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_dbstateJustCreated<br />1</p> | <p>La base de datos se acaba de crear.</p> | 
| <p>JET_dbstateDirtyShutdown<br />2</p> | <p>La base de datos requiere que se ejecute una recuperación de forma dura o flexible para poder usarse o moverse. No se deben intentar mover bases de datos en este estado.</p> | 
| <p>JET_dbstateCleanShutdown<br />3</p> | <p>La base de datos está en un estado limpio. La base de datos se puede adjuntar sin archivos de registro.</p> | 
| <p>JET_dbstateBeingConverted<br />4</p> | <p>La base de datos se está actualizando.</p> | 
| <p>JET_dbstateForceDetach<br />5</p> | <p>Interno.</p> | 



**lgposConsistent**

Null si la base de datos se encuentra en un estado de desvía. Esta es la posición del registro que se usó cuando la base de datos se hizo por última vez en un estado de apagado limpio.

**logtimeConsistent**

Null si la base de datos se encuentra en un estado de desvía. Esta es la hora en que la base de datos se hizo por última vez en un estado de apagado limpio.

**logtimeAttach**

Hora a la que se ha adjuntado la base de datos por última vez [con JetAttachDatabase.](./jetattachdatabase-function.md)

**lgposAttach**

Posición del registro que se usó la última vez que se adjunta la base de datos [con JetAttachDatabase](./jetattachdatabase-function.md).

**logtimeDetach**

Hora a la que se desasociaron por última vez la base de datos [con JetDetachDatabase](./jetdetachdatabase-function.md).

**lgposDetach**

Posición del registro que se usó la última vez que la base de datos se [desasocia con JetDetachDatabase](./jetdetachdatabase-function.md).

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

**genMinRequired**

Representa la generación mínima de registros necesaria para reproducir los registros. Esto se usa normalmente como generación de puntos de control.

**genMaxRequired**

Representa la generación máxima de registros necesaria para reproducir los registros.

**logtimeGenMaxCreate**

Representa la fecha y hora de creación del archivo de registro genMax.

**ulRepairCount**

Número de veces que se ha llamado a una reparación en esta base de datos.

**logtimeRepair**

Representa la fecha y hora en que se ha ejecutado la última reparación.

**ulRepairCountOld**

Número de veces que se había ejecutado la reparación en esta base de datos antes de la última desfragmentación.

**ulECCFixSuccess**

Número de veces que se corrigió un error de un bit y dio lugar a una página buena.

**logtimeECCFixSuccess**

Representa la fecha y hora en que se corrigió el último error de un bit y dio lugar a una página buena.

**ulECCFixSuccessOld**

Representa el número de veces que se corrigió un error de un bit y dio lugar a una página buena antes de la última reparación.

**ulECCFixFail**

Número de veces que se corrigió un error de un bit y se produjo una página no buena.

**logtimeECCFixFail**

Representa la fecha y hora en que se corrigió el último error de un bit y dio lugar a una página no activa.

**ulECCFixFailOld**

Número de veces que se corrigió un error de un bit y se produjo una página no buena antes de la última reparación.

**ulBadChecksum**

Número de veces que se encontró un error ecc/suma de comprobación no corregible.

**logtimeBadChecksum**

Representa la fecha y hora en que se encontró el último error de ECC o suma de comprobación no corregible.

**ulBadChecksumOld**

Número de veces que se encontró un error ecc/suma de comprobación no corregible antes de la última reparación.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
