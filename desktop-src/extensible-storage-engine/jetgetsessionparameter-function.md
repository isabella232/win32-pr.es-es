---
description: 'Más información acerca de: JetGetSessionParameter (función)'
title: JetGetSessionParameter función)
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
ms.openlocfilehash: f0ac02142d48009d668d903b39163b425d738b55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907632"
---
# <a name="jetgetsessionparameter-function"></a>JetGetSessionParameter función)


_**Se aplica a:** Windows | Windows Server_

La función **JetGetSessionParameter** lee el parámetro de sesión para la sesión especificada.

La función **JetGetSessionParameter** se presentó en el sistema operativo Windows 8.

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

Cuando se especifica, se omite la instancia especificada y se utilizará la instancia asociada a la sesión.

*sesparamid*

IDENTIFICADOR del parámetro de sesión que se va a establecer.

*pvParam*

Datos de este parámetro de sesión.

*cbParamMax*

Tamaño máximo del conjunto de datos en este parámetro de sesión.

*pcbParamActual*

Tamaño real del conjunto de datos en este parámetro de sesión.

### <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, el búfer de salida adecuado para el parámetro de sesión solicitado se establecerá en el valor de ese parámetro de sesión.

En caso de error, el estado de los búferes de salida será undefined.

#### <a name="remarks"></a>Observaciones

El parámetro Session se usa para la duración de la sesión o hasta que se restablezca el valor.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vea también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
