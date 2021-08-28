---
description: Desusado. Obtiene el intervalo de fechas admitido para un calendario especificado.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: Función GetCalendarSupportedDateRange
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
ms.openlocfilehash: cf665b2591702b1b833cccb392c7345c1d76d44d324fabc214192c012c60f785
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765455"
---
# <a name="getcalendarsupporteddaterange-function"></a>Función GetCalendarSupportedDateRange

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

*Calendario* \[ En\]
</dt> <dd>

[Identificador de calendario](calendar-identifiers.md) para el que se va a obtener el intervalo de fechas admitido.

</dd> <dt>

*lpCalMinDateTime* \[ out\]
</dt> <dd>

Puntero a una [**estructura CALDATETIME**](caldatetime.md) que define la fecha mínima admitida.

</dd> <dt>

*lpCalMaxDateTime* \[ out\]
</dt> <dd>

Puntero a una [**estructura CALDATETIME**](caldatetime.md) que define la fecha máxima admitida.

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

[NLS: ejemplo de API basadas en nombres](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
