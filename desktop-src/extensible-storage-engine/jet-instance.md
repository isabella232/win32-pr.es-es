---
description: 'Más información sobre: JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: c4e80edf41a83f205747c269cad98e4f5175030a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887457"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_instance"></a>JET_INSTANCE

El **JET_INSTANCE** tipo de datos contiene un identificador para la instancia de la base de datos que se usará para una llamada a la API jet.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Tipo de datos

JET_INSTANCE

Null **o** [JET_instanceNil](./invalid-handle-constants.md) se pueden usar para indicar un identificador de instancia no válido.

### <a name="remarks"></a>Observaciones

Este identificador se obtiene cuando se crea una instancia de la base de datos mediante una llamada a las funciones [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2,](./jetcreateinstance2-function.md) [JetInit](./jetinit-function.md)o [JetInit2.](./jetinit2-function.md)

**Windows XP:**  El uso explícito de instancias solo se admite en Windows XP y versiones posteriores.

**Windows 2000:**  Solo se admite una instancia global por proceso.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)
