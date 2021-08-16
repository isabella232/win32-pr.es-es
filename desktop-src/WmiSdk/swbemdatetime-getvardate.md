---
description: Convierte un valor de fecha y hora en el formato CIM DATETIME al formato \_ VT DATE.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Método SWbemDateTime.GetVarDate (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 506c897da130b9558b37637918674a7c6024adb787ac3d91e53e430a6edfcd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314760"
---
# <a name="swbemdatetimegetvardate-method"></a>Método SWbemDateTime.GetVarDate

El **método GetVarDate** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte un valor de fecha y hora en el formato [**CIM DATETIME**](datetime.md) al formato VT **\_ DATE.**

El **formato \_ VT DATE** es un valor [**DATETIME**](datetime.md) de variante de automatización que Visual Basic y ActiveX usar.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bIsLocal* \[ en, opcional\]
</dt> <dd>

Indica si el valor devuelto se interpreta como hora local. La propiedad Hora universal coordinada (UTC) contiene la hora local convertida al desplazamiento UTC correcto. Si el valor es **FALSE,** el valor se interpreta como UTC con un desplazamiento de cero (0).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor de fecha y hora en formato **\_ VT DATE.**

## <a name="remarks"></a>Comentarios

**VT \_ Los valores DATE** **y FILETIME** no pueden contener campos comodín.

Se produce un error en el método **GetVarDate** (**wbemErrFailed**) si alguna de las siguientes propiedades es **FALSE**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosegundosEspecificado**](swbemdatetime-microsecondsspecified.md)
-   [**UTCEspecificado**](swbemdatetime-utcspecified.md)

Si la devolución de [**SetVarDate**](swbemdatetime-setvardate.md)se realiza correctamente, todas estas propiedades se establecen en **TRUE.**

Después de una llamada correcta a [**SetVarDate**](swbemdatetime-setvardate.md), el valor [**DATETIME**](datetime.md) siempre se interpreta como un valor **DATETIME** absoluto en lugar de un intervalo, y [**IsInterval**](swbemdatetime-isinterval.md) se establece en **FALSE.**

Si [**IsInterval**](swbemdatetime-isinterval.md) se establece en **TRUE,** una llamada a **GetVarDate** produce el error **wbemErrFailed.**

Algunas pérdidas de precisión se producen cuando se llama a **GetVarDate,** porque los valores [datetime](datetime.md) tienen una resolución de un microsegundos (s) y los valores **VT \_ DATE** tienen una resolución de 500 milisegundos.

## <a name="examples"></a>Ejemplos

Para obtener ejemplos de cómo usar el objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores [**DATETIME**](datetime.md) de CIM a y desde el formato **FILETIME** o **VT \_ DATE,** vea [Wmi Tasks: Dates and Times](wmi-tasks--dates-and-times.md). Para obtener una descripción del formato **DATETIME de** CIM, vea [Formato de fecha y hora](date-and-time-format.md).

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemDateTime.GetFileTime**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




