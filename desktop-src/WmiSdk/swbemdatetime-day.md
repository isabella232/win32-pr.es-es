---
description: Obtiene o establece un valor que representa el componente de día del valor de fecha y hora.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. Day (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1de77a8e5d616284c3dc13a19bce2526db371c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002825"
---
# <a name="swbemdatetimeday-property"></a>SWbemDateTime. Day (propiedad)

La propiedad **Day** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente de día del valor DateTime. El valor debe estar en el intervalo comprendido entre 1 y 31 si [**IsInterval**](swbemdatetime-isinterval.md) es **false**. Sin embargo, la comprobación de errores no es sensible al valor del mes. Por lo tanto, el valor en el intervalo de 31 no devolverá un error en los casos en los que el valor de [**SWbemDateTime. month**](swbemdatetime-month.md) sea para un mes de menos de 31 días (febrero, abril, junio, septiembre, noviembre).

El valor predeterminado para **Day** es 01.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Después de obtener o establecer la propiedad **Day** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

Si [**IsInterval**](swbemdatetime-isinterval.md) es **true** y el intervalo de valores correctos supera de 0 a 99999999.

</dd> </dl>

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

[**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

