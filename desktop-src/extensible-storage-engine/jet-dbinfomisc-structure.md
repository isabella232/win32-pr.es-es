---
description: 'Más información sobre: JET_DBINFOMISC estructura'
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
ms.openlocfilehash: 7d7861e558bbf6a1938d252a52e7bb781068a331
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476871"
---
# <a name="jet_dbinfomisc-structure"></a>Estructura de JET_DBINFOMISC


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_dbinfomisc-structure"></a>Estructura de JET_DBINFOMISC

La **JET_DBINFOMISC** contiene información miscelánea sobre una base de datos. Esta es la información contenida en el encabezado de la base de datos.

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
| <p>0x623,0</p> | <p>Nuevo Administrador de espacio (15/5/99).</p> | 



**signDb**

Firma de la base de datos (incluida la hora de creación). Esta estructura es de 28 bytes.

**dbstate**

Este es el estado de la base de datos.

Las siguientes opciones están disponibles para este miembro.


| <p>Valor</p> | <p>Significado</p> | 
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

Hora a la que se adjunta la base de datos por última vez [con JetAttachDatabase](./jetattachdatabase-function.md).

**lgposAttach**

Posición del registro que se usó la última vez que se adjunta la base de datos [con JetAttachDatabase](./jetattachdatabase-function.md).

**logtimeDetach**

Hora a la que se desasociaron por última vez la base de datos [con JetDetachDatabase](./jetdetachdatabase-function.md).

**lgposDetach**

Posición de registro que se usó la última vez que la base de datos se [desasocia con JetDetachDatabase](./jetdetachdatabase-function.md).

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


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
