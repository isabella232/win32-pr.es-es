---
description: Determina la ubicación de un recurso con el tipo y el nombre especificados, en el módulo especificado.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: FindResourceWrapW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276764"
---
# <a name="findresourcewrapw-function"></a>FindResourceWrapW función)

\[**FindResourceWrapW** está disponible para su uso en Windows XP. Puede que no esté disponible en versiones posteriores. En su lugar, debe usar [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) .\]

Determina la ubicación de un recurso con el tipo y el nombre especificados, en el módulo especificado.

> [!Note]  
> **FindResourceWrapW** es un contenedor para la función **FindResourceW** . Consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) para obtener más notas sobre el uso.

 

## <a name="syntax"></a>Sintaxis


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hModule* \[ de\]
</dt> <dd>

Tipo: **HMODULE**

Identificador del módulo cuyo archivo ejecutable contiene el recurso. Un valor **null** especifica el identificador de módulo asociado al archivo de imagen que el sistema operativo usó para crear el proceso actual.

</dd> <dt>

*lpName* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Nombre del recurso. Para obtener más información, vea [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> <dt>

*lpType* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena que especifica el tipo de recurso. Para obtener más información, vea [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRSRC**

Si la función se ejecuta correctamente, el valor devuelto es un identificador del bloque de información del recurso especificado. Para obtener un identificador para el recurso, pase este identificador a la función [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .

Si se produce un error en la función, el valor devuelto es **null**. Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Observaciones

Si necesita especificar una localización determinada, use la función [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) en lugar de **FindResourceWrapW**.

**FindResourceWrapW** ofrece la posibilidad de usar cadenas Unicode en sistemas operativos anteriores. El método preferido es usar [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) junto con la capa de Microsoft para Unicode (MSLU).

Se debe llamar a **FindResourceWrapW** directamente desde Shlwapi.dll, mediante el ordinal 66.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>None</dt> </dl>                               |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5,0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **FindResourceWrapW** (Unicode)<br/>                                                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
