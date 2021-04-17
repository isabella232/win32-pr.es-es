---
description: 'Más información acerca de: JetCreateInstance (función)'
title: Función JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717168"
---
# <a name="jetcreateinstance-function"></a>Función JetCreateInstance


_**Se aplica a:** Windows | Windows Server_

## <a name="jetcreateinstance-function"></a>Función JetCreateInstance

La función **JetCreateInstance** asigna una nueva instancia del motor de base de datos para su uso en un único proceso.

**Windows XP: JetCreateInstance** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a>Parámetros

*pinstance*

Búfer de salida que recibe la instancia creada recientemente.

*szInstanceName*

Identificador de cadena único para la instancia que se va a crear. Esta cadena debe ser única dentro de un proceso determinado que hospede el motor de base de datos.

**Nota:** Un valor NULL se trata como un identificador de cadena válido para una instancia de. Solo una instancia puede tener un identificador de cadena NULL.

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
<td><p>JET_errInstanceNameInUse</p></td>
<td><p>El nombre de instancia especificado ya está en uso para este proceso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para <strong>JetCreateInstance</strong> cuando <em>pinstance</em> es <strong>null</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>No se pudo realizar la operación porque no se puede usar cuando el motor de base de datos está funcionando en modo de instancia única (modo de compatibilidad de Windows 2000).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances</p></td>
<td><p>No se pudo crear una nueva instancia porque se ha alcanzado el número máximo de instancias. El número máximo de instancias admitidas se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxInstances</em>.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se asignará una nueva instancia de y se devolverá el identificador de la misma. En este momento, todos los parámetros del sistema para la instancia de tendrán los valores de los parámetros globales del sistema predeterminados. Una vez que se asigna una instancia, debe terminarse o liberarse más adelante.

En caso de error, se devolverá un error que representa la causa del error y no se asignará ninguna instancia.

#### <a name="remarks"></a>Observaciones

Una instancia de se debe inicializar con una llamada a [JetInit](./jetinit-function.md) para que pueda ser utilizada por cualquier cosa que no sea [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Una instancia de se destruye mediante una llamada a la función [JetTerm](./jetterm-function.md) , incluso si esa instancia nunca se inicializó con [JetInit](./jetinit-function.md). El número máximo de instancias que se pueden crear en un momento determinado se controla mediante [JET_paramMaxInstances](./resource-parameters.md), que se puede configurar mediante una llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md). Una instancia es la unidad de capacidad de recuperación del motor de base de datos. Controla el ciclo de vida de todos los archivos utilizados para proteger la integridad de los datos en un conjunto de archivos de base de datos. Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.

Si la función se ejecuta correctamente, el motor de base de datos se cambiará automáticamente al modo de varias instancias como un efecto secundario de esta llamada. Si la aplicación desea permitir solo una instancia en el proceso, se debe utilizar [JetInit](./jetinit-function.md) para iniciar el motor de base de datos en el modo de compatibilidad de Windows 2000.

Si está presente, el *szDisplayName* se usará para identificar la instancia en lugares como el registro de eventos o en otros llamadores como aplicaciones de copia de seguridad (a través de funciones como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) o [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)). Si no se proporciona el nombre para mostrar, se usará en su lugar el valor de *szInstanceName* único, si está presente; de lo contrario, se devolverá una cadena vacía. Si el motor no tenía establecido el modo de ejecución, después de esta llamada se establecerá en modo de varias instancias.

La secuencia de inicio típica para un proceso que puede ejecutar varias instancias de jet sería:

  - Una llamada a [JetCreateInstance2](./jetcreateinstance2-function.md) que asignará y denominará a la instancia.

  - Varias llamadas a [JetSetSystemParameter](./jetsetsystemparameter-function.md) para esa instancia con el fin de establecer diferentes parámetros del sistema. Tenga en cuenta que algunos parámetros del sistema deben ser únicos por cada instancia (como [JET_paramSystemPath](./transaction-log-parameters.md) o [JET_paramLogFilePath](./transaction-log-parameters.md)), por lo que lo más probable es que tenga que establecer cada uno de ellos.

  - Inicie la instancia de mediante [JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md). Para finalizar y/o liberar una instancia, se debe usar [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) .

Si esta es la primera instancia que se va a iniciar, hay una serie de pasos adicionales que se ejecutarán durante esta llamada para realizar la inicialización y configuración básicas del sistema. Algunos de estos pasos pueden dar lugar a errores concretos a partir de JET_errOutOfMemory pero otros también (consulte los errores anteriores).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetCreateInstanceW</strong> (Unicode) y <strong>JetCreateInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
