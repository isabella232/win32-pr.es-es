---
description: Convierte un valor de fecha y hora en el formato de fecha y hora de CIM al formato FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Método SWbemDateTime. GetFileTime (Wbemdisp. h)
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
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498052"
---
# <a name="swbemdatetimegetfiletime-method"></a>SWbemDateTime. GetFileTime, método

El método **GetFileTime** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte un valor de fecha y hora en el formato de fecha y hora [de CIM al](datetime.md) formato FILETIME.

Si el parámetro se establece en **true**, el valor devuelto representa una hora local para el cliente. De lo contrario, el valor devuelto es una hora UTC (hora universal coordinada). Una estructura de [fecha y hora](datetime.md) de **FILETIME** es un valor de 64 bits que representa el número de unidades de 100-nanosegundos desde el comienzo del 1 de enero de 1601. Instrumental de administración de Windows (WMI) trata los valores de **FILETIME** como representaciones de cadena de números de bits 64 sin signo.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bIsLocaL* \[ en, opcional\]
</dt> <dd>

Indica si el valor devuelto se interpreta como hora local. A continuación, la propiedad UTC contiene la hora local convertida en el desplazamiento correcto de hora universal coordinada (UTC). Si el valor es **false**, el valor se interpreta como UTC con un desplazamiento de cero (0).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Fecha y hora en formato **FILETIME** .

## <a name="error-codes"></a>Códigos de error

Después de completar el método **GetFileTime** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Se produjo un error en la llamada.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**VT \_** Los valores Date y **FILETIME** no pueden contener campos comodín.

Se produce un error en el método **GetFileTime** (wbemErrFailed) si alguna de las siguientes propiedades es **falsa**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

En una devolución correcta de [**SetFileTime**](swbemdatetime-setfiletime.md), todas estas propiedades se establecen en **true**.

## <a name="examples"></a>Ejemplos

Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md). Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | \_ISWBEMDATETIME IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemDateTime. Getvardate (**](swbemdatetime-getvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

