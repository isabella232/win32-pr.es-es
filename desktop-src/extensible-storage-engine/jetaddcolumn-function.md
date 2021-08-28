---
description: 'Más información sobre: JetAddColumn (Función)'
title: Función JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c735fb077816fc555b28e4b81b93798898efd92e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989098"
---
# <a name="jetaddcolumn-function"></a>Función JetAddColumn


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetaddcolumn-function"></a>Función JetAddColumn

La **función JetAddColumn** agrega una nueva columna a una tabla existente en una base de datos ese.

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Tabla a la que se va a agregar la columna.

*szColumnName*

Nombre de la columna que se agregará. El nombre debe cumplir los siguientes criterios:

  - Debe tener menos de JET_cbNameMost longitud, sin incluir el valor **NULL final.**

  - Solo debe contener caracteres de los siguientes conjuntos: de 0 a 9, de A a Z, de a a z y de todos los demás signos de puntuación, excepto el signo de exclamación ( ), la coma (,), el corchete de apertura ( ) y el corchete de cierre ( ), es decir, los caracteres ASCII 0x20, 0x22 a través de 0x2d, 0x2f a 0x5a, 0x5c y 0x5d \! \[ a \] 0x7f.

  - No puede comenzar con un espacio.

  - Debe contener al menos un carácter que no sea de espacio.

*pcolumndef*

Puntero a una [estructura JET_COLUMNDEF,](./jet-columndef-structure.md) que define los datos que se pueden almacenar en una columna.

*pvDefault*

Puntero a un búfer que contiene el valor predeterminado de la columna. La longitud del búfer es **cbDefault.** Si no hay ningún valor predeterminado, establezca **pvDefault** en **NULL** y **cbDefault** en cero. Los valores predeterminados no pueden ser mayores que JET_cbColumnMost bytes para columnas fijas o bytes JET_cbLVDefaultValueMost bytes para los valores largos. Si un valor predeterminado es mayor que ese, se truncará de forma silenciosa.

Si *grbit* tiene JET_bitColumnUserDefinedDefault, **pvDefault** se interpretará como un puntero a una [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) estructura.

*cbDefault*

Tamaño, en bytes, del búfer especificado en **pvDefault.**

*pcolumnid*

Puntero a una [estructura JET_COLUMNID,](./jet-columnid.md) que, si se ejecuta correctamente, recibirá el identificador de la columna recién creada. En caso de error, el valor es indefinido.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se realizó correctamente.</p> | 
| <p>JET_errFixedDDL</p> | <p>Se intentó modificar la definición de datos de una tabla DDL fija. Un ejemplo de una tabla con DDL fijo es una tabla de plantilla.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Se pasó un parámetro no válido a la API. Algunos ejemplos de parámetros no válidos son:</p><ul><li><p>Pasar el tamaño incorrecto de la <a href="gg294130(v=exchg.10).md">estructura JET_COLUMNDEF</a> estructura en su <em>miembro cbStruct.</em></p></li><li><p>Pasar JET_bitColumnUserDefinedDefault, pero no establecer <strong>cbDefault</strong> en sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p></li></ul> | 
| <p>JET_errInTransaction</p> | <p>Se intentó agregar una columna con el conjunto JET_bitColumnUnversioned bits, pero la sesión está actualmente en una transacción.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Ya existe una columna. Se intentó agregar una columna sin información de versión y esa columna ya existe.</p> | 
| <p>JET_errTableNotEmpty</p> | <p>La tabla contiene datos. Una columna Actualización de custodia solo se puede agregar a una tabla vacía.</p> | 
| <p>JET_errRecordTooBig</p> | <p>El registro es demasiado grande. La suma del <strong>parámetro cbMax</strong> para las columnas fijas no debe superar un valor determinado.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, no más de JET_ccolVarMost columnas de longitud variable y no más de JET_ccolTaggedMost columnas etiquetadas.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Se intentó agregar una columna redundante. No debería haber más de una columna de autoincremento y no más de una columna de versión por tabla.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>No se pudo resolver la función de devolución de llamada. Es posible que no se haya encontrado el archivo DLL o que la función del archivo DLL no se haya encontrado. El registro de eventos proporcionará más detalles si se habilita el registro suficiente.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Advertencia que indica que la longitud máxima (<strong>cbMax</strong>) de una columna fija o variable era mayor que JET_cbColumnMost. Este límite no se aplica a los valores largos (es <a href="gg269213(v=exchg.10).md">decir,</a> JET_coltypLongBinary y <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p> | 
| <p>JET_errInvalidName</p> | <p>Se pasó un nombre no válido <strong>como szColumnName</strong>. Para obtener más información sobre las restricciones, vea los criterios <strong>de szColumnName</strong>.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>El <strong>campo coltyp</strong> no se estableció en un tipo de columna válido.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>El <strong>parámetro cp</strong> de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se estableció en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (inglés, 1252).</p> | 
| <p>JET_errTaggedNotNULL</p> | <p>JET_bitColumnNotNULL se puede usar con columnas etiquetadas, valor largo o SLV.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Se especificó una combinación no válida de <em>grbits.</em> Algunos de los motivos de este error son:</p><ul><li><p>JET_bitColumnFixed se usó en una columna etiquetada, valor largo o SLV.</p></li><li><p>JET_bitColumnEscrowUpdate se usó en una columna que no era de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li><li><p>JET_bitColumnEscrowUpdate se usó en una columna Versión (JET_bitColumnVersion).</p></li><li><p>JET_bitColumnEscrowUpdate se usó en una columna AutoIncrememnt (JET_bitColumnAutoincrement).</p></li><li><p>JET_bitColumnEscrowUpdate se usó en una columna que no tenía un valor predeterminado<strong>(cbDefault</strong> era igual a cero).</p></li><li><p>JET_bitColumnFinalize se usó en una columna que no era una columna de actualización de custodia (JET_bitColumnEscrowUpdate no se estableció).</p></li><li><p>JET_bitColumnDeleteOnZero se usó en una columna que no era una columna de actualización de custodia (JET_bitColumnEscrowUpdate no se estableció).</p></li><li><p>JET_bitColumnAutoincrement se usó en una columna que no se <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p><p><strong>Windows 2000:</strong> Esta razón para el código de error solo se usa en Windows 2000.</p><p>JET_bitColumnAutoincrement se usó en una columna que no era <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> ni <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</p><p><strong>Windows XP:</strong> Esta razón para el código de error se usa en Windows XP y sistemas operativos posteriores.</p></li><li><p>JET_bitColumnVersion se usó en una columna que no se <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li><li><p>JET_bitColumnVersion se usó en una columna de decremento automático.</p></li><li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnFixed.</p></li><li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnNotNULL.</p></li><li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnVersion.</p></li><li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnAutoincrement.</p></li><li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnUpdatable.</p></li><li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnEscrowUpdate.</p></li><li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnFinalize.</p></li><li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnDeleteOnZero.</p></li><li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnMaybeNull.</p></li><li><p>JET_bitColumnUserDefinedDefault se usó en una columna no etiquetada (que es fija o variable).</p></li></ul> | 
| <p>JET_errMultiValuedColumnMustBeTagged</p> | <p>Una columna con varios valores (JET_bitColumnMultiValued) solo se puede usar<a href="gg269213(v=exchg.10).md"></a> en una columna etiquetada o de valor largo <a href="gg269213(v=exchg.10).md">(JET_coltypLongBinary o JET_coltypLongText</a>).</p> | 
| <p>JET_errCannotBeTagged</p> | <p>Se intentó usar una columna etiquetada cuando es posible que la columna no se etiquetase. Algunas de las restricciones para no permitir columnas etiquetadas son:</p><ul><li><p>No se puede usar una columna de actualización de custodia (JET_bitColumnEscrowUpdate) en una columna etiquetada o de valor largo<a href="gg269213(v=exchg.10).md">(</a> <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary o JET_coltypLongText</a>).</p></li><li><p>Es posible que una columna de autoincremento no se etiquete.</p></li><li><p>Es posible que una columna Versión no se etiquete.</p></li></ul> | 
| <p>JET_errExclusiveTableLockRequired</p> | <p>Se requiere un bloqueo exclusivo en la tabla para esta operación.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Advertencia que indica que la longitud máxima (<em>cbMax</em>) de una columna fija o variable era mayor que JET_cbColumnMost. Este límite no se aplica a los valores largos (es <a href="gg269213(v=exchg.10).md">decir,</a> JET_coltypLongBinary y <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p> | 



#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetAddColumnW</strong> (Unicode) y <strong>JetAddColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
