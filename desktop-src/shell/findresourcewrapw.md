---
description: Determina la ubicación de un recurso con el tipo y el nombre especificados, en el módulo especificado.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: Función FindResourceWrapW
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
ms.openlocfilehash: bfd640aaf0bbc68e8798f62f41542d794db34808674c0bdb47587c7396ad7bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094200"
---
# <a name="findresourcewrapw-function"></a>Función FindResourceWrapW

\[**FindResourceWrapW** está disponible para su uso en Windows XP. Es posible que no esté disponible en versiones posteriores. En su lugar, [**debe usar FindResourceW.**](/windows/win32/api/winbase/nf-winbase-findresourcea)\]

Determina la ubicación de un recurso con el tipo y el nombre especificados, en el módulo especificado.

> [!Note]  
> **FindResourceWrapW es** un contenedor de la **función FindResourceW.** Consulte [**FindResource para**](/windows/win32/api/winbase/nf-winbase-findresourcea) obtener más notas de uso.

 

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

*hModule* \[ En\]
</dt> <dd>

Tipo: **HMODULE**

Identificador del módulo cuyo archivo ejecutable contiene el recurso. Un valor **NULL especifica** el identificador de módulo asociado al archivo de imagen que el sistema operativo usó para crear el proceso actual.

</dd> <dt>

*lpName* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Nombre del recurso. Para obtener más información, [**vea FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> <dt>

*lpType* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena que especifica el tipo de recurso. Para obtener más información, [**vea FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRSRC**

Si la función se realiza correctamente, el valor devuelto es un identificador del bloque de información del recurso especificado. Para obtener un identificador para el recurso, pase este identificador a la [**función LoadResource.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)

Si se produce un error en la función, el valor devuelto es **NULL.** Para obtener información de error extendida, llame a [**la función GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentarios

Si necesita especificar una localización determinada, use la [**función FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) en lugar de **FindResourceWrapW.**

**FindResourceWrapW proporciona** la capacidad de usar cadenas Unicode en sistemas operativos anteriores. El método preferido es usar [**FindResourceW junto**](/windows/win32/api/winbase/nf-winbase-findresourcea) con la capa de Microsoft para Unicode (MSLU).

**Se debe llamar a FindResourceWrapW** directamente Shlwapi.dll, mediante ordinal 66.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>None</dt> </dl>                               |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5.0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **FindResourceWrapW** (Unicode)<br/>                                                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
