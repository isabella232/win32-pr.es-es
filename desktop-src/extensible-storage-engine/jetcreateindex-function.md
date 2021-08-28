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
ms.openlocfilehash: 698f9a050415568c06c8e10819cfed12a4a17181
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478401"
---
# <a name="jetcreateindex-function"></a>Función JetCreateIndex


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcreateindex-function"></a>Función JetCreateIndex

La **función JetCreateIndex** permite crear un índice de datos en una base de datos extensible de Storage Engine (ESE), que puede usar para buscar datos específicos rápidamente.

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

  - Solo debe contener caracteres de las categorías siguientes: de 0 a 9, de A a Z, de a a a a z y de todos los caracteres de puntuación excepto " \! " (signo de exclamación), "," (coma), " " (corchete de apertura) y " " (corchete de cierre), es decir, los caracteres \[ \] ASCII 0x20, 0x22 a través de 0x2d, 0x2f a través de 0x5a, 0x5c y 0x5d a 0x7f.

  - No debe comenzar con un espacio.

  - Debe contener al menos un carácter que no sea de espacio.

*grbit*

Grupo de bits que contiene las opciones que se usarán para una llamada determinada. Este parámetro puede incluir cero o más de las opciones que se encuentran en la [JET_INDEXCREATE](./jet-indexcreate-structure.md) estructura.

*szKey*

Puntero a una cadena terminada en null doble de tokens delimitados por NULL.

Para obtener más información sobre este parámetro, vea la [JET_INDEXCREATE](./jet-indexcreate-structure.md) estructura.

*cbKey*

Longitud, en bytes, del *parámetro szKey,* incluidos los dos caracteres NULL finales.

*lDensity*

Densidad de porcentaje del árbol B+ del índice inicial.

Para obtener más información sobre este parámetro, vea la [JET_INDEXCREATE](./jet-indexcreate-structure.md) estructura.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Significado</p> | 
|--------------------|----------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 



Para obtener una lista de errores adicionales que puede devolver la función **JetCreateIndex,** vea [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Comentarios

Llamar a la función **JetCreateIndex** es idéntico a llamar a la función [JetCreateIndex2](./jetcreateindex2-function.md) con una estructura JET_INDEXCREATE que contiene la misma configuración que los parámetros de **JetCreateIndex** y un parámetro *cIndexCreate* igual [a](./jet-indexcreate-structure.md) 1. Para los campos de la [JET_INDEXCREATE](./jet-indexcreate-structure.md) que no tienen los parámetros correspondientes en **JetCreateIndex**, se supone un valor de 0.

Tenga en **cuenta que JetCreateIndex** ha sido reemplazado por [JetCreateIndex2.](./jetcreateindex2-function.md)

#### <a name="requirements"></a>Requisitos


| | | <p>Remoto</p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p>Servidor</p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p>Encabezado</p> | <p>Se declara en Esent.h.</p> | | <p>Biblioteca</p> | <p>Usa ESENT.lib.</p> | | <p>Archivo DLL</p> | <p>Requiere ESENT.dll.</p> | | <p>Unicode</p> | <p>Se implementa como <strong>JetCreateIndexW</strong> (Unicode) y <strong>JetCreateIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
