---
description: Desusado. Identifica si el año especificado es un año bisiesto dentro de la era especificada para el calendario específico.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: IsCalendarLeapYear función)
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
ms.openlocfilehash: 484531f8107bacb70f9e24ba2537090317825e26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910109"
---
# <a name="iscalendarleapyear-function"></a>IsCalendarLeapYear función)

En desuso. Identifica si el año especificado es un año bisiesto dentro de la era especificada para el calendario específico.

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

*calId* \[ de\]
</dt> <dd>

[Identificador del calendario](calendar-identifiers.md) que se va a usar para comprobar el año bisiesto.

</dd> <dt>

*año* \[ de\]
</dt> <dd>

Año que se va a comprobar.

</dd> <dt>

*era* \[ de\]
</dt> <dd>

La era que se va a comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el año especificado es un año bisiesto o **false** en caso contrario. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ de \_ parámetro no válido. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado un archivo de encabezado o archivo de biblioteca. La aplicación puede llamar a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de DLL (Kernel32.dll) para obtener un identificador de módulo. Después, puede llamar a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el nombre de esta función para obtener la dirección de la función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con National Language](national-language-support.md)
</dt> <dt>

[Funciones de soporte de National Language](national-language-support-functions.md)
</dt> </dl>

 

 
