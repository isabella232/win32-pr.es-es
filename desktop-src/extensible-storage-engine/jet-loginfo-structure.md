---
description: 'Más información acerca de: estructura de JET_LOGINFO'
title: Estructura de JET_LOGINFO
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
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
ms.openlocfilehash: b7e643d775d1fb8e0c19286bfb7a50d887644e99
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105698462"
---
# <a name="jet_loginfo-structure"></a>Estructura de JET_LOGINFO


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_loginfo-structure"></a>Estructura de JET_LOGINFO

La estructura **JET_LOGINFO** devuelve información estructurada sobre el conjunto de archivos de registro de transacciones que debe formar parte de un conjunto de archivos de copia de seguridad. La estructura **JET_LOGINFO** es el conjunto mínimo de información necesaria para representar un intervalo de registros que se recupera con [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) o que se especifica para una recuperación de hardware con [JetExternalRestore2](./jetexternalrestore2-function.md).

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a>Miembros

**cbSize**

Tamaño de la estructura, en bytes.

Este miembro permite la expansión futura de esta estructura mientras se habilita la compatibilidad con versiones anteriores. Siempre debe establecerse en sizeof (JET_LOGINFO).

**ulGenLow**

El número de archivo de registro más bajo (o más antiguo) que se restaura. Se debe conservar la fidelidad total de una longitud sin signo, pero en las versiones actuales del motor, este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF. Esto podría cambiar en versiones futuras.

**ulGenHigh**

El número de archivo de registro más alto (o más reciente) que se restaura. Se debe conservar la fidelidad total de una longitud sin signo, pero en las versiones actuales del motor, este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF. Esto podría cambiar en versiones futuras.

**szBaseName**

El prefijo usado para asignar un nombre a los archivos de registro de transacciones.

El valor que se devuelve en este miembro siempre es igual al valor de [JET_paramBaseName](./transaction-log-parameters.md) para la instancia que generó esta información.

### <a name="remarks"></a>Observaciones

Los archivos de registro de transacciones se denominan según el nombre base de la instancia y el número de generación del archivo de registro. El nombre tiene el formato BBBXXXXX. Inicia. BBB corresponde al nombre base del archivo de registro y tiene siempre tres caracteres de longitud. XXXXX corresponde al número de generación del archivo de registro en un valor hexadecimal con ceros rellenado y siempre tiene cinco caracteres de longitud. LOG es la extensión de archivo que el motor siempre proporciona a los archivos de registro de transacciones.

No se recomienda el uso de esta información estructurada porque hace que la aplicación tenga un conocimiento profundo de este esquema de nomenclatura para los archivos de registro de transacciones. Si el esquema de nombres cambia alguna vez en el futuro, este tipo de aplicación dejará de funcionar correctamente. Es imaginable que el formato del registro cambie para incorporar 8 dígitos hexadecimales en el futuro. En su lugar, las aplicaciones deben utilizar la lista explícita de nombres de archivo devueltos por [JetGetLogInfo](./jetgetloginfo-function.md) .

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_LOGINFO_W</strong> (Unicode) y <strong>JET_LOGINFO_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetExternalRestore2](./jetexternalrestore2-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
