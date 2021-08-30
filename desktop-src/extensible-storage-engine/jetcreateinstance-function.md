---
description: 'Más información sobre: JetCreateInstance (Función)'
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
ms.openlocfilehash: eb1f785e5536097430867674eb10295cef81c37b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478031"
---
# <a name="jetcreateinstance-function"></a>Función JetCreateInstance


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcreateinstance-function"></a>Función JetCreateInstance

La **función JetCreateInstance** asigna una nueva instancia del motor de base de datos para su uso en un único proceso.

**Windows XP: JetCreateInstance** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a>Parámetros

*pinstance*

Búfer de salida que recibe la instancia recién creada.

*szInstanceName*

Identificador de cadena único para la instancia que se va a crear. Esta cadena debe ser única dentro de un proceso determinado que hospeda el motor de base de datos.

**Nota** Un valor NULL se trata como un identificador de cadena válido para una instancia de . Solo una instancia puede tener un identificador de cadena NULL.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInstanceNameInUse</p> | <p>El nombre de instancia especificado ya está en uso para este proceso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetCreateInstance cuando</strong> <em>pinstance</em> es <strong>NULL.</strong></p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Error en la operación porque no se puede usar cuando el motor de base de datos funciona en modo de instancia única (Windows modo de compatibilidad 2000).</p> | 
| <p>JET_errTooManyInstances</p> | <p>No se pudo crear una nueva instancia porque se ha alcanzado el número máximo de instancias. El número máximo de instancias admitidas se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <em>mediante JET_paramMaxInstances</em>.</p> | 



Si se ejecuta correctamente, se asignará una nueva instancia y se devolverá el identificador de ella. En este momento, todos los parámetros del sistema para la instancia tendrán los valores de los parámetros del sistema predeterminados globales. Una vez asignada una instancia, debe terminarse o liberarse más adelante.

En caso de error, se devolverá un error que representa la causa del error y no se asignará ninguna instancia.

#### <a name="remarks"></a>Comentarios

Una instancia de debe inicializarse con una llamada a [JetInit](./jetinit-function.md) antes de que pueda ser utilizada por cualquier otro elemento que no [sea JetSetSystemParameter](./jetsetsystemparameter-function.md).

Una instancia de se destruye mediante una llamada a la función [JetTerm,](./jetterm-function.md) incluso si esa instancia nunca se inicializó [mediante JetInit](./jetinit-function.md). El número máximo de instancias que se pueden crear en cualquier momento se controla mediante JET_paramMaxInstances [,](./resource-parameters.md)que se puede configurar mediante una llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md). Una instancia de es la unidad de capacidad de recuperación del motor de base de datos. Controla el ciclo de vida de todos los archivos usados para proteger la integridad de los datos en un conjunto de archivos de base de datos. Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.

Si la función se realiza correctamente, el motor de base de datos se cambiará automáticamente al modo de varias instancias como efecto secundario de esta llamada. Si la aplicación desea permitir solo una instancia en el proceso, se debe usar [JetInit](./jetinit-function.md) para iniciar el motor de base de datos en el modo de compatibilidad Windows 2000.

Si está presente, *szDisplayName* se usará para identificar la instancia en lugares como el registro de eventos o hacia otros llamadores como aplicaciones de copia de seguridad (a través de funciones como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) o [JetOSSnapshotFreeze).](./jetossnapshotfreeze-function.md) Si no se proporciona el nombre para mostrar, se usará *el szInstanceName* único en su lugar si está presente; de lo contrario, se devolverá una cadena vacía. Si el motor no tenía establecido el modo de ejecución, después de esta llamada, se establecerá en modo de varias instancias.

La secuencia de inicio típica para un proceso que podría ejecutar varias instancias de Jet sería:

  - Una llamada a [JetCreateInstance2](./jetcreateinstance2-function.md) que asignará y asignará un nombre a la instancia.

  - Varias llamadas a [JetSetSystemParameter](./jetsetsystemparameter-function.md) para esa instancia con el fin de establecer distintos parámetros del sistema. Tenga en cuenta que algunos parámetros del sistema deben ser únicos por instancia (como [JET_paramSystemPath](./transaction-log-parameters.md) o [JET_paramLogFilePath](./transaction-log-parameters.md)), por lo que lo más probable es que uno de ellos tenga que establecer cada uno de ellos.

  - Inicie la instancia mediante [JetInit](./jetinit-function.md) o [JetInit2.](./jetinit2-function.md) Para finalizar o liberar una instancia, debe [usarSe JetTerm](./jetterm-function.md), [JetTerm2.](./jetterm2-function.md)

Si esta es la primera instancia que se va a iniciar, hay una serie de pasos adicionales que se ejecutarán durante esta llamada para realizar la inicialización y configuración básicas del sistema. Algunos de estos pasos pueden dar lugar a errores específicos a partir de JET_errOutOfMemory pero también otros (consulte los errores anteriores).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetCreateInstanceW</strong> (Unicode) y <strong>JetCreateInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
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
