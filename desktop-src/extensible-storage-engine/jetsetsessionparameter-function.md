---
description: 'Más información sobre: JetSetSessionParameter (Función)'
title: JetSetSessionParameter (Función)
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9451844edc9f55bda75e5ec80e4958b3c474c919
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476361"
---
# <a name="jetsetsessionparameter-function"></a>JetSetSessionParameter (Función)


_**Se aplica a:** Windows | Windows Servidor_

La **función JetSetSessionParameter** configura el motor de base de datos.

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Especifica la sesión que se va a usar para esta llamada.

Cuando se especifica, se omite la instancia especificada y se usa la instancia asociada a la sesión.

*sesparamid*

Identificador del parámetro de sesión que se establecerá.

*pvParam*

Datos que se establecerán en este parámetro de sesión.

*cbParam*

Tamaño de los datos proporcionados.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores extensibles Storage Engine (ESE), vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>La instancia se ha inicializado mediante una llamada a la función <a href="gg294068(v=exchg.10).md">JetInit</a> y esta operación no se puede realizar como resultado. Esto puede ocurrir cuando se intenta configurar un parámetro del sistema después de que un cambio en el valor del parámetro ya no pueda afectar al estado del motor de base de datos.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a la <a href="gg269240(v=exchg.10).md">función JetStopService.</a></p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Los parámetros de índice de tupla especificados no eran ilegales. Este error solo se devuelve cuando el <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>o <em>JET_paramIndexTuplesToIndexMax</em> parámetro está establecido en un valor no válido. Para obtener información sobre estos parámetros, vea <a href="gg294119(v=exchg.10).md">Parámetros de índice</a>.</p> | 
| <p>JET_errInitInProgress</p> | <p>No es posible completar la operación porque se está inicializando la instancia asociada a la sesión.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir cuando ocurre lo siguiente:</p><ul><li><p>El identificador de parámetro del sistema especificado no es válido o no se admite.</p></li><li><p>Se intentó establecer un parámetro del sistema con valores de cadena con una cadena cuya longitud estaba fuera del intervalo legal del parámetro.</p></li><li><p>Se intentó establecer un parámetro del sistema con valores de cadena con una ruta de acceso de archivo donde la longitud de su representación de ruta de acceso absoluta estaba fuera del intervalo legal para ese parámetro.</p></li><li><p>Se intentó establecer un parámetro del sistema con valores enteros con un entero que estaba fuera del intervalo legal del parámetro.</p></li><li><p>Se intentó establecer JET_paramUnicodeIndexDefault con un <a href="gg294097(v=exchg.10).md"></a> puntero JET_UNICODEINDEX null, un LCID no válido o un conjunto no admitido de <strong>marcas LCMapString.</strong></p></li><li><p>No se puede establecer el parámetro del sistema especificado porque es de solo lectura.</p></li><li><p>Se intentó establecer un parámetro del sistema después de llamar a la función <a href="gg294068(v=exchg.10).md">JetInit,</a> el motor de base de datos está en modo de instancia única y no se especificó una sesión.</p></li><li><p>El parámetro del sistema especificado es solo global y se intentó establecer un valor específico de instancia para ese parámetro del sistema.</p></li><li><p>El parámetro del sistema especificado es solo por instancia y se intentó establecer el valor global para ese parámetro del sistema.</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>La ruta de acceso del sistema de archivos especificada no era válida. <strong>JetSetSessionParameter</strong> solo puede devolver este error al establecer parámetros del sistema que representan rutas de acceso del sistema de archivos. Por ejemplo, el <em>JET_paramSystemPath</em> parámetro puede devolver este error. Para obtener información sobre este parámetro, vea <a href="gg269235(v=exchg.10).md">Parámetros del registro de transacciones</a>.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errInvalidSesid</p> | <p>El identificador de sesión no es válido o hace referencia a una sesión cerrada.</p><p>Este error no se devuelve en todas las circunstancias. Los identificadores solo se validan con el mejor esfuerzo.</p> | 
| <p>JET_errInvalidInstance</p> | <p>El identificador de instancia no es válido o hace referencia a una instancia que se ha cerrado.</p><p>Este error no se devuelve en todas las circunstancias. Los identificadores solo se validan con el mejor esfuerzo.</p> | 



Si se ejecuta correctamente, el parámetro del sistema se establecerá en el valor proporcionado.

En caso de error, el valor del parámetro del sistema permanecerá sin cambios.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
