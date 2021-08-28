---
description: 'Más información sobre: JetSetSystemParameter (Función)'
title: JetSetSystemParameter (Función)
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4da3dc4c0d211039378b5cc1301a84e35f67ab24
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475801"
---
# <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter (Función)

La **función JetSetSystemParameter** se usa para establecer los numerosos valores de configuración del motor de base de datos.

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a>Parámetros

*pinstance*

Especifica la instancia que se va a usar para esta llamada.

**Windows 2000:**  Para Windows 2000, este parámetro se omite y siempre debe ser **NULL.**

**Windows XP:**  Para Windows XP y versiones posteriores, este parámetro está algo sobrecargado. Si el motor funciona en modo heredado (modo de compatibilidad Windows 2000) donde solo se admite una instancia, este parámetro puede ser **NULL** o puede contener la instancia real devuelta por [JetInit](./jetinit-function.md). En cualquier caso, toda la configuración de parámetros del sistema se lee de esa instancia. Si el motor funciona en modo de varias instancias, este parámetro puede ser **NULL** o un puntero a una instancia creada mediante [JetInit](./jetinit-function.md) o [JetCreateIndex.](./jetcreateindex-function.md) Cuando este parámetro es **NULL,** se lee la configuración global del parámetro del sistema (o el valor predeterminado). Cuando este parámetro es una instancia de , se lee la configuración del parámetro del sistema para esa instancia.

Aunque técnicamente se trata de un parámetro out, esta API nunca modifica el contenido del búfer proporcionado.

*sesid*

Especifica la sesión que se va a usar para esta llamada.

Cuando se especifica, se omite la instancia especificada y se usará la instancia asociada a la sesión.

*paramid*

Identificador del parámetro del sistema que se establecerá. Consulte [Parámetros del sistema](./extensible-storage-engine-system-parameters.md) para obtener una lista completa de los parámetros del sistema y sus propiedades.

*lParam*

Proporciona el valor que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo entero.

*szParam*

Proporciona el valor del parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo de cadena.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p><p><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores, se puede devolver el valor correcto sin cambiar el valor del parámetro del sistema. Consulte el JET_paramEnableAdvanced del sistema en el tema <a href="gg269346(v=exchg.10).md">Meta Parameters</a> para obtener más información.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>La instancia se ha inicializado mediante una llamada a <a href="gg294068(v=exchg.10).md">JetInit</a> y esta operación no se puede realizar como resultado. Esto puede ocurrir para <strong>JetSetSystemParameter</strong> cuando se intenta configurar un parámetro del sistema después de que un cambio en su valor no pueda afectar al estado del motor de base de datos.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Los parámetros de índice de tupla especificados no eran ilegales. <strong>JetSetSystemParameter</strong> solo puede devolver este error al establecer JET_paramIndexTuplesLengthMin <a href="gg294119(v=exchg.10).md">,</a> <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> en un valor no válido.</p><p><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</p> | 
| <p>JET_errInitInProgress</p> | <p>No es posible completar la operación porque se está inicializando la instancia asociada a la sesión.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetSetSystemParameter</strong> cuando:</p><ul><li><p>El identificador de parámetro del sistema especificado no es válido o no se admite.</p></li><li><p>Se intentó establecer un parámetro del sistema con valores de cadena con una cadena cuya longitud estaba fuera del intervalo legal del parámetro.</p></li><li><p>Se intentó establecer un parámetro del sistema con valores de cadena con una ruta de acceso de archivo donde la longitud de su representación de ruta de acceso absoluta estaba fuera del intervalo legal para ese parámetro.</p><p><strong>Windows Vista:</strong>  Esto solo puede ocurrir en Windows Vista y versiones posteriores.</p></li><li><p>Se intentó establecer un parámetro del sistema con valores enteros con un entero que estaba fuera del intervalo legal del parámetro.</p></li><li><p>Se ha intentado establecer JET_paramUnicodeIndexDefault con <strong></strong><a href="gg294097(v=exchg.10).md"></a> un puntero JET_UNICODEINDEX NULL, un LCID no válido o un conjunto no compatible de marcas LCMapString.</p><p><strong>Windows Vista:</strong>  Esto solo puede ocurrir en Windows Vista y versiones posteriores.</p></li><li><p>No se puede establecer el parámetro del sistema especificado porque es de solo lectura.</p></li><li><p>Se intentó establecer un parámetro del sistema después de llamar a <a href="gg294068(v=exchg.10).md">JetInit,</a> el motor de base de datos está en modo de instancia única y no se especificó una sesión.</p><p><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</p></li><li><p>El parámetro del sistema especificado es solo global y se ha intentado establecer un valor específico de instancia para ese parámetro del sistema.</p><p><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</p></li><li><p>El parámetro del sistema especificado es solo por instancia y se intentó establecer el valor global para ese parámetro del sistema.</p><p><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>La ruta de acceso del sistema de archivos especificada no era válida. <strong>JetSetSystemParameter</strong> solo puede devolver este error al establecer parámetros del sistema que representan rutas de acceso del sistema de archivos. Por ejemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> puede devolver este error.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errInvalidSesid</p> | <p>El identificador de sesión no es válido o hace referencia a una sesión cerrada.</p><p>Este error no se devuelve en todas las circunstancias. Los identificadores solo se validan con el mejor esfuerzo.</p> | 
| <p>JET_errInvalidInstance</p> | <p>El identificador de instancia no es válido o hace referencia a una instancia que se ha apagado.</p><p>Este error no se devuelve en todas las circunstancias. Los identificadores solo se validan con el mejor esfuerzo.</p><p><strong>Windows Vista:</strong>  Este error solo lo devolverán Windows Vista y versiones posteriores.</p> | 



Si se ejecuta correctamente, la configuración del parámetro del sistema se establecerá en el valor proporcionado.

En caso de error, la configuración del parámetro del sistema permanecerá sin cambios.

#### <a name="remarks"></a>Comentarios

**JetSetSystemParameter realiza** un trabajo deficiente al validar la configuración elegida para cada parámetro del sistema. Debe tener cuidado de no confiar en esta validación para aplicar una buena configuración. Preste mucha atención a la descripción de cada parámetro del sistema y siga esas directrices para una buena configuración de parámetros del sistema.

Hay un conjunto de parámetros del sistema que siempre se deben establecer para garantizar que el motor de base de datos funciona según lo previsto. En concreto, siempre se deben establecer los parámetros del sistema que afecten al diseño físico de los archivos utilizados por el motor de base de datos. Para obtener más información, vea [Parámetros del sistema](./extensible-storage-engine-system-parameters.md).

Cada parámetro del sistema tiene un valor predeterminado. Estos valores predeterminados han evolucionado con el tiempo y son bastante arbitrarios. Se recomienda encarecidamente que una aplicación evalúe todos los valores predeterminados para asegurarse de que son adecuados. Si no son adecuados, la aplicación los debe configurar. Esto es importante, ya que muchos de estos parámetros pueden afectar en gran medida a la confiabilidad, el rendimiento y el uso de recursos del motor de base de datos.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetSetSystemParameterW</strong> (Unicode) y <strong>JetSetSystemParameterA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
