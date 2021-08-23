---
description: Desusado. Identifica si el año especificado es un año bisiesco dentro de la era especificada para el calendario específico.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: Función IsCalendarLeapYear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: fe89f11bbaf41235449e882626680cf4d4af075d93f76c2d2aacd90d8d38707a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948741"
---
# <a name="iscalendarleapyear-function"></a>Función IsCalendarLeapYear

En desuso. Identifica si el año especificado es un año bisiesco dentro de la era especificada para el calendario específico.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*calId* \[ En\]
</dt> <dd>

Identificador [del calendario que se](calendar-identifiers.md) va a usar para comprobar el año bisieste.

</dd> <dt>

*año* \[ En\]
</dt> <dd>

Año que se va a comprobar.

</dd> <dt>

*era* \[ En\]
</dt> <dd>

Era que se debe comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el año especificado es un año bisiesco o **FALSE** en caso contrario. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ PARÁMETRO NO \_ VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Comentarios

Esta función no tiene un archivo de encabezado o archivo de biblioteca asociado. La aplicación puede llamar [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre dll (Kernel32.dll) para obtener un identificador de módulo. A continuación, puede llamar [**a GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el nombre de esta función para obtener la dirección de la función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> </dl>

 

 
