---
description: Desusado. Obtiene el intervalo de fechas admitido para un calendario especificado.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: GetCalendarSupportedDateRange función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002379"
---
# <a name="getcalendarsupporteddaterange-function"></a>GetCalendarSupportedDateRange función)

En desuso. Obtiene el intervalo de fechas admitido para un calendario especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Calendario* \[ de de\]
</dt> <dd>

[Identificador de calendario](calendar-identifiers.md) para el que se va a obtener el intervalo de fechas admitido.

</dd> <dt>

*lpCalMinDateTime* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**CALDATETIME**](caldatetime.md) que define la fecha mínima admitida.

</dd> <dt>

*lpCalMaxDateTime* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**CALDATETIME**](caldatetime.md) que define la fecha máxima admitida.

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

[NLS: ejemplo de API basadas en nombre](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
