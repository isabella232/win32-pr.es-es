---
description: 'Más información sobre: JET_RSTMAP estructura'
title: JET_RSTMAP estructura
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: e1f3813be8e1ea076a401ce5cdabef3e454b98c1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983588"
---
# <a name="jet_rstmap-structure"></a>JET_RSTMAP estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_rstmap-structure"></a>JET_RSTMAP estructura

La **JET_RSTMAP** permite volver a crear rutas de acceso de archivo de base de datos que se almacenan en los registros de transacciones durante la recuperación, cuando las usan las funciones [JetInit](./jetinit-function.md) y [JetExternalRestore.](./jetexternalrestore-function.md) Esto permite mover las bases de datos cuando están sin conexión o cuando se restauran desde la copia de seguridad.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Miembros

**szDatabaseName**

Ruta de acceso absoluta actual de una base de datos asociada a los registros de transacciones que se reproducen durante la recuperación.

**szNewDatabaseName**

Nueva ruta de acceso absoluta para la base de datos.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_RSTMAP_W</strong> (Unicode) <strong>y JET_RSTMAP_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
