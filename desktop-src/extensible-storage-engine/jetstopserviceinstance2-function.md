---
description: 'Más información acerca de: JetStopServiceInstance2 (función)'
title: JetStopServiceInstance2 función)
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
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810358"
---
# <a name="jetstopserviceinstance2-function"></a>JetStopServiceInstance2 función)


_**Se aplica a:** Windows | Windows Server_

La función **JetStopServiceInstance2** prepara una instancia antes de la suspensión y prepara una instancia después de la reanudación. Suspender y reanudar son Estados de ejecución del modelo de ciclo de vida de aplicaciones de la tienda Windows.

La función **JetStopServiceInstance2** se presentó en Windows 8.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Parámetros

*repetición*

Instancia de de destino. El tipo de datos **JET_INSTANCE** es un identificador de la instancia de la base de datos que se va a usar para una llamada a la API de jet. Este identificador se obtiene cuando se crea una instancia de la base de datos mediante una llamada a las funciones [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)o [JetInit2](./jetinit2-function.md) .

*grbit*

Grupo de bits que especifica uno o más de los valores enumerados y definidos en la tabla siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitStopServiceAll</p></td>
<td><p>Detiene todos los servicios del motor de almacenamiento extensible (ESE) para la instancia especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceBackgroundUserTasks</p></td>
<td><p>Detiene las tareas de mantenimiento en segundo plano especificadas por el cliente que se reinician (por ejemplo, la desfragmentación de árbol B +).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitStopServiceQuiesceCaches</p></td>
<td><p>Quiesces todas las cachés desfasadas en el disco. Este valor es asincrónico y se puede cancelar.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceResume</p></td>
<td><p>Reanuda las operaciones StopService emitidas previamente. es decir, reinicia el servicio. Este valor se puede combinar con el parámetro <em>grbits</em> para reanudar servicios específicos o con JET_bitStopServiceAll para reanudar todos los servicios detenidos previamente. Este bit solo se puede usar para reanudar StopServiceBackgroundUserTasks y JET_bitStopServiceQuiesceCaches. Si anteriormente llamó a con JET_bitStopServiceAll, se producirá un error al intentar usar JET_bitStopServiceResume. Si no se llama al segundo paso de reanudación, la aplicación tendrá un rendimiento degradado. En esta situación, el punto de comprobación se mantiene en cero.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

Esta función permite que una aplicación JET mueva la memoria caché de la base de datos a un estado limpio o casi limpio (con la e/s de sistema operativo inactiva), de modo que, si la aplicación se terminara, la recuperación sería rápida. Este enfoque es preferible a la terminación de JET llamando a las funciones [JetTerm](./jetterm-function.md) o [JetDetachDatabase](./jetdetachdatabase-function.md) , de modo que en el escenario más común, la aplicación no se suspenda y, posteriormente, la aplicación tenga la memoria caché completa y esté lista para funcionar lo antes posible.

Si esta función se ejecuta correctamente, prepara la caché de base de datos para una suspensión inminente. Esta función pone en cola el trabajo en un subproceso de trabajo en segundo plano y vuelve al autor de la llamada inmediatamente. Se debe llamar a la función en función de la VisibilityNotice de PLM en lugar de llamar a desde el controlador de eventos de suspensión de la aplicación para asegurarse de que JET tiene tiempo para vaciar los búferes sucios antes de que un PLM se suspenda/finalice el proceso. Internamente, JET desencadena una distribución inmediata del mantenimiento del punto de comprobación en el cambio de configuración (actualización de puntos de comprobación o este nuevo bit de caché de inactividad). Para obtener más información sobre los eventos de VisibilityNotice, vea [clase VisibilityChangedEventArgs](/uwp/api/windows.ui.core.visibilitychangedeventargs).

Se debe llamar dos veces a esta función. Se llama después de que la aplicación reciba el aviso de suspensión del sistema operativo, pero antes de que la aplicación se haya suspendido. Después, se vuelve a llamar después de que el sistema operativo reanude la aplicación. Por ejemplo:

Cuando se llama a Suspend: JET_ERR JET_API JetStopServiceInstance2 (instancia, JET_bitStopServiceQuiesceCaches);

Cuando se reanude: JET_ERR JET_API JetStopServiceInstance2 (instancia, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);

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
