---
description: 'Más información sobre: JetEnableMultiInstance (Función)'
title: JetEnableMultiInstance (Función)
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dba0b8094187f3a59f05f4b1a1fae1b95dbab66e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989040"
---
# <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance (Función)

La **función JetEnableMultiInstance** configura el motor de base de datos para su uso con varias instancias en el mismo proceso. Hay disponible una matriz opcional de parámetros del sistema global para el primer autor de la llamada que permite el cambio al modo de varias instancias.

**Windows XP: JetEnableMultiInstance** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a>Parámetros

*psetsysparam*

Matriz de parámetros del sistema global que se va a establecer si y solo si el motor entra en modo de instancias múltiples como resultado de esta llamada. Si *csetsysparam es* cero, *se omite psetsysparam.*

*csetsysparam*

Recuento de elementos de la matriz de parámetros globales que se establecerán si y solo si el motor entra en modo de instancias múltiples como resultado de esta llamada. Si *csetsysparam es* cero, *se omite psetsysparam.*

*pcsetsucceed*

Puntero al recuento de parámetros globales del sistema que se configuraron correctamente como resultado de esta llamada.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>No se han permitido los parámetros de índice de tupla especificados. <strong>JetEnableMultiInstance</strong> solo puede devolver este error al establecer JET_paramIndexTuplesLengthMin <a href="gg294119(v=exchg.10).md">,</a> <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> en un valor no válido.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errInvalidPath</p> | <p>La ruta de acceso del sistema de archivos especificada no era válida. <strong>JetEnableMultiInstance</strong> solo puede devolver este error al establecer parámetros del sistema que representan rutas de acceso del sistema de archivos. Por ejemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> puede devolver este error.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Error en la operación porque no es posible cuando el motor de base de datos funciona en modo de instancia única (Windows modo de compatibilidad 2000).</p> | 
| <p>JET_errSystemParamsAlreadySet</p> | <p><strong>Error de JetEnableMultiInstance</strong> porque el motor ya está en modo de varias instancias.</p><p><strong>Nota  </strong> Esto ocurrirá incluso si no se especifican parámetros del sistema.</p> | 



Si esta función se realiza correctamente, el motor de base de datos se configurará para ejecutarse en modo de varias instancias. El motor también se configuró correctamente con la lista opcional de parámetros globales del sistema.

Si se produce un error en esta función, el motor de base de datos permanecerá en el modo actual. Si *pcsetsucceed* es distinto de cero, ese número de parámetros del sistema permanecerá establecido.

#### <a name="remarks"></a>Observaciones

Esta función solo debe usarse si la aplicación debe configurar un conjunto determinado de parámetros del sistema de forma atómica al configurar el motor de base de datos para su uso en un escenario de varios usuarios en el mismo proceso. Si hay otro método de sincronización disponible, es preferible llamar a [JetCreateInstance](./jetcreateinstance-function.md) y [JetSetSystemParameter por](./jetsetsystemparameter-function.md) separado.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetEnableMultiInstanceW</strong> (Unicode) y <strong>JetEnableMultiInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
