---
description: 'Más información acerca de: JetEnableMultiInstance (función)'
title: JetEnableMultiInstance función)
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
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697873"
---
# <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance función)

La función **JetEnableMultiInstance** configura el motor de base de datos para su uso con varias instancias en el mismo proceso. Una matriz opcional de parámetros globales del sistema está disponible para el primer llamador, lo que permite el cambio en el modo de varias instancias.

**Windows XP: JetEnableMultiInstance** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a>Parámetros

*psetsysparam*

Una matriz de parámetros globales del sistema para establecer si y solo si el motor entra en modo de varias instancias como resultado de esta llamada. Si *csetsysparam* es cero, *psetsysparam* se omite.

*csetsysparam*

Recuento de elementos de la matriz de parámetros globales que se van a establecer si y solo si el motor entra en modo de varias instancias como resultado de esta llamada. Si *csetsysparam* es cero, *psetsysparam* se omite.

*pcsetsucceed*

Puntero al recuento de parámetros del sistema globales que se configuraron correctamente como resultado de esta llamada.

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
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>No se permiten los parámetros de índice de tupla especificados. Este error puede ser devuelto por <strong>JetEnableMultiInstance</strong> solo cuando se establece <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> en un valor no válido.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>La ruta de acceso del sistema de archivos especificada no era válida. Este error puede ser devuelto por <strong>JetEnableMultiInstance</strong> solo cuando se establecen parámetros del sistema que representan rutas de acceso del sistema de archivos. Por ejemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> puede devolver este error.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>No se pudo realizar la operación porque no es válida cuando el motor de base de datos está funcionando en modo de instancia única (modo de compatibilidad de Windows 2000).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemParamsAlreadySet</p></td>
<td><p>Error de <strong>JetEnableMultiInstance</strong> porque el motor ya está en modo de varias instancias.</p>
<p><strong>Nota:  </strong> Esto ocurrirá aunque no se especifiquen parámetros del sistema.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, el motor de base de datos se configurará para ejecutarse en modo de varias instancias. El motor también se configuró correctamente con la lista opcional de parámetros del sistema globales.

Si se produce un error en esta función, el motor de base de datos permanecerá en el modo actual. Si *pcsetsucceed* es distinto de cero, ese número de parámetros del sistema permanecerá establecido.

#### <a name="remarks"></a>Observaciones

Esta función solo se debe usar si la aplicación debe configurar un conjunto determinado de parámetros del sistema de forma atómica al configurar el motor de base de datos para su uso en un escenario de varios usuarios en el mismo proceso. Si hay otro método de sincronización disponible, es preferible llamar a [JetCreateInstance](./jetcreateinstance-function.md) y [JetSetSystemParameter](./jetsetsystemparameter-function.md) por separado.

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
<td><p>Se implementa como <strong>JetEnableMultiInstanceW</strong> (Unicode) y <strong>JetEnableMultiInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
