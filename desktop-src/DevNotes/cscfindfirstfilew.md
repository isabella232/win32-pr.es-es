---
description: Busca un archivo en la caché Archivos sin conexión que cumpla los criterios especificados.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: Función CSCFindFirstFileW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 7289fb19a0062ce66212927bbe3e77c9e90c54ceb1980f83265000cc228e27ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833415"
---
# <a name="cscfindfirstfilew-function"></a>Función CSCFindFirstFileW

\[Esta función no se admite y no se debe usar.\]

Busca un archivo en la caché Archivos sin conexión que cumpla los criterios especificados.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszFileName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica un directorio UNC o una ruta de acceso válidos.

</dd> <dt>

*lpFind32* \[ out\]
</dt> <dd>

Puntero a la estructura [**\_ FIND \_ DATA de WIN32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) que recibe información sobre el archivo o subdirectorio.

</dd> <dt>

*lpdwStatus* \[ out\]
</dt> <dd>

Código NTSTATUS que indica el estado de la llamada.

</dd> <dt>

*lpdwPinCount* \[ out\]
</dt> <dd>

Este parámetro es distinto de cero si el archivo se ha puesto a disposición sin conexión o 0 en caso contrario.

</dd> <dt>

*lpdwHintFlags* \[ out\]
</dt> <dd>

Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                | Significado                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**FLAG \_ Pin DE SUGERENCIA CSC \_ \_ PIN \_ USER**</dt> <dt>0x01</dt> </dl>                                | Un usuario ha hecho que el archivo esté disponible sin conexión.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**FLAG \_ EL PIN \_ DE \_ SUGERENCIA CSC \_ \_ HEREDA LOS DATOS**</dt> <dt>0X02</dt> </dl>       | Un usuario ha hecho que el elemento primario esté disponible sin conexión y ha marcado el elemento primario para que sus elementos secundarios estén disponibles sin conexión.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**FLAG \_ EL \_ PIN DE SUGERENCIA CSC \_ \_ \_ HEREDA los**</dt> <dt>0x04</dt> </dl> | Una directiva de administrador o grupo ha hecho que el elemento primario esté disponible sin conexión y ha marcado el elemento primario para que sus elementos secundarios estén disponibles sin conexión.<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**FLAG \_ SISTEMA \_ DE PIN DE \_ \_ SUGERENCIAS CSC**</dt> <dt>0x10</dt> </dl>                          | Una directiva de administrador o grupo ha hecho que el archivo esté disponible sin conexión.<br/>                                                                      |



 

</dd> <dt>

*lpOrgFileTime* \[ out\]
</dt> <dd>

Puntero a una [**estructura FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para recibir la información de fecha y hora del archivo o subdirectorio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador de búsqueda utilizado en una llamada posterior a [**CSCFindNextFileW**](cscfindnextfilew.md) [**o CSCFindClose**](cscfindclose.md).

Si la función no se ejecuta correctamente, el valor devuelto es **INVALID\_HANDLE\_VALUE**.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
