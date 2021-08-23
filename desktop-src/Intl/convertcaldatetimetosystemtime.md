---
description: Desusado. Convierte una estructura CALDATETIME especificada en una estructura SYSTEMTIME.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: Función ConvertCalDateTimeToSystemTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: cb579eb80c421d6f206045889edfe3f1b64130f58d02d96c61b3867abcaabb75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631935"
---
# <a name="convertcaldatetimetosystemtime-function"></a>Función ConvertCalDateTimeToSystemTime

En desuso. Convierte una estructura [**CALDATETIME especificada**](caldatetime.md) en una [**estructura SYSTEMTIME.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)

## <a name="syntax"></a>Sintaxis


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpCalDateTime* \[ En\]
</dt> <dd>

Puntero a la [**estructura CALDATETIME que**](caldatetime.md) se convertirá.

</dd> <dt>

*lpSysTime* \[ out\]
</dt> <dd>

Puntero a la estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) equivalente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   FECHA \_ DE ERROR FUERA DEL \_ \_ \_ INTERVALO. La fecha especificada estaba fuera del intervalo.
-   ERROR \_ PARÁMETRO \_ NO VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Comentarios

Esta función no tiene un archivo de encabezado o un archivo de biblioteca asociados. La aplicación puede llamar [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre dll (Kernel32.dll) para obtener un identificador de módulo. A continuación, puede llamar [**a GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con el identificador del módulo y el nombre de esta función para obtener la dirección de la función.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> <dt>

[Recuperar información de fecha y hora](time-and-date.md)
</dt> </dl>

 

 
