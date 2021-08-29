---
description: 'Más información sobre: JetCreateIndex (Función)'
title: Función JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e2a5132ae950384a748af27d1d1f8de48952cf3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986048"
---
# <a name="jetcreateindex-function"></a>Función JetCreateIndex


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcreateindex-function"></a>Función JetCreateIndex

La **función JetCreateIndex** permite crear un índice de datos en una base de datos extensible Storage Engine (ESE), que puede usar para localizar datos específicos rápidamente.

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para una llamada API determinada.

*tableid*

Tabla para la que se creará un índice.

*szIndexName*

Puntero a una cadena terminada en NULL que especifica el nombre del índice que se va a crear.

El nombre del índice debe cumplir las siguientes directrices:

  - Debe contener menos caracteres que JET_cbNameMost, sin incluir el carácter nulo final.

  - Solo debe contener caracteres de las siguientes categorías: de 0 a 9, de A a Z, de a a z y de todos los caracteres de puntuación excepto " \! " (signo de exclamación), "," (coma), " " (corchete de apertura) y " " (corchete de cierre), es decir, los caracteres \[ \] ASCII 0x20, 0x22 a través de 0x2d, 0x2f a través de 0x5a, 0x5c y 0x5d a 0x7f.

  - No debe comenzar con un espacio.

  - Debe contener al menos un carácter que no sea de espacio.

*grbit*

Grupo de bits que contiene las opciones que se usarán para una llamada determinada. Este parámetro puede incluir cero o más de las opciones que se encuentran en [la JET_INDEXCREATE](./jet-indexcreate-structure.md) estructura.

*szKey*

Puntero a una cadena terminada en null doble de tokens delimitados por NULL.

Para obtener más información sobre este parámetro, vea la [estructura JET_INDEXCREATE](./jet-indexcreate-structure.md) datos.

*cbKey*

Longitud, en bytes, del *parámetro szKey,* incluidos los dos caracteres null de terminación.

*lDensity*

Densidad porcentual del árbol B+ del índice inicial.

Para obtener más información sobre este parámetro, vea la [estructura JET_INDEXCREATE](./jet-indexcreate-structure.md) datos.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Significado</p> | 
|--------------------|----------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 



Para obtener una lista de errores adicionales que puede devolver la función **JetCreateIndex,** vea [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Observaciones

Llamar a la función **JetCreateIndex** es idéntico a llamar a la función [JetCreateIndex2](./jetcreateindex2-function.md) con una estructura JET_INDEXCREATE que contiene la misma configuración que los parámetros de **JetCreateIndex** y un parámetro *cIndexCreate* igual [a](./jet-indexcreate-structure.md) 1. Para los campos de la [estructura JET_INDEXCREATE](./jet-indexcreate-structure.md) que no tienen los parámetros correspondientes en **JetCreateIndex**, se supone un valor de 0.

Tenga en **cuenta que JetCreateIndex** ha sido reemplazado por [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p>Remoto</p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p>Server</p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p>Encabezado</p> | <p>Se declara en Esent.h.</p> | 
| <p>Biblioteca</p> | <p>Usa ESENT.lib.</p> | 
| <p>Archivo DLL</p> | <p>Requiere ESENT.dll.</p> | 
| <p>Unicode</p> | <p>Se implementa como <strong>JetCreateIndexW</strong> (Unicode) y <strong>JetCreateIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
