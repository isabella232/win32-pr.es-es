---
description: Convierte un valor de fecha y hora en el formato de fecha y hora de CIM en el formato de fecha de VT \_ .
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Método SWbemDateTime. Getvardate ((Wbemdisp. h)
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
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715746"
---
# <a name="swbemdatetimegetvardate-method"></a>SWbemDateTime. Getvardate (, método

El método **getvardate (** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte un valor de fecha y hora en el formato de fecha y hora [**de CIM al**](datetime.md) formato de **\_ fecha de VT** .

El formato de **\_ fecha VT** es un valor [**DateTime**](datetime.md) de la variante de automatización que Visual Basic y el uso de ActiveX.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

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

Indica si el valor devuelto se interpreta como hora local. La propiedad hora universal coordinada (UTC) contiene la hora local convertida en el desplazamiento UTC correcto. Si el valor es **false**, el valor se interpreta como UTC con un desplazamiento de cero (0).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor de fecha y hora en el formato de **\_ fecha de VT** .

## <a name="remarks"></a>Observaciones

**VT \_** Los valores Date y **FILETIME** no pueden contener campos comodín.

Se produce un error en el método **getvardate (** (**wbemErrFailed**) si alguna de las siguientes propiedades es **falsa**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

Todas estas propiedades se establecen en **true** si se devuelve correctamente desde [**SetVarDate**](swbemdatetime-setvardate.md).

Después de una llamada correcta a [**SetVarDate**](swbemdatetime-setvardate.md), el valor [**DateTime**](datetime.md) siempre se interpreta como un valor de **fecha y hora** absoluto en lugar de un intervalo, y [**IsInterval**](swbemdatetime-isinterval.md) se establece en **false**.

Si [**IsInterval**](swbemdatetime-isinterval.md) se establece en **true**, una llamada a **getvardate (** produce el error **wbemErrFailed** .

Se produce una pérdida de precisión cuando se llama a **getvardate (**, ya que los valores [DateTime](datetime.md) tienen una resolución de un microsegundo (s) y los valores de **\_ fecha de VT** tienen una resolución de 500 milisegundos.

## <a name="examples"></a>Ejemplos

Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM a y desde el formato de **\_ fecha** de **FILETIME** o VT, vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md). Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).

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

[**SWbemDateTime.GetFileTime**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




