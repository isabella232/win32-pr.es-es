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
ms.openlocfilehash: 7309d803421d4bf9221ba1d968d5034f940b016f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126962812"
---
# <a name="jet_setsysparam-structure"></a>JET_SETSYSPARAM estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_setsysparam-structure"></a>JET_SETSYSPARAM estructura

Una matriz **de JET_SETSYSPARAM** estructura indica un conjunto específico de parámetros globales del sistema que se establecen como argumento al usar la función [JetEnableMultiInstance.](./jetenablemultiinstance-function.md)

**Windows XP:** Esta estructura se introduce en Windows XP.

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a>Members

**paramid**

Identificador del parámetro del sistema que se establecerá.

Consulte [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) (Parámetros extensibles del sistema del motor de motor de aplicaciones) para obtener una lista completa de los parámetros del sistema y sus propiedades.

**lParam**

Valor opcional que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo entero.

**Sz**

Valor opcional que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo de cadena.

**Err**

Error resultante de la llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md) con los parámetros especificados anteriormente.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_ SETSYSPARAM_W</strong> (Unicode) <strong>y JET_ SETSYSPARAM_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[Parámetros extensibles Storage del sistema del motor de base de datos](./extensible-storage-engine-system-parameters.md)  
[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
