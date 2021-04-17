---
description: En la tabla siguiente se enumeran los métodos CHString.
ms.assetid: e2e4378f-d842-4bca-bffc-a60e718caed3
ms.tgt_platform: multiple
title: Clase CHString (ChString. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CHString
- ??1CHString@@QAE@XZ
- ??1CHString@@QEAA@XZ
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 0c94fcd89a41e610d039afe17f4b56e58cb117bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697596"
---
# <a name="chstring-class"></a>Clase CHString

\[La clase **CHString** forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

En la tabla siguiente se enumeran los métodos **CHString** .

## <a name="members"></a>Miembros

La clase **CHString** tiene estos tipos de miembros:

-   [Constructores](#constructors)
-   [Métodos](#methods)
-   [Operadores](#operators)

### <a name="constructors"></a>Constructores

La clase **CHString** tiene estos constructores.



| Constructor                           | Descripción                                                 |
|:--------------------------------------|:------------------------------------------------------------|
| [**CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_)) | Construye cadenas **CHString** de varias maneras.<br/> |



 

### <a name="methods"></a>Métodos

La clase **CHString** tiene estos métodos.



| Método                                                    | Descripción                                                                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)         | Asigna un BSTR a partir de datos **CHString** .<br/>                                                            |
| [**COLLATE**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)                       | Compara dos cadenas (distingue mayúsculas de minúsculas; usa información específica de la configuración regional).<br/>                            |
| [**Comparar**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)                       | Compara dos cadenas (distingue mayúsculas de minúsculas).<br/>                                                              |
| [**CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)           | Compara dos cadenas (no distingue mayúsculas de minúsculas).<br/>                                                            |
| [**Vacía**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)                           | Fuerza que una cadena tenga una longitud de 0 (cero).<br/>                                                            |
| [**Buscar**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))                        | Sobrecargado. Busca un carácter o subcadena dentro de una cadena más grande.<br/>                                  |
| [**FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)                   | Busca el primer carácter coincidente de un conjunto.<br/>                                                      |
| [**Aplique**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))                         | Sobrecargado. Da formato a la cadena como **sprintf** .<br/>                                                 |
| [**FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))         | Sobrecargado. Da formato a una cadena de mensaje.<br/>                                                               |
| [**FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)                       | Da formato a la cadena como **vsprintf** .<br/>                                                            |
| [**FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)                   | Quita cualquier sobrecarga de esta cadena liberando cualquier memoria adicional asignada previamente a la cadena.<br/> |
| [**GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)         | Devuelve el tamaño del búfer de cadena.<br/>                                                              |
| [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))                           | Sobrecargado. Devuelve el carácter que se encuentra en una posición determinada.<br/>                                              |
| [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)                   | Devuelve un puntero a los caracteres de la cadena **CHString** .<br/>                                     |
| [**GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength) | Devuelve un puntero a los caracteres de la cadena **CHString** y se trunca a la longitud especificada.<br/> |
| [**GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)                       | Devuelve un puntero a los datos de la cadena **CHString** .<br/>                                           |
| [**GetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)                   | Devuelve el número de caracteres Unicode de una cadena **CHString** .<br/>                                  |
| [**Vacío**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)                       | Comprueba si una cadena de **CHString** no contiene caracteres.<br/>                                         |
| [**Salido**](/windows/desktop/api/ChString/nf-chstring-chstring-left)                             | Extrae la parte izquierda de una cadena (como la función **$ left** básica).<br/>                             |
| [**LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))               | Carga una cadena de **CHString** existente desde un archivo de recursos.<br/>                                         |
| [**LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)                 | Deshabilita el recuento de referencias y protege la cadena en el búfer.<br/>                                  |
| [**MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)                   | Convierte todos los caracteres de esta cadena en caracteres en minúsculas.<br/>                              |
| [**MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)               | Invierte los caracteres de esta cadena.<br/>                                                             |
| [**MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)                   | Convierte todos los caracteres de esta cadena en caracteres en mayúsculas.<br/>                              |
| [**Mid**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))                               | Sobrecargado. Extrae la parte intermedia de una cadena (como la función básica **Mid $** ).<br/>                |
| [**ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)           | Libera el control del búfer devuelto por [**getBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer).<br/>                 |
| [**ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)               | Busca un carácter dentro de una cadena más grande; comienza desde el final.<br/>                                      |
| [**Correcta**](/windows/desktop/api/ChString/nf-chstring-chstring-right)                           | Extrae la parte derecha de una cadena (como la función **$ right** básica).<br/>                           |
| [**SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)                           | Establece un carácter en una posición determinada.<br/>                                                               |
| [**SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)           | Extrae una subcadena que contiene solo los caracteres que no están en el conjunto.<br/>                     |
| [**SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)           | Extrae una subcadena que contiene solo los caracteres de un conjunto.<br/>                                    |
| [**TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)                     | Recorta los caracteres de espacio en blanco iniciales de la cadena.<br/>                                                |
| [**TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)                   | Recorta los caracteres de espacio en blanco finales de la cadena.<br/>                                               |
| [**UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)             | Habilita el recuento de referencias y libera la cadena en el búfer.<br/>                                   |



 

### <a name="operators"></a>Operadores
`
The **CHString** class has these operators.`



| Operator                                                                                            | Descripción                                                                                                       |
|:----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| [**Operator! = (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))            | Compara dos **CHStrings** para determinar si no son iguales.<br/>                                                             |
| [**Operator! = (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))              | Compara un **CHString** con un **LPCWSTR** para determinar si no son iguales.<br/>                                             |
| [**Operator \[\]**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))                                                | Devuelve el carácter que se encuentra en una sustitución de operador de posición determinada para [**GetAd**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int)).<br/> |
| [**operador +**](chstring--operator-plus.md)                                                       | Concatena dos cadenas y devuelve una nueva cadena.<br/>                                                     |
| [**operador + =**](chstring--operator-plus-equal.md)                                                | Concatena una nueva cadena al final de una cadena existente.<br/>                                            |
| [**operador < (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))            | Compara un **CHString** con un **LPCWSTR**.<br/>                                                            |
| [**operador < (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))          | Compara dos **CHStrings**.<br/>                                                                            |
| [**operador <= (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))    | Compara dos **CHStrings**.<br/>                                                                            |
| [**operador <= (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))      | Compara un **CHString** con un **LPCWSTR**.<br/>                                                            |
| [**operador =**](chstring--operator-equal.md)                                                      | Asigna un nuevo valor a una cadena **CHString** .<br/>                                                          |
| [**operador = = (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))          | Compara dos **CHStrings** para determinar si son iguales.<br/>                                                               |
| [**operador = = (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))            | Compara un **CHString** con **LPCWSTR** para determinar si son iguales.<br/>                                               |
| [**operador > (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))       | Compara dos **CHStrings**.<br/>                                                                            |
| [**operador > (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))         | Compara un **CHString** con un **LPCWSTR**.<br/>                                                            |
| [**operador >= (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85)) | Compara dos **CHStrings**.<br/>                                                                            |
| [**operador >= (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))   | Compara un **CHString** con un **LPCWSTR**.<br/>                                                            |
| [**operador LPCWSTR**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)                                               | Accede directamente a los caracteres almacenados en una cadena **CHString** como una cadena de estilo C.<br/>                      |



 

## <a name="remarks"></a>Observaciones

El destructor de la clase es **CHString:: ~ CHString**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>ChString. h (incluye FwCommon. h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



