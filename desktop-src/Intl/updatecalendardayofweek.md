---
description: Desusado. Obtiene el día de la semana que corresponde a un día especificado y rellena el miembro DayOfWeek en la estructura CALDATETIME especificada con ese valor.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: Función UpdateCalendarDayOfWeek
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254919"
---
# <a name="updatecalendardayofweek-function"></a>Función UpdateCalendarDayOfWeek

En desuso. Obtiene el día de la semana que corresponde a un día especificado y rellena el **miembro DayOfWeek** en la estructura [**CALDATETIME**](caldatetime.md) especificada con ese valor.

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

Puntero a la [**estructura CALDATETIME**](caldatetime.md) que contiene la fecha para la que se va a establecer el día de la semana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   FECHA \_ DE ERROR FUERA DEL \_ \_ \_ INTERVALO. La fecha especificada estaba fuera del intervalo.
-   ERROR \_ PARÁMETRO \_ NO VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

Esta función no tiene un archivo de encabezado o un archivo de biblioteca asociados. La aplicación puede llamar [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre dll (Kernel32.dll) para obtener un identificador de módulo. A continuación, puede llamar [**a GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el nombre de esta función para obtener la dirección de la función.

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

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
