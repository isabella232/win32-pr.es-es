---
description: Desusado. Convierte una estructura SYSTEMTIME especificada en una estructura CALDATETIME.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: Función ConvertSystemTimeToCalDateTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 01eb78f9045e43db3e97b252a8fdf8fe8ed7297905174efeff2f3b2bbe1a5171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746045"
---
# <a name="convertsystemtimetocaldatetime-function"></a>Función ConvertSystemTimeToCalDateTime

En desuso. Convierte una estructura [**SYSTEMTIME especificada**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) en una [**estructura CALDATETIME.**](caldatetime.md)

## <a name="syntax"></a>Sintaxis


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpSysTime* \[ En\]
</dt> <dd>

Puntero a la [**estructura SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que se convertirá.

</dd> <dt>

*calId* \[ En\]
</dt> <dd>

Identificador del [calendario del sistema que](calendar-identifiers.md) se usará en la conversión.

</dd> <dt>

*lpCalDateTime* \[ out\]
</dt> <dd>

Puntero a la estructura [**CALDATETIME**](caldatetime.md) equivalente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ PARÁMETRO \_ NO VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Comentarios

La fecha más temprana admitida por esta función es el 1 de enero de 1601.

Esta función no tiene un archivo de encabezado o un archivo de biblioteca asociados. La aplicación puede llamar [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre dll (Kernel32.dll) para obtener un identificador de módulo. A continuación, puede llamar [**a GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con el identificador del módulo y el nombre de esta función para obtener la dirección de la función.

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
</dt> <dt>

[Recuperar información de fecha y hora](time-and-date.md)
</dt> </dl>

 

 
