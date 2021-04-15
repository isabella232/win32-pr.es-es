---
description: 'Más información acerca de: JetTerm (función)'
title: Función JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ce78ea12dfa61265a12b3858cc1e859adcae6e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696294"
---
# <a name="jetterm-function"></a>Función JetTerm


_**Se aplica a:** Windows | Windows Server_

## <a name="jetterm-function"></a>Función JetTerm

La función **JetTerm** inicia el cierre de una instancia de que [JetInit](./jetinit-function.md)ha inicializado.

**JetTerm** también se puede usar para destruir una instancia no inicializada creada por [JetCreateInstance](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parámetros

*repetición*

Especifica la instancia de que se va a usar para esta llamada.

**Windows 2000:**  Este parámetro se omite y siempre debe ser **null**.

**Windows XP y versiones posteriores:**  Este parámetro está sobrecargado. Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser **null** o contener la instancia real devuelta por [JetInit](./jetinit-function.md). Si el motor está funcionando en modo de varias instancias, este parámetro debe ser un puntero a una instancia de creada mediante [JetCreateInstance](./jetcreateinstance-function.md).

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios parámetros produjo un resultado inesperado. <strong>JetTerm</strong> devolverá este error cuando el motor está en modo de varias instancias y cuando <em>pinstance</em> hace referencia a una instancia no válida.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque la instancia aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque la instancia se está cerrando.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de copia de seguridad en curso en la instancia.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyActiveUsers</p></td>
<td><p>No se puede cerrar la instancia porque actualmente hay sesiones con transacciones activas para la instancia especificada. Este error solo se produce si se usa el JET_bitTermComplete.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, se cerrará la instancia especificada. El identificador de instancia también se cerrará y no estará disponible para ninguna API que tome un identificador de instancia. También se cerrarán todos los demás objetos asociados a la instancia de, como sesiones. El estado del archivo de punto de comprobación, los archivos de registro de transacciones y los archivos de base de datos adjuntos a la instancia se modificarán durante el proceso de cierre.

Si se produce un error en esta función como resultado de un error de uso, la instancia permanece en un estado inicializado y no cambia nada. De lo contrario, la instancia de se sigue cerrando según el caso de éxito. La diferencia es que la instancia de deberá pasar a través de la recuperación de bloqueos la próxima vez que se inicialice. El motor intentará vaciar tantos datos como sea posible para minimizar la cantidad de recuperación necesaria. Conceptualmente, un error de **JetTerm** no es diferente de un bloqueo del proceso.

#### <a name="remarks"></a>Observaciones

Si el proceso de host de una instancia se cierra por cualquier motivo antes de que **JetTerm** se llame correctamente en esa instancia, se considera que la instancia está en un estado bloqueado. La recuperación tras bloqueo se producirá en el siguiente intento de inicializar esa instancia.

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

[Archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm2](./jetterm2-function.md)
