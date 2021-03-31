---
description: 'Más información acerca de: estructura de JET_RSTMAP'
title: Estructura de JET_RSTMAP
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809067"
---
# <a name="jet_rstmap-structure"></a>Estructura de JET_RSTMAP


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_rstmap-structure"></a>Estructura de JET_RSTMAP

La estructura **JET_RSTMAP** habilita la reasignación de las rutas de acceso de archivos de base de datos que se almacenan en los registros de transacciones durante la recuperación, cuando las funciones [JetInit](./jetinit-function.md) y [JetExternalRestore](./jetexternalrestore-function.md) las utilizan. Esto permite que las bases de datos se muevan cuando estén sin conexión o cuando se restauren desde la copia de seguridad.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Miembros

**szDatabaseName**

La ruta de acceso absoluta actual de una base de datos que está asociada a los registros de transacciones que se reproducen durante la recuperación.

**szNewDatabaseName**

Nueva ruta de acceso absoluta para la base de datos.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_RSTMAP_W</strong> (Unicode) y <strong>JET_RSTMAP_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
