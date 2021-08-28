---
description: 'Más información sobre: JetCreateInstance2 (Función)'
title: Función JetCreateInstance2
TOCTitle: JetCreateInstance2 Function
ms:assetid: 1f894b19-fa15-4d89-a3d1-ee13b346f545
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269202(v=EXCHG.10)
ms:contentKeyID: 32765505
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstance2
- JetCreateInstance2W
- JetCreateInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cebf23486505cd0381bd8cd62024ad0bc767633
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987428"
---
# <a name="jetcreateinstance2-function"></a>Función JetCreateInstance2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcreateinstance2-function"></a>Función JetCreateInstance2

La **función JetCreateInstance2** se usa para asignar una nueva instancia del motor de base de datos para su uso en un único proceso, con un nombre para mostrar especificado.

**Windows XP:****JetCreateInstance2** se introdujo en Windows XP.  

```cpp
    JET_ERR JET_API JetCreateInstance2(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName,
      __in_opt      const tchar* szDisplayName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*pinstance*

Búfer de salida que recibirá la instancia recién creada.

*szInstanceName*

Especifica un identificador de cadena único para la instancia que se va a crear. Esta cadena debe ser única dentro de un proceso determinado que hospeda el motor de base de datos.

**Nota** Un valor NULL se trata como un identificador de cadena válido para una instancia de . Solo una instancia puede tener un identificador de cadena NULL.

*szDisplayName*

Nombre para mostrar de la instancia que se va a crear. Cuando este parámetro no está presente, se supone que su valor es NULL.

*grbit*

Reservado para uso futuro. Cuando este parámetro no está presente, se supone que su valor es cero.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInstanceNameInUse</p> | <p>El nombre de instancia especificado ya está en uso para este proceso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <a href="gg269354(v=exchg.10).md">JetCreateInstance cuando</a> <em>pinstance</em> es NULL.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Error en la operación porque no se puede usar cuando el motor de base de datos funciona en modo de instancia única (Windows modo de compatibilidad 2000).</p> | 
| <p>JET_errTooManyInstances</p> | <p>No se pudo crear una nueva instancia porque se ha alcanzado el número máximo de instancias. El número máximo de instancias admitidas se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <em>mediante JET_paramMaxInstances</em>.</p> | 



Si se ejecuta correctamente, se asignará una nueva instancia y se devolverá el identificador de ella. En este momento, todos los parámetros del sistema de la instancia tendrán los valores de los parámetros del sistema predeterminados globales. Una vez asignada una instancia, debe terminarse o liberarse más adelante.

En caso de error, se devolverá un error que representa la causa del error y no se asignará ninguna instancia.

#### <a name="remarks"></a>Observaciones

Una instancia debe inicializarse con una llamada a [JetInit](./jetinit-function.md) antes de que pueda ser utilizada por cualquier otro elemento que no [sea JetSetSystemParameter.](./jetsetsystemparameter-function.md)

Una llamada a la función [JetTerm](./jetterm-function.md) destruye una instancia de , incluso si esa instancia nunca se inicializó mediante [JetInit](./jetinit-function.md). El número máximo de instancias que se pueden crear en cualquier momento se controla mediante *JET_paramMaxInstances*, que se puede configurar mediante una llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md). Una instancia es la unidad de capacidad de recuperación del motor de base de datos. Controla el ciclo de vida de todos los archivos usados para proteger la integridad de los datos en un conjunto de archivos de base de datos. Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.

Si la función se realiza correctamente, el motor de base de datos se cambiará automáticamente al modo de varias instancias como efecto secundario de esta llamada. Si la aplicación desea permitir solo una instancia en el proceso, [jetInit](./jetinit-function.md) debe usarse para iniciar el motor de base de datos Windows modo de compatibilidad 2000.

Si está presente, el parámetro *szDisplayName* se usará para identificar la instancia en lugares como el registro de eventos o hacia otros llamadores como aplicaciones de copia de seguridad (a través de funciones como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) o [JetOSSnapshotFreeze).](./jetossnapshotfreeze-function.md) Si no se proporciona el nombre para mostrar, se usará el parámetro *szInstanceName* único en su lugar, si está presente, de lo contrario, se devolverá una cadena vacía. Si el motor no tenía establecido el modo de ejecución, después de esta llamada, se establecerá en modo de varias instancias.

La secuencia de inicio típica de un proceso que podría ejecutar varias instancias de Jet sería:

  - Una llamada a **JetCreateInstance2** que asignará y asignará un nombre a la instancia.

  - Varias llamadas a [JetSetSystemParameter para](./jetsetsystemparameter-function.md) esa instancia con el fin de establecer distintos parámetros del sistema. Tenga en cuenta que algunos parámetros del sistema deben ser únicos para cada instancia (como *JET_paramSystemPath* o *JET_paramLogFilePath*), por lo que lo más probable es que cada uno de ellos deba establecerse.

  - Inicie la instancia con [JetInit](./jetinit-function.md) o [JetInit2.](./jetinit2-function.md) Para finalizar o liberar una instancia, use [JetTerm](./jetterm-function.md) o [JetTerm2.](./jetterm2-function.md)

Si se trata de la primera instancia que se va a iniciar, hay una serie de pasos adicionales que se ejecutarán durante esta llamada para realizar la inicialización y configuración básicas del sistema. Algunos de estos pasos pueden dar lugar a errores específicos a partir de JET_errOutOfMemory pero también otros (consulte Valores devueltos para obtener más información).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetCreateInstance2W</strong> (Unicode) y <strong>JetCreateInstance2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
