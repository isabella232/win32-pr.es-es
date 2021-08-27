---
description: 'Más información sobre: EnumerateColumnsGrbit (enumeración)'
title: EnumerateColumnsGrbit (enumeración)
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1e6f768d2f8a837416540bcd3ca31f8984e55ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466812"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>EnumerateColumnsGrbit (enumeración)

Opciones de JetEnumerateColumns.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a>Miembros


|  | Nombre del miembro | Descripción | 
|--|-------------|-------------|
|  | Ninguno | Opciones predeterminadas. | 
|  | EnumerateCompressOutput | Al enumerar valores de columna, todas las columnas para las que se recuperan todos los valores y que tienen solo un valor de columna distinto de NULL se pueden devolver en un formato comprimido. El estado de estas columnas se establecerá en <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> y el tamaño del valor de columna y la memoria que contiene el valor de columna se devolverán directamente en la <a href="dn335081(v=exchg.10).md">estructura JET_ENUMCOLUMN</a> columna. No se garantiza que todas las columnas aptas se comprimen de esta manera. Consulte <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> para obtener más información. | 
|  | EnumerateCopy | Esta opción indica que los valores de columna modificados del registro deben enumerarse en lugar de los valores de columna originales. Si no se ha modificado un valor de columna, se enumera el valor de columna original. De esta manera, se puede enumerar un valor de columna que aún no se ha insertado o actualizado al insertar o actualizar un registro.<p>Esta opción es idéntica a <a href="hh578120(v=exchg.10).md">RetrieveCopy.</a></p> | 
|  | EnumerateIgnoreDefault | Si una columna determinada no está presente en el registro, no se devolverá ningún valor de columna. Normalmente, el valor predeterminado de la columna, si lo hubiera, se devolvería en este caso. Se garantiza que si la columna se establece en un valor diferente del valor predeterminado, se devolverá ese valor diferente (es decir, si una columna con un valor predeterminado se establece explícitamente en NULL, se devolverá un valor NULL como valor de esa columna). Incluso si se solicita esta opción, todavía es posible ver un valor de columna que resulta ser igual al valor predeterminado. No se realiza ningún esfuerzo para quitar valores de columna que coincidan con sus valores predeterminados. Es importante recordar que esta opción afecta a la salida de <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> cuando se usa con EnumeratePresenceOnly o EnumerateTaggedOnly. | 
|  | EnumeratePresenceOnly | Si existe un valor distinto de NULL para el valor de columna o columna solicitado, no se devuelven los datos asociados. En su lugar, el estado asociado para ese valor de columna o columna se establecerá en <a href="hh557250(v=exchg.10).md">ColumnPresent</a>. Si el valor de columna o columna es NULL, <a href="hh557250(v=exchg.10).md">ColumnNull</a> se devolverá como de costumbre. | 
|  | EnumerateTaggedOnly | Al enumerar todos los valores de columna del registro (por ejemplo, cuando numColumnids es cero), solo se devolverán los valores de columna etiquetados. Esta opción no se permite al enumerar una matriz específica de id. de columna. | 



## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

[EnumerateIgnoreUserDefinedDefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[EnumerateInRecordOnly](./windows7grbits.enumerateinrecordonly-field.md)
