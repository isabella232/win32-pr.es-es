---
description: 'Más información sobre: Función JetStopServiceInstance2'
title: Función JetStopServiceInstance2
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b5446306bd4035c68f33db2966b1cfadd0b6d82
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987238"
---
# <a name="jetstopserviceinstance2-function"></a>Función JetStopServiceInstance2


_**Se aplica a:** Windows | Windows Servidor_

La **función JetStopServiceInstance2** prepara una instancia antes de Suspender y prepara una instancia después de Reanudar. Suspender y reanudar son estados de ejecución del modelo de ciclo Windows de vida de la aplicación de la Tienda.

La **función JetStopServiceInstance2** se introdujo en Windows 8.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia de destino. El **JET_INSTANCE** tipo de datos es un identificador de la instancia de la base de datos que se va a usar para una llamada a la API jet. Este identificador se obtiene al crear una instancia de la base de datos mediante una llamada a las funciones [JetCreateInstance,](./jetcreateinstance-function.md) [JetCreateInstance2,](./jetcreateinstance2-function.md) [JetInit](./jetinit-function.md)o [JetInit2.](./jetinit2-function.md)

*grbit*

Grupo de bits que especifica uno o varios de los valores enumerados y definidos en la tabla siguiente.


| <p>Value</p> | <p>Descripción</p> | 
|--------------|--------------------|
| <p>JET_bitStopServiceAll</p> | <p>Detiene todos los servicios Storage motor de base de datos extensible (ESE) para la instancia especificada.</p> | 
| <p>JET_bitStopServiceBackgroundUserTasks</p> | <p>Detiene las tareas de mantenimiento en segundo plano que se pueden reiniciar especificadas por el cliente (desfragmentación de árbol B+, por ejemplo).</p> | 
| <p>JET_bitStopServiceQuiesceCaches</p> | <p>Se desasocian todas las memorias caché desasembladas en el disco. Este valor es asincrónico y se puede cancelar.</p> | 
| <p>JET_bitStopServiceResume</p> | <p>Reanuda las operaciones StopService emitidas anteriormente; es decir, reinicia el servicio. Este valor se puede combinar con el parámetro <em>grbits</em> para reanudar servicios específicos o con JET_bitStopServiceAll reanudar todos los servicios detenidos previamente. Este bit solo se puede usar para reanudar StopServiceBackgroundUserTasks y JET_bitStopServiceQuiesceCaches. Si anteriormente llamó a con JET_bitStopServiceAll, se producirá un error al intentar JET_bitStopServiceResume de datos. Si no se llama al segundo paso de reanudación, la aplicación tendrá un rendimiento degradado. En esta situación, el punto de control se mantiene en cero.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 



#### <a name="remarks"></a>Observaciones

Esta función permite que una aplicación JET mueva la memoria caché de la base de datos a un estado limpio o casi limpio (con la E/S del sistema operativo inactiva), de modo que, si la aplicación se terminara, la recuperación sería rápida. Este enfoque es preferible a la terminación de JET mediante una llamada a las funciones [JetTerm](./jetterm-function.md) o [JetDetachDatabase,](./jetdetachdatabase-function.md) de modo que en el escenario más común, la aplicación simplemente no esté en suspensión y, posteriormente, la aplicación tenga toda la caché y esté lista para funcionar lo antes posible.

Si esta función se realiza correctamente, prepara la memoria caché de la base de datos para una suspensión inminente. Esta función pone en cola el trabajo en un subproceso de trabajo en segundo plano y vuelve al autor de la llamada inmediatamente. Se debe llamar a la función en función de PLM VisibilityNotice en lugar de llamar desde el controlador de eventos de suspensión de la aplicación para asegurarse de que JET tiene tiempo para vaciar los búferes desaperciados antes de que PLM suspenda o finalice el proceso. Internamente, JET desencadena un envío inmediato del mantenimiento del punto de control tras el cambio de configuración (ya sea la actualización del punto de control o este nuevo modo de inquiete almacena en caché el bit). Para obtener más información sobre los eventos VisibilityNotice, vea [VisibilityChangedEventArgs (clase).](/uwp/api/windows.ui.core.visibilitychangedeventargs)

Se debe llamar a esta función dos veces. Se llama después de que la aplicación reciba el aviso de suspensión del sistema operativo, pero antes de que se suspenda la aplicación. A continuación, se llama de nuevo después de que el sistema operativo reanude la aplicación. Por ejemplo:

Cuando se llama a Suspend: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches);

Cuando se reanuda: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches| JET_bitStopServiceResume );

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
