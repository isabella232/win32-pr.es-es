---
description: 'Más información sobre: JET_LOGINFO estructura'
title: JET_LOGINFO estructura
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
ms.openlocfilehash: 8f5619211a5fc76bb080b81b22c08c9e369abf93
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983168"
---
# <a name="jet_loginfo-structure"></a>JET_LOGINFO estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_loginfo-structure"></a>JET_LOGINFO estructura

La **JET_LOGINFO** devuelve información estructurada sobre el conjunto de archivos de registro de transacciones que deben formar parte de un conjunto de archivos de copia de seguridad. La **JET_LOGINFO** estructura es el conjunto mínimo de información necesaria para representar un intervalo de registros que se recupera con [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) o se especifica para una recuperación en disco [con JetExternalRestore2.](./jetexternalrestore2-function.md)

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

Este miembro permite la expansión futura de esta estructura a la vez que se habilita la compatibilidad con versiones anteriores. Siempre debe establecerse en sizeof( JET_LOGINFO ).

**ulGenLow**

Número de archivo de registro más bajo (o más antiguo) que se restaura. Se debe conservar la fidelidad total de un long sin signo, pero en las versiones actuales del motor este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF. Esto puede cambiar en versiones futuras.

**ulGenHigh**

Número de archivo de registro más alto (o más reciente) que se restaura. Se debe conservar la fidelidad total de un long sin signo, pero en las versiones actuales del motor este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF. Esto puede cambiar en versiones futuras.

**szBaseName**

Prefijo utilizado para dar nombre a los archivos de registro de transacciones.

El valor que se devuelve en este miembro siempre es igual al valor de [JET_paramBaseName](./transaction-log-parameters.md) para la instancia que generó esta información.

### <a name="remarks"></a>Observaciones

Los archivos de registro de transacciones se denominan según el nombre base de la instancia y el número de generación del archivo de registro. El nombre tiene el formato BBBXXXXX. REGISTRO. BBB corresponde al nombre base del archivo de registro y siempre tiene tres caracteres de longitud. XXXXX corresponde al número de generación del archivo de registro en hexadecimal cero y siempre tiene cinco caracteres de longitud. LOG es la extensión de archivo que el motor siempre da a los archivos de registro de transacciones.

No se recomienda el uso de esta información estructurada porque hace que la aplicación tenga un conocimiento profundo de este esquema de nomenclatura para los archivos de registro de transacciones. Si el esquema de nomenclatura cambia en el futuro, dicha aplicación ya no funcionará correctamente. Es posible que el formato del registro cambie para incorporar 8 dígitos hexadecimales en el futuro. Las aplicaciones deben usar la lista explícita de nombres de archivo devueltos [por JetGetLogInfo en su](./jetgetloginfo-function.md) lugar.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_LOGINFO_W</strong> (Unicode) <strong>y JET_LOGINFO_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[JetExternalRestore2](./jetexternalrestore2-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
