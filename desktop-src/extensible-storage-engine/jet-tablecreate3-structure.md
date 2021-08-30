---
description: 'Más información sobre: JET_TABLECREATE3 estructura'
title: Estructura de JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e89ef10fede80b6b48bf0177c2eb7d883c072633
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468322"
---
# <a name="jet_tablecreate3-structure"></a>Estructura de JET_TABLECREATE3


_**Se aplica a:** Windows | Windows Servidor_

La **JET_TABLECREATE3** contiene la información necesaria para crear una tabla rellenada con columnas e índices en una base de datos extensible de motor de Storage (ESE) y que designa una función de devolución de llamada. La **función** [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) usa la estructura JET_TABLECREATE3 de datos.

La **JET_TABLECREATE3** se introdujo en el sistema operativo Windows 7.

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de esta estructura en bytes (para futuras expansiones). Debe establecerse en sizeof( JET_TABLECREATE3 ) en bytes.

**szTableName**

El objeto de la tabla que se va a crear.

El nombre debe cumplir las condiciones siguientes:

  - Debe tener un valor menor que JET_cbNameMost, sin incluir el valor NULL final.

  - Debe constar del siguiente conjunto de caracteres: de 0 a 9, de la A a la Z, de la a la z y de todos los demás signos de puntuación excepto el signo de exclamación ( ), la coma (,), el corchete de apertura ( ) y el corchete de cierre (); es decir, caracteres ASCII 0x20, 0x22 a través de 0x2d, 0x2f a través de 0x5a, 0x5c y 0x5d a \! \[ través de \] 0x7f.

  - No debe comenzar con un espacio.

  - Debe constar de al menos un carácter que no sea de espacio.

**szTemplateTableName**

Nombre de una tabla existente de la que se va a heredar el lenguaje de definición de datos base (DDL). El uso de una tabla de plantillas permite crear fácilmente muchas tablas con columnas e índices idénticos.

**ulPages**

Número inicial de páginas de base de datos que se asignarán a la tabla. Especificar un número mayor que uno puede reducir la fragmentación si se insertan muchas filas en esta tabla.

**ulDensity**

Densidad de tabla, en puntos porcentuales. El número debe ser 0 o en el intervalo de 20 a 100. Pasar 0 significa que se debe usar el valor predeterminado. El valor predeterminado es 80.

**rgcolumncreate**

Matriz de [JET_COLUMNCREATE](./jet-columncreate-structure.md) estructura, cada una de las cuales corresponde a una columna que se va a crear en la nueva tabla.

**cColumns**

Número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) en el *parámetro rgcolumncreate.*

**rgindexcreate**

Matriz de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) estructura, cada una de las cuales corresponde a un índice que se va a crear en la nueva tabla.

**cIndexes**

Número de elementos [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) en el *parámetro rgindexcreate.*

**szCallback**

Función a la que se llama durante determinados eventos. **cbtyp** determina cuándo se llamará a la función de devolución de llamada.

El formato de **szCallback** debe ser "función de módulo"; por ejemplo, "alpha beta" hace referencia a la función beta en el módulo \! \! denominado "alpha".

El prototipo de la función debe coincidir con la [JET_CALLBACK](./jet-callback-callback-function.md) de devolución de llamada.

**cbtyp**

Describe el tipo de función de devolución de llamada designada por **szCallback**. Para obtener más información, [vea JET_CBTYP](./jet-cbtyp.md).

Este campo de bits se compone de uno o varios de los valores de bits enumerados en la tabla siguiente.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_cbtypFinalize</p> | <p>Se llamará a la función de devolución de llamada cuando una columna que se pueda finalizar haya pasado a cero.</p> | 
| <p>JET_cbtypBeforeInsert</p> | <p>Se llamará a la función de devolución de llamada antes de la inserción del registro.</p> | 
| <p>JET_cbtypAfterInsert</p> | <p>Se llamará a la función de devolución de llamada después de que el motor de base de datos haya terminado de insertar un registro.</p> | 
| <p>JET_cbtypBeforeReplace</p> | <p>Se llamará a la función de devolución de llamada antes de la modificación de un registro.</p> | 
| <p>JET_cbtypAfterReplace</p> | <p>Se llamará a la función de devolución de llamada después de finalizar la modificación de un registro.</p> | 
| <p>JET_cbtypBeforeDelete</p> | <p>Se llamará a la función de devolución de llamada antes de la eliminación de un registro.</p> | 
| <p>JET_cbtypAfterDelete</p> | <p>Se llamará a la función de devolución de llamada después de eliminar un registro.</p> | 
| <p>JET_cbtypUserDefinedDefaultValue</p> | <p>Se llamará a la función de devolución de llamada para calcular un valor predeterminado definido por el usuario.</p> | 
| <p>JET_cbtypFreeCursorLS</p> | <p>Se llamará a la función de devolución de llamada cuando se deba liberar el almacenamiento local asociado a un cursor.</p> | 
| <p>JET_cbtypFreeTableLS</p> | <p>Se llamará a la función de devolución de llamada cuando se deba liberar el almacenamiento local asociado a una tabla.</p> | 



**grbit**

Grupo de bits que contiene cero o más de los valores de opción de llamada enumerados en la tabla siguiente.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>Impide las operaciones DDL en la tabla (por ejemplo, agregar o quitar columnas).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>Hace que la tabla sea una tabla de plantillas. A continuación, las nuevas tablas pueden especificar el nombre de esta tabla como tabla de plantilla. Establecer JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Debe usarse junto con JET_bitTableCreateTemplateTable. Desusado. No utilizar.</p> | 



**pSeqSpacehints**

Puntero a una estructura [JET_SPACEHINTS](./jet-spacehints-structure.md) para el índice secuencial predeterminado.

**pSeqSpacehints** se introdujo en Windows 7.

**pLVSpacehints**

Puntero a una estructura [JET_SPACEHINTS](./jet-spacehints-structure.md) para un árbol de valores largos separados.

**pLVSpacehints** se introdujo en Windows 7.

**cbSeparateLV**

Tamaño para separar un LV intrínseco del registro principal. Cualquier estructura c de valor largo para un árbol lv separado. Para obtener más información, vea ng-value en [JET_SPACEHINTS](./jet-spacehints-structure.md). Las columnas de valor largo más pequeñas que este valor se pueden separar si el registro se vuelve demasiado grande.

**cbSeparateLV** se introdujo en Windows 7.

**tableid**

Campo de salida que contiene el [JET_TABLEID](./jet-tableid.md) de la nueva tabla si la llamada API se realiza correctamente. Si se produce un error en la llamada API, el valor no está definido. Esta tabla se abre exclusivamente.

**cCreated**

Campo de salida que contiene el recuento de objetos que se crean si la llamada API se realiza correctamente. Si se produce un error en la llamada API, el valor no está definido.

El recuento de objetos que se crean es igual a la suma de columnas, tablas e índices creados correctamente.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_TABLECREATE3_W</strong> (Unicode) <strong>y JET_TABLECREATE3_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetDefragment2](./jetdefragment2-function.md)
