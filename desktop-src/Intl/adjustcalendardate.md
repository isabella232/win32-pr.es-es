---
description: Desusado. Ajusta una fecha según un número especificado de años, meses, semanas o días.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: Función AdjustCalendarDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 061d0e246f7839345b0f1e55221d26d276f52af4997a7cb47d62b680d2638fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520625"
---
# <a name="adjustcalendardate-function"></a>Función AdjustCalendarDate

En desuso. Ajusta una fecha según un número especificado de años, meses, semanas o días.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpCalDateTime* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura CALDATETIME**](caldatetime.md) que contiene la información de fecha y calendario que se debe ajustar.

</dd> <dt>

*calUnit* \[ En\]
</dt> <dd>

Valor [**de enumeración \_ CALDATETIME DATEUNIT**](caldatetime-dateunit.md) que indica la unidad de fecha, por ejemplo, DayUnit.

</dd> <dt>

*amount* \[ out\]
</dt> <dd>

Cantidad por la que se va a ajustar la fecha especificada.

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

[NLS: ejemplo de API basadas en nombres](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
