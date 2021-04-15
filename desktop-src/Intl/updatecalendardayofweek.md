---
description: Desusado. Obtiene el día de la semana que corresponde a un día especificado y rellena el miembro DayOfWeek de la estructura CALDATETIME especificada con ese valor.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: UpdateCalendarDayOfWeek función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688703"
---
# <a name="updatecalendardayofweek-function"></a>UpdateCalendarDayOfWeek función)

En desuso. Obtiene el día de la semana que corresponde a un día especificado y rellena el miembro **DayOfWeek** de la estructura [**CALDATETIME**](caldatetime.md) especificada con ese valor.

## <a name="syntax"></a>Sintaxis


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpCalDateTime* \[ in, out\]
</dt> <dd>

Puntero a la estructura [**CALDATETIME**](caldatetime.md) que contiene la fecha para la que se va a establecer el día de la semana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   \_fecha \_ de error fuera \_ del \_ intervalo. La fecha especificada estaba fuera del intervalo.
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
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
