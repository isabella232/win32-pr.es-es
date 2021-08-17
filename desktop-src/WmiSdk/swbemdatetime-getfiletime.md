---
description: Convierte un valor de fecha y hora en el formato CIM DATETIME al formato FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Método SWbemDateTime.GetFileTime (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8c35daf5b6e986b2519f127969edc5bbcf05a260bd23e8aa1168b1a7c20a5372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739451"
---
# <a name="swbemdatetimegetfiletime-method"></a>Método SWbemDateTime.GetFileTime

El **método GetFileTime** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte un valor de fecha y hora en el formato [DATETIME](datetime.md) cim al formato FILETIME.

Si el parámetro se establece en **TRUE**, el valor devuelto representa una hora local para el cliente. De lo contrario, el valor devuelto es una hora universal coordinada (UTC). Una **estructura FILETIME** [DATETIME](datetime.md) es un valor de 64 bits que representa el número de unidades de 100 nanosegundos desde el 1 de enero de 1601. Windows Instrumental de administración (WMI) trata los valores **FILETIME** como representaciones de cadena de números de 64 bits sin signo.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bIsLocaL* \[ in, opcional\]
</dt> <dd>

Indica si el valor devuelto se interpreta como hora local. A continuación, la propiedad UTC contiene la hora local convertida en el desplazamiento de hora universal coordinada (UTC) correcto. Si el valor es **FALSE**, el valor se interpreta como UTC con un desplazamiento de cero (0).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Fecha y hora en formato **FILETIME.**

## <a name="error-codes"></a>Códigos de error

Después de completar el **método GetFileTime,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error en la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Se produjo un error en la llamada.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**VT \_ Los valores DATE** **y FILETIME** no pueden contener campos comodín.

Se produce un error **en el método GetFileTime** (wbemErrFailed) si alguna de las siguientes propiedades es **FALSE**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosegundosSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCEspecificado**](swbemdatetime-utcspecified.md)

En una devolución correcta de [**SetFileTime,**](swbemdatetime-setfiletime.md)todas estas propiedades se establecen en **TRUE.**

## <a name="examples"></a>Ejemplos

Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores [**DATETIME**](datetime.md) de CIM a y desde el formato **FILETIME** o el formato **VT \_ DATE,** vea [Tareas wmi:](wmi-tasks--dates-and-times.md)fechas y horas. Para obtener una descripción del formato **CIM DATETIME,** vea [Formato de fecha y hora](date-and-time-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemDateTime.GetVarDate**](swbemdatetime-getvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

