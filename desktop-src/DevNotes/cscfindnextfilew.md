---
description: Continúa una operación de búsqueda de archivos.
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: CSCFindNextFileW función)
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
ms.openlocfilehash: 50b387a1ff99a95fcbe0fae8fe8ad93d14c335b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660703"
---
# <a name="cscfindnextfilew-function"></a>CSCFindNextFileW función)

\[Esta función no se admite y no debe usarse.\]

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

*hFind* \[ de\]
</dt> <dd>

Identificador de búsqueda devuelto por la función [**CSCFindFirstFileW**](cscfindfirstfilew.md) .

</dd> <dt>

*lpFind32* \[ enuncia\]
</dt> <dd>

Puntero a la estructura [**de \_ \_ datos de búsqueda de Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) que recibe información sobre el archivo o subdirectorio.

</dd> <dt>

*lpdwStatus* \[ enuncia\]
</dt> <dd>

Código NTSTATUS que indica el estado de la llamada.

</dd> <dt>

*lpdwPinCount* \[ enuncia\]
</dt> <dd>

Este parámetro es distinto de cero si el archivo está disponible sin conexión o 0 en caso contrario.

</dd> <dt>

*lpdwHintFlags* \[ enuncia\]
</dt> <dd>

Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                | Significado                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**Marca \_ de \_Usuario de \_ PIN \_ de sugerencia de CSC**</dt> <dt>0x01</dt> </dl>                                | Un usuario ha hecho que el archivo esté disponible sin conexión.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**Marca \_ de El \_ PIN de sugerencia de CSC \_ hereda el \_ \_ usuario**</dt> <dt>0x02</dt> </dl>       | Un usuario ha hecho que el elemento primario esté disponible sin conexión y marcado como primario para que sus elementos secundarios estén disponibles sin conexión.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**Marca \_ de El \_ PIN de sugerencia de CSC \_ hereda el \_ \_ sistema**</dt> <dt>0x04</dt> </dl> | Un administrador o una directiva de grupo ha hecho que el elemento primario esté disponible sin conexión y marcado como elemento primario para que sus elementos secundarios estén disponibles sin conexión.<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**Marca \_ de CSC \_ Hint \_ PIN \_ System**</dt> <dt>0x10</dt> </dl>                          | Un administrador o una directiva de grupo ha hecho que el archivo esté disponible sin conexión.<br/>                                                                      |



 

</dd> <dt>

*lpOrgFileTime* \[ de\]
</dt> <dd>

Un puntero a una estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para recibir la información de fecha y hora para el archivo o subdirectorio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
