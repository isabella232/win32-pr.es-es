---
description: 'Más información sobre: JET_SETSYSPARAM estructura'
title: JET_SETSYSPARAM estructura
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
ms.openlocfilehash: 50ef6d611010a0b1847479a8e6045395d14785a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472691"
---
# <a name="jet_setsysparam-structure"></a>JET_SETSYSPARAM estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_setsysparam-structure"></a>JET_SETSYSPARAM estructura

Una matriz **de JET_SETSYSPARAM** indica un conjunto específico de parámetros globales del sistema que se establecen como argumento al usar la función [JetEnableMultiInstance.](./jetenablemultiinstance-function.md)

**Windows XP:** Esta estructura se introduce en Windows XP.

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

Identificador del parámetro del sistema que se establecerá.

Consulte [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) (Parámetros del sistema del motor de motor extensible) para obtener una lista completa de los parámetros del sistema y sus propiedades.

**lParam**

Valor opcional que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo entero.

**Sz**

Valor opcional que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo de cadena.

**Err**

Error resultante de la llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md) con los parámetros especificados anteriormente.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_ SETSYSPARAM_W</strong> (Unicode) <strong>y JET_ SETSYSPARAM_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[Parámetros extensibles Storage del sistema del motor de base de datos](./extensible-storage-engine-system-parameters.md)  
[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
