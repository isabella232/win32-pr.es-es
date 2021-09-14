---
description: 'Más información sobre: JetRetrieveKey (Función)'
title: Función JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 938cc8161326afaa9d0d5b3bf905bf976e850b40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964231"
---
# <a name="jetretrievekey-function"></a>Función JetRetrieveKey


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetretrievekey-function"></a>Función JetRetrieveKey

La **función JetRetrieveKey** recupera la clave de la entrada de índice en la posición actual de un cursor. Estas claves se construyen mediante llamadas a [JetMakeKey](./jetmakekey-function.md). La clave recuperada se puede usar para devolver eficazmente ese cursor a la misma entrada de índice mediante una llamada a [JetSeek](./jetseek-function.md).

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*pvData*

Búfer de salida que recibirá la clave.

*cbMax*

Tamaño máximo en bytes del búfer de salida.

*actual*

Recibe el tamaño real en bytes de la clave.

Si este parámetro es NULL, no se devolverá el tamaño real de la clave.

Si el búfer de salida es demasiado pequeño, se devolverá el tamaño real de la clave. Esto significa que este número será mayor que el tamaño del búfer de salida.

*grbit*

Grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Cuando se especifica, el motor devolverá la clave de búsqueda del cursor. La clave de búsqueda se ha creado mediante una o varias llamadas anteriores a <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con el fin de buscar esa clave mediante <a href="gg294103(v=exchg.10).md">JetSeek</a> o establecer un intervalo de índice mediante <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errKeyNotMade</p> | <p>No hay ninguna clave de búsqueda actual para el cursor. Esto ocurrirá con <strong>JetRetrieveKey</strong> si JET_bitRetrieveCopy se especifica y no se ha construido una clave de búsqueda para este cursor mediante una llamada anterior a <a href="gg269329(v=exchg.10).md">JetMakeKey</a>. La clave de búsqueda se eliminará mediante una llamada anterior a cualquier API de navegación en el cursor que no <a href="gg294117(v=exchg.10).md">sea JetMove.</a></p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor no está situado en un registro. Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor se coloca actualmente después del último registro en el índice actual.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir toda la clave. El búfer de salida se ha rellenado con la mayor parte de la clave que cabría. También se ha devuelto el tamaño real de la clave, si se solicita.</p><p><strong>Nota</strong>   Este error no se devolverá si JET_bitRetrieveCopy se especifica . Consulte la sección Comentarios para obtener más información.</p> | 



Si se ejecuta correctamente, se devolverá la clave de la entrada de índice en la posición actual de un cursor en el búfer de salida. Si JET_wrnBufferTruncated se devuelve, el búfer de salida contendrá la mayor parte de la clave que cabe en el espacio proporcionado y el tamaño real de la clave será preciso. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, el estado del búfer de salida y el tamaño real de la clave serán indefinidos. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Las claves generalmente se deben tratar como fragmentos opacos de datos. No se debe intentar aprovechar la estructura interna de estos datos. Sin embargo, se pueden conocer las siguientes propiedades sobre todas las claves DE ESENT:

  - Las claves se pueden comparar entre sí mediante la función [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) para establecer su ordenación relativa en el índice de origen sobre la tabla de las entradas del índice de origen.

  - No tiene sentido comparar las claves de las entradas de índice de distintos índices entre sí.

  - Una clave siempre es menor o igual que JET_cbKeyMost (255) bytes de longitud antes de Windows Vista. En Windows Vista y versiones posteriores, las claves pueden ser mayores. El tamaño máximo de una clave es igual al valor actual de JET_paramKeyMost.

Además de las propiedades anteriores de las claves ESENT en general, es importante tener en cuenta que una clave de búsqueda es diferente de la clave para una entrada de índice. En concreto, una clave de búsqueda puede ser más larga que una clave normal. Esta longitud adicional se produce cuando se usa una opción comodín al construir la clave de búsqueda. Consulte [JetMakeKey para](./jetmakekey-function.md) obtener más información.

Hay un error importante en esta API que está presente en todas las versiones. Si se solicita la clave de búsqueda mediante el uso de JET_bitRetrieveCopy y el búfer de salida es demasiado pequeño para recibir la clave completa, JET_wrnBufferTruncated no se devolverá. JET_errSuccess se devolverá en su lugar. Es importante comprobar que el tamaño real de la clave tal y como se devuelve mediante *fuenactual* es menor o igual que el tamaño del búfer de salida. Si el tamaño real es mayor que el tamaño del búfer de salida, el llamador de **JetRetrieveKey** debe reaccionar como si se devolvieron JET_wrnBufferTruncated en su lugar.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
