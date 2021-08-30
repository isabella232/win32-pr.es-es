---
description: 'Más información sobre: JetGetSystemParameter (Función)'
title: JetGetSystemParameter (Función)
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4cdb8769ff05dde61df13d07564a1e0467fa8897
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474081"
---
# <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter (Función)

La **función JetGetSystemParameter** lee las numerosas opciones de configuración del motor de base de datos.

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia de que se va a usar para esta llamada.

Para Windows 2000, este parámetro se omite y siempre debe ser **NULL.**

Para Windows XP y versiones posteriores, este parámetro está algo sobrecargado. Si el motor funciona en modo heredado (Windows modo de compatibilidad 2000) donde solo se admite una instancia, este parámetro puede ser **NULL** o puede contener la instancia real devuelta por [JetInit](./jetinit-function.md). En cualquier caso, toda la configuración de parámetros del sistema se lee de esa instancia. Si el motor funciona en modo de varias instancias, este parámetro puede ser **NULL** o un puntero a una instancia creada mediante [JetInit](./jetinit-function.md) o [JetCreateInstance.](./jetcreateinstance-function.md) Cuando este parámetro es **NULL,** se lee la configuración global del parámetro del sistema (o el valor predeterminado). Cuando este parámetro es una instancia de , se lee la configuración del parámetro del sistema para esa instancia.

*sesid*

Sesión que se va a usar para esta llamada.

Cuando se especifica, se omite la instancia especificada y se usará la instancia asociada a la sesión.

*paramid*

Identificador del parámetro del sistema que se leerá.

Consulte [Parámetros del sistema](./extensible-storage-engine-system-parameters.md) para obtener una lista completa de los parámetros del sistema y sus propiedades.

*plParam*

Búfer de salida que recibe el valor del parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo entero.

*szParam*

Búfer de salida que recibe el valor del parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo de cadena.

*cbMax*

Tamaño máximo en bytes del búfer de salida de cadena.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInitInProgress</p> | <p>No es posible completar la operación porque se está inicializando la instancia asociada a la sesión.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro.</p><p>Esto puede ocurrir para <strong>JetGetSystemParameter</strong> cuando:</p><ul><li><p>El identificador de parámetro del sistema especificado no es válido o no se admite.</p></li><li><p>El parámetro del sistema especificado requiere que se especifique el búfer de salida entero y que el puntero del búfer de salida sea <strong>NULL.</strong></p></li><li><p>El parámetro del sistema especificado requiere que se especifique un búfer de salida de cadena y que el puntero del búfer de salida sea <strong>NULL.</strong></p><p><strong>Windows Vista:</strong> Esto solo puede ocurrir en Windows Vista y versiones posteriores.</p></li><li><p>El parámetro del sistema especificado requiere que se proporciona un búfer de salida de cadena y el tamaño de ese búfer de salida es demasiado pequeño para aceptar una cadena terminada en NULL.</p><p><strong>Windows Vista:</strong> Esto solo puede ocurrir en Windows Vista y versiones posteriores.</p></li><li><p>No se puede leer el parámetro del sistema especificado porque es de solo escritura.</p></li><li><p>El parámetro del sistema especificado es solo global y se intentó leer un valor específico de instancia para ese parámetro del sistema. Esto solo puede ocurrir en Windows XP y versiones posteriores.</p></li><li><p>El parámetro del sistema especificado es solo por instancia y se intentó leer el valor global de ese parámetro del sistema. Esto solo puede ocurrir en Windows XP y versiones posteriores.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errInvalidSesid</p> | <p>El identificador de sesión no es válido o hace referencia a una sesión cerrada. Este error no se devuelve en todas las circunstancias. Los identificadores solo se validan con el mejor esfuerzo.</p> | 
| <p>JET_errInvalidInstance</p> | <p>El identificador de instancia no es válido o hace referencia a una instancia que se ha apagado. Este error no se devuelve en todas las circunstancias. Los identificadores solo se validan con el mejor esfuerzo.</p><p><strong>Windows Vista:</strong> Este error solo lo devolverán Windows Vista y versiones posteriores.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir toda la configuración de parámetros del sistema.</p><p>El búfer de salida se ha rellenado con la mayor parte de la configuración de parámetros del sistema que cabría. Si el búfer de salida tiene al menos un carácter de longitud, la cadena de ese búfer de salida finalizará en null.</p><p><strong>Nota  </strong> Este error no lo devuelven todas las versiones. Consulte la sección Comentarios para obtener más información.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Error en la operación porque el búfer de salida era demasiado pequeño para recibir toda la configuración de parámetros del sistema.</p><p><strong>Nota  </strong> Este error no se devuelve en algunos casos para conservar la compatibilidad de la aplicación. Consulte la sección Comentarios para obtener más información.</p><p><strong>Windows Vista:</strong> Este error solo lo devolverán Windows Vista y versiones posteriores.</p> | 



Si se ejecuta correctamente, el búfer de salida adecuado para el parámetro del sistema solicitado se establecerá en el valor de ese parámetro del sistema.

En caso de error, el estado de los búferes de salida será indefinido.

#### <a name="remarks"></a>Comentarios

Hay un problema importante en esta API que está presente en todas las versiones. Si se solicita un parámetro del sistema con un valor de cadena y el búfer de salida es demasiado pequeño para recibir toda la configuración de parámetros del sistema, JET_wrnBufferTruncated no se devolverá. JET_errSuccess se devuelve en su lugar. Si la longitud de la cadena devuelta es igual al tamaño del búfer de salida menos el terminador **NULL,** el autor de la llamada debe reaccionar como si se devolvieron JET_wrnBufferTruncated datos. Si se especifica un búfer de salida de cadena de tamaño cero, el autor de la llamada debe reaccionar como si JET_errInvalidParameter se devolvieron.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetGetSystemParameterW</strong> (Unicode) y <strong>JetGetSystemParameterA</strong> (ANSI).</p> | 



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
