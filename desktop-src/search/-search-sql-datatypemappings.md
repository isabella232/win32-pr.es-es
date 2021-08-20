---
description: En la tabla siguiente se enumeran las asignaciones entre tipos de datos variantes OLE DB tipos de datos.
ms.assetid: 213458bf-b847-4ced-8a92-686b4eee6d07
title: Asignaciones de tipo de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e25e909755c87b15526b97488285a0cf688e15dab64073fad603efc190f382b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462599"
---
# <a name="data-type-mappings"></a>Asignaciones de tipo de datos

En la tabla siguiente se enumeran las asignaciones entre tipos de datos variantes OLE DB tipos de datos.




| Tipo de datos variant | Tipo de datos de OLE DB |
|-------------------|------------------|
| VT \_ BOOL          | DBTYPE \_ BOOL     |
| VT \_ BSTR          | DBTYPE \_ BSTR     |
| VT \_ BYREF         | DBTYPE \_ BYREF    |
| VT \_ CY            | DBTYPE \_ CY       |
| VT \_ DATE          | DBTYPE \_ DATE     |
| VT \_ DECIMAL       | DBTYPE \_ DECIMAL  |
| VT \_ EMPTY         | DBTYPE \_ EMPTY    |
| VT \_ FILETIME      | DBTYPE \_ FILETIME |
| \_GUID de VT          | GUID \_ de DBTYPE     |
| VT \_ I1            | DBTYPE \_ I1       |
| VT \_ I2            | DBTYPE \_ I2       |
| VT \_ I4            | DBTYPE \_ I4       |
| VT \_ I8            | DBTYPE \_ I8       |
| VT \_ NULL          | DBTYPE \_ NULL     |
| VT \_ R4            | DBTYPE \_ R4       |
| VT \_ R8            | DBTYPE \_ UI8      |
| VT \_ VECTOR        | DBTYPE \_ VECTOR   |
| VT \_ WSTR          | DBTYPE \_ WSTR     |



 

En la tabla siguiente se enumeran las asignaciones entre los tipos de datos XML OLE DB tipos de datos.



| Tipo de datos variant | Tipo de datos de OLE DB |
|-------------------|------------------|
| Bin. BASE64        | DBTYPE \_ BYTES    |
| Bin. Hexagonal           | DBTYPE \_ I8       |
| BOOLEAN           | DBTYPE \_ BOOL     |
| CHAR              | DBTYPE \_ STR      |
| DATE              | DBTYPE \_ DATE     |
| DATETIME          | DBTYPE \_ DATE     |
| Datetime. Tz       | DBTYPE \_ DATE     |
| FIXED.14.4        | DBTYPE \_ R4       |
| FLOAT             | DBTYPE \_ R8       |
| I1                | DBTYPE \_ I1       |
| I2                | DBTYPE \_ I2       |
| I4                | DBTYPE \_ I4       |
| I8                | DBTYPE \_ I8       |
| INT               | DBTYPE \_ I8       |
| LONG              | DBTYPE \_ I4       |
| NUMBER            | DBTYPE \_ R8       |
| R4                | DBTYPE \_ R4       |
| R8                | DBTYPE \_ R8       |
| STRING            | DBTYPE \_ WSTR     |
| TIME              | DBTYPE \_ FILETIME |
| hora. Tz           | DBTYPE \_ FILETIME |
| UI1               | DBTYPE \_ UI2      |
| UI2               | DBTYPE \_ UI2      |
| UI4               | DBTYPE \_ UI4      |
| UI8               | DBTYPE \_ UI8      |
| Identificador URI               | DBTYPE \_ WSTR     |
| UUID              | GUID \_ de DBTYPE     |



 

Puede convertir datos de cadena a otros tipos de datos. Para obtener más información, consulte [Conversión del tipo de datos de una columna](-search-sql-castingdatacolumntype.md).

 

 



