---
description: 'Más información sobre: JetGetInstanceInfo (Función)'
title: JetGetInstanceInfo (Función)
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4abec75ccb8e444d4689fea65514fea9a6538e8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988578"
---
# <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo (Función)

La **función JetGetInstanceInfo** recupera información sobre las instancias que se están ejecutando.

**Windows XP: JetGetInstanceInfo** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Parámetros

*pcInstanceInfo*

Puntero a un búfer que recibirá el número de elementos almacenados en *paInstanceInfo.*

*paInstanceInfo*

Puntero a un búfer que recibirá la dirección del primer elemento de una matriz de estructuras.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. <strong>JetGetInstanceInfo</strong> devolverá este error cuando:</p><ul><li><p><em>pcInstanceInfo</em> o <em>paInstanceInfo</em> son NULL.</p></li></ul> | 
| <p>JET_errOutOfMemory</p> | <p>No hay memoria suficiente para procesar la solicitud.</p> | 



#### <a name="remarks"></a>Observaciones

El motor de base de datos asignará una matriz de [JET_INSTANCE_INFO](./jet-instance-info-structure.md) estructuras. El autor de la llamada es responsable de liberar esta memoria [con JetFreeBuffer.](./jetfreebuffer-function.md)

Si no hay ninguna instancia activa, **JetGetInstanceInfo** devolverá JET_errSuccess y *pcInstanceInfo* recibirá un valor de 0.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetGetInstanceInfoW</strong> (Unicode) y <strong>JetGetInstanceInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)
