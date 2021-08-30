---
description: Continúa una operación de búsqueda de archivos.
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: Función CSCFindNextFileW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindNextFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 99f3ed77dde867fecee6fd85b3a499fcd491f9fbef8b7a8aac0a5d7db5fe7550
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984425"
---
# <a name="cscfindnextfilew-function"></a>Función CSCFindNextFileW

\[Esta función no se admite y no se debe usar.\]

Continúa una operación de búsqueda de archivos.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CSCFindNextFileW(
  _In_  HANDLE           hFind,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _In_  FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFind* \[ En\]
</dt> <dd>

Identificador de búsqueda devuelto por la [**función CSCFindFirstFileW.**](cscfindfirstfilew.md)

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
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**FLAG \_ PIN DE SUGERENCIA CSC \_ \_ PIN \_ USER**</dt> <dt>0x01</dt> </dl>                                | Un usuario ha hecho que el archivo esté disponible sin conexión.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**FLAG \_ EL PIN \_ DE \_ SUGERENCIA CSC \_ \_ HEREDA LOS DATOS**</dt> <dt>0X02</dt> </dl>       | Un usuario ha hecho que el elemento primario esté disponible sin conexión y ha marcado el elemento primario para que sus elementos secundarios estén disponibles sin conexión.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**FLAG \_ EL PIN DE SUGERENCIA DE CSC \_ \_ \_ \_ HEREDA los**</dt> <dt>0x04</dt> </dl> | Una directiva de administrador o grupo ha hecho que el elemento primario esté disponible sin conexión y ha marcado el elemento primario para que sus elementos secundarios estén disponibles sin conexión.<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**FLAG \_ SISTEMA \_ DE PIN DE \_ \_ SUGERENCIAS CSC**</dt> <dt>0x10</dt> </dl>                          | Una directiva de administrador o grupo ha hecho que el archivo esté disponible sin conexión.<br/>                                                                      |



 

</dd> <dt>

*lpOrgFileTime* \[ En\]
</dt> <dd>

Puntero a una [**estructura FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para recibir la información de fecha y hora del archivo o subdirectorio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** se realiza correctamente; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
