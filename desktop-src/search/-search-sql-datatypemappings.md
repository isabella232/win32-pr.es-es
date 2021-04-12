---
description: En la tabla siguiente se enumeran las asignaciones entre los tipos de datos Variant y los tipos de datos OLE DB.
ms.assetid: 213458bf-b847-4ced-8a92-686b4eee6d07
title: Asignaciones de tipos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9beae5a9ce1fbaafadfae54979d63c97310f57db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153963"
---
# <a name="data-type-mappings"></a>Asignaciones de tipos de datos

En la tabla siguiente se enumeran las asignaciones entre los tipos de datos Variant y los tipos de datos OLE DB.




| Variant (tipo de datos) | Tipo de datos de OLE DB |
|-------------------|------------------|
| VT \_ bool          | DBTYPE \_ bool     |
| VT \_ BSTR          | BSTR de DBTYPE \_     |
| VT \_ BYREF         | DBTYPE \_ BYREF    |
| VT \_ CY            | DBTYPE \_ CY       |
| fecha de VT \_          | fecha del DBTYPE \_     |
| VT \_ decimal       | DBTYPE \_ decimal  |
| VT \_ vacío         | DBTYPE \_ vacío    |
| VT \_ FILETIME      | DBTYPE \_ FILETIME |
| GUID de VT \_          | GUID de DBTYPE \_     |
| VT \_ I1            | DBTYPE \_ I1       |
| I2 de VT \_            | I2 de DBTYPE \_       |
| VT \_ I4            | DBTYPE \_ I4       |
| VT \_ i8            | DBTYPE \_ i8       |
| VT \_ null          | DBTYPE \_ null     |
| VT \_ R4            | DBTYPE \_ R4       |
| VT \_ R8            | DBTYPE \_ UI8      |
| \_Vector VT        | \_Vector DbType   |
| VT \_ WSTR          | DBTYPE \_ WSTR     |



 

En la tabla siguiente se enumeran las asignaciones entre los tipos de datos XML y los tipos de datos de OLE DB.



| Variant (tipo de datos) | Tipo de datos de OLE DB |
|-------------------|------------------|
| BIN. BASE64        | \_bytes DbType    |
| BIN. HUECA           | DBTYPE \_ i8       |
| BOOLEAN           | DBTYPE \_ bool     |
| CHAR              | Str de DBTYPE \_      |
| DATE              | fecha del DBTYPE \_     |
| DATETIME          | fecha del DBTYPE \_     |
| DateTime. TZ       | fecha del DBTYPE \_     |
| SOLUCIONAdo. 14.4        | DBTYPE \_ R4       |
| FLOAT             | DBTYPE \_ R8       |
| I1                | DBTYPE \_ I1       |
| I2                | I2 de DBTYPE \_       |
| I4                | DBTYPE \_ I4       |
| I8                | DBTYPE \_ i8       |
| INT               | DBTYPE \_ i8       |
| LONG              | DBTYPE \_ I4       |
| NUMBER            | DBTYPE \_ R8       |
| R4                | DBTYPE \_ R4       |
| R8                | DBTYPE \_ R8       |
| STRING            | DBTYPE \_ WSTR     |
| TIME              | DBTYPE \_ FILETIME |
| Tiempo. TZ           | DBTYPE \_ FILETIME |
| UI1               | DBTYPE \_ UI2      |
| UI2               | DBTYPE \_ UI2      |
| UI4               | DBTYPE \_ UI4      |
| UI8               | DBTYPE \_ UI8      |
| URI               | DBTYPE \_ WSTR     |
| UUID              | GUID de DBTYPE \_     |



 

Puede convertir datos de cadena en otros tipos de datos. Para obtener más información, consulte [conversión del tipo de datos de una columna](-search-sql-castingdatacolumntype.md).

 

 



