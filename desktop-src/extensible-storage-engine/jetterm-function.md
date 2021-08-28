---
description: 'Más información sobre: JetTerm (Función)'
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
ms.openlocfilehash: a22e9f21ab1c3d296a770c53bc6ad5847264b703
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988418"
---
# <a name="jetterm-function"></a>Función JetTerm


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetterm-function"></a>Función JetTerm

La **función JetTerm** inicia el cierre de una instancia de inicializada por [JetInit.](./jetinit-function.md)

**JetTerm** también se puede usar para destruir una instancia no inicializada creada por [JetCreateInstance.](./jetcreateinstance-function.md)

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Especifica la instancia que se va a usar para esta llamada.

**Windows 2000:**  Este parámetro se omite y siempre debe ser **NULL.**

**Windows XP y versiones posteriores:**  Este parámetro está sobrecargado. Si el motor funciona en modo heredado (modo de compatibilidad Windows 2000) donde solo se admite una instancia, este parámetro podría ser **NULL** o podría contener la instancia real devuelta por [JetInit](./jetinit-function.md). Si el motor funciona en modo de varias instancias, este parámetro debe ser un puntero a una instancia que se creó [mediante JetCreateInstance](./jetcreateinstance-function.md).

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios parámetros producía un resultado inesperado. <strong>JetTerm</strong> devolverá este error cuando el motor esté en modo de varias instancias y cuando <em>pinstance</em> haga referencia a una instancia no válida.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque la instancia aún no se ha inicializado.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque la instancia se está cerrando.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia.</p> | 
| <p>JET_errBackupInProgress</p> | <p>La operación no se puede completar porque hay una operación de copia de seguridad en curso en la instancia.</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>La instancia no se puede cerrar porque actualmente hay sesiones con transacciones activas para la instancia especificada. Este error solo se produce si se usa JET_bitTermComplete de datos.</p> | 



Si esta función se realiza correctamente, se cerrará la instancia especificada. El identificador de instancia también se cerrará y no estará disponible para ninguna API que tome un identificador de instancia. También se cerrarán todos los demás objetos asociados a la instancia, como sesiones. El estado del archivo de punto de comprobación, los archivos de registro de transacciones y los archivos de base de datos asociados a la instancia se modificarán durante el proceso de apagado.

Si se produce un error en esta función como resultado de un error de uso, la instancia permanece en estado inicializado y no cambia nada. De lo contrario, la instancia se sigue apagando según el caso de éxito. La diferencia es que la instancia tendrá que pasar por la recuperación de bloqueos cuando se inicialice a continuación. El motor intentará vaciar tantos datos como sea posible para minimizar la cantidad de recuperación necesaria. Conceptualmente, este error de **JetTerm** no es diferente de un bloqueo del proceso.

#### <a name="remarks"></a>Observaciones

Si el proceso de host de una instancia se cierra por cualquier motivo antes de llamar correctamente a **JetTerm** en esa instancia, se considera que la instancia está en estado de bloqueo. La recuperación de bloqueos se producirá en el siguiente intento de inicializar esa instancia.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm2](./jetterm2-function.md)
