---
description: Desusado. Convierte una estructura SYSTEMTIME especificada en una estructura CALDATETIME.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: ConvertSystemTimeToCalDateTime función)
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
ms.openlocfilehash: 738899c7307797f0edeade93f7e4e706919be900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652709"
---
# <a name="convertsystemtimetocaldatetime-function"></a>ConvertSystemTimeToCalDateTime función)

En desuso. Convierte una estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) especificada en una estructura [**CALDATETIME**](caldatetime.md) .

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

*lpSysTime* \[ de\]
</dt> <dd>

Puntero a la estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que se va a convertir.

</dd> <dt>

*calId* \[ de\]
</dt> <dd>

Identificador del [calendario](calendar-identifiers.md) del sistema que se va a utilizar en la conversión.

</dd> <dt>

*lpCalDateTime* \[ enuncia\]
</dt> <dd>

Puntero a la estructura [**CALDATETIME**](caldatetime.md) equivalente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ de \_ parámetro no válido. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

La primera fecha admitida por esta función es el 1 de enero de 1601.

Esta función no tiene asociado un archivo de encabezado o archivo de biblioteca. La aplicación puede llamar a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de DLL (Kernel32.dll) para obtener un identificador de módulo. Después, puede llamar a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con el identificador de módulo y el nombre de esta función para obtener la dirección de la función.

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
</dt> <dt>

[Recuperar información de fecha y hora](time-and-date.md)
</dt> </dl>

 

 
