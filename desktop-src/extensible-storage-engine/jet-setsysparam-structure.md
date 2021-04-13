---
description: 'Más información acerca de: estructura de JET_SETSYSPARAM'
title: Estructura de JET_SETSYSPARAM
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360197"
---
# <a name="jet_setsysparam-structure"></a>Estructura de JET_SETSYSPARAM


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_setsysparam-structure"></a>Estructura de JET_SETSYSPARAM

Una matriz de estructuras **JET_SETSYSPARAM** indica un conjunto específico de parámetros globales del sistema que se establecen como argumento cuando se usa la función [JetEnableMultiInstance](./jetenablemultiinstance-function.md) .

**Windows XP:** Esta estructura se ha introducido en Windows XP.

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a>Miembros

**paramid**

IDENTIFICADOR del parámetro del sistema que se va a establecer.

Consulte [parámetros del sistema del motor de almacenamiento extensible](./extensible-storage-engine-system-parameters.md) para obtener una lista completa de parámetros del sistema y sus propiedades.

**lParam**

Valor opcional que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo entero.

**SZ**

Valor opcional que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo de cadena.

**ERR**

El error resultante de la llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md) con los parámetros especificados anteriormente.

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
<td><p>Se implementa como <strong>JET_ SETSYSPARAM_W</strong> (Unicode) y <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[Parámetros del sistema del motor de almacenamiento extensible](./extensible-storage-engine-system-parameters.md)  
[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
