---
description: 'Más información acerca de: JetSetSessionContext (función)'
title: JetSetSessionContext función)
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715296"
---
# <a name="jetsetsessioncontext-function"></a>JetSetSessionContext función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetsetsessioncontext-function"></a>JetSetSessionContext función)

La función **JetSetSessionContext** asocia una sesión con el subproceso actual utilizando el identificador de contexto especificado. Esta asociación invalida el requisito de motor predeterminado que una transacción para una sesión determinada debe aparecer completamente en el mismo subproceso.

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*ulContext*

Identificador único al que se asociará esta sesión.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado. Este error lo devolverá <strong>JetSetSessionContext</strong> en las siguientes condiciones:</p>
<ul>
<li><p><em>ulContext</em> es null</p></li>
<li><p><em>ulContext</em> es-1</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionContextAlreadySet</p></td>
<td><p>No se pudo asociar la sesión con el subproceso actual porque ya se ha asociado a un subproceso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, la sesión se asociará al subproceso actual. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, el estado de la sesión permanecerá sin cambios. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Normalmente, una sesión está enlazada a un subproceso concreto para la duración de una transacción. Este comportamiento está diseñado para ayudar a las aplicaciones a detectar y evitar el uso compartido conceptualmente inadvertido de una sola sesión entre varios subprocesos. A veces, esta simple comprobación no funciona con la arquitectura de la aplicación. Por ejemplo, si la aplicación hospeda objetos del servidor mediante un grupo de subprocesos y las transacciones abarcan varias llamadas de servidor a un objeto determinado, esta protección puede hacer que algunas de esas llamadas produzcan un error con JET_errSessionSharingViolation aunque el patrón de uso sea correcto. Esta situación es común para los servidores de objetos COM.

**JetSetSessionContext** y [JetResetSessionContext](./jetresetsessioncontext-function.md) solucionan este problema haciendo que la comprobación de uso compartido de la sesión sea un poco más flexible. Cuando la aplicación empieza a realizar una serie de llamadas de la API de ESE mediante una sesión determinada, primero establece el contexto de la sesión en un valor determinado. Esta acción asocia la sesión al subproceso que realiza la llamada. En el ejemplo dado, este contexto podría ser la dirección del objeto que contiene el identificador de sesión JET. Una vez realizadas las llamadas a la API de ESE, la aplicación restablece el contexto de la sesión. Esta acción desasocia la sesión del subproceso que realiza la llamada. Otro subproceso puede utilizar el objeto y su sesión, incluso si la sesión tiene una transacción activa.

Es importante tener en cuenta que se debe llamar a **JetSetSessionContext** antes de abrir una transacción en esa sesión, o bien la asociación no funcionará.

**JetSetSessionContext** es seguro para subprocesos. Varios subprocesos pueden intentar establecer un contexto de subproceso en la misma sesión al mismo tiempo y solo se ganará uno. Este hecho puede ser utilizado por la aplicación como un medio para asignar una sesión de un grupo sin almacenar el estado externo sobre su asignación.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
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


#### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
