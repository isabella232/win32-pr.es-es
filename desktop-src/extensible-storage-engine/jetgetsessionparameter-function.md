---
description: 'Más información sobre: JetGetSessionParameter (Función)'
title: JetGetSessionParameter (Función)
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7953c2359d651d1bb6c9d5a006c02d9b19de6662
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477921"
---
# <a name="jetgetsessionparameter-function"></a>JetGetSessionParameter (Función)


_**Se aplica a:** Windows | Windows Servidor_

La **función JetGetSessionParameter** lee el parámetro de sesión de la sesión determinada.

La **función JetGetSessionParameter** se introdujo en el Windows 8 operativo.

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

Cuando se especifica, se omite la instancia especificada y se usa la instancia asociada a la sesión.

*sesparamid*

Identificador del parámetro de sesión que se establecerá.

*pvParam*

Datos de este parámetro de sesión.

*cbParamMax*

Tamaño máximo del conjunto de datos en este parámetro de sesión.

*pwParamActual*

Tamaño real del conjunto de datos en este parámetro de sesión.

### <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, el búfer de salida adecuado para el parámetro de sesión solicitado se establecerá en el valor de ese parámetro de sesión.

En caso de error, el estado de los búferes de salida será indefinido.

#### <a name="remarks"></a>Comentarios

El parámetro session se usa durante la duración de la sesión o hasta que se restablece el valor.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
