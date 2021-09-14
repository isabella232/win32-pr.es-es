---
description: 'Más información sobre: JetTerm2 (Función)'
title: Función JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 332fa937e7540c31bfea49fe8591e9dc66b0f5e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269708"
---
# <a name="jetterm2-function"></a>Función JetTerm2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetterm2-function"></a>Función JetTerm2

La **función JetTerm2** inicia el apagado de una instancia de inicializada por [JetInit](./jetinit-function.md).

**JetTerm2** también puede destruir una instancia no inicializada creada por [JetCreateInstance.](./jetcreateinstance-function.md)

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia de que se va a usar para esta llamada.

**Windows 2000:**  Este parámetro se omite y siempre debe ser **NULL.**

**Windows XP y versiones posteriores:**  Este parámetro está sobrecargado. Si el motor funciona en modo heredado (modo de compatibilidad Windows 2000) donde solo se admite una instancia, este parámetro podría ser **NULL** o puede contener la instancia real devuelta por [JetInit](./jetinit-function.md). Si el motor funciona en modo de varias instancias, este parámetro debe ser un puntero a una instancia que se creó [mediante JetCreateInstance](./jetcreateinstance-function.md).

*grbit*

Grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de los valores siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTermComplete</p> | <p>Solicita que la instancia se cierre correctamente. Cualquier trabajo de limpieza opcional que normalmente se realizaría en segundo plano en tiempo de ejecución se completa inmediatamente.</p> | 
| <p>JET_bitTermAbrupt</p> | <p>Solicita que la instancia se cierre lo antes posible. Se abandona cualquier trabajo opcional que normalmente se realizaría en segundo plano en tiempo de ejecución.</p><p><strong>Nota</strong>  Esta opción puede provocar una pérdida de espacio temporal o permanente en la base de datos. Este espacio perdido siempre se puede recuperar mediante una desfragmentación sin conexión de la base de datos.</p> | 
| <p>JET_bitTermStopBackup</p> | <p>Solicita que se cierre la instancia incluso si actualmente hay una copia de seguridad en curso. Normalmente, una copia de seguridad pendiente haría que <a href="gg269298(v=exchg.10).md">JetTerm</a> generara un error con JET_errBackupInProgress. Cuando este parámetro no está presente, se supone que su valor JET_bitTermAbrupt.</p> | 
| <p>JET_bitTermDirty</p> | <p>Solicita que la instancia se cierre con todas las bases de datos adjuntas que quedan en un estado desasedado.</p><p>Windows 7: JET_bitTermDirty se introdujo en Windows 7.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupInProgress</p> | <p>La operación no se puede completar porque hay una operación de copia de seguridad en curso en la instancia de .</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios parámetros produjo un resultado inesperado. <a href="gg269298(v=exchg.10).md">JetTerm</a> devolverá este error cuando el motor esté en modo de varias instancias y cuando <em>pinstance</em> haga referencia a una instancia no válida.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque la instancia aún no se ha inicializado.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque la instancia se está cerrando.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia de .</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>La instancia no se puede cerrar porque actualmente hay sesiones con transacciones activas para la instancia especificada. Este error solo se produce si se JET_bitTermComplete se usa el objeto .</p> | 



Si esta función se realiza correctamente, se cerrará la instancia especificada. El identificador de instancia también se cerrará y no estará disponible para ninguna API que tome un identificador de instancia. También se cerrarán todos los demás objetos asociados a la instancia, como las sesiones. El estado del archivo de punto de comprobación, los archivos de registro de transacciones y los archivos de base de datos asociados a la instancia se modificarán durante el proceso de apagado.

Si se produce un error en esta función como resultado de un error de uso, la instancia permanece en un estado inicializado y no cambia nada. De lo contrario, la instancia todavía se cierra como se indica para el caso de éxito. La diferencia es que la instancia tendrá que pasar por la recuperación de bloqueos cuando se inicialice por primera vez. El motor intentará vaciar tantos datos como sea posible para minimizar la cantidad de recuperación necesaria. Conceptualmente, este error de [JetTerm](./jetterm-function.md) no es diferente de un bloqueo del proceso.

#### <a name="remarks"></a>Observaciones

Consulte [JetTerm](./jetterm-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm](./jetterm-function.md)
