---
description: Obtiene o establece un valor que representa el componente de día del valor datetime.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime.Day (Wbemdisp.h)
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
ms.openlocfilehash: d2483e52d9b40978a28f96bb5352df4f9abf4f89becf52550b82fd931580d7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640505"
---
# <a name="swbemdatetimeday-property"></a>SWbemDateTime.Day, propiedad

La **propiedad Day** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente day del valor datetime. El valor debe estar en el intervalo de 1 a 31 si [**IsInterval**](swbemdatetime-isinterval.md) es **FALSE.** Sin embargo, la comprobación de errores no es sensible al valor de mes. Por lo tanto, el valor dentro del intervalo de 31 no devolverá un error en los casos en los que el valor [**SWbemDateTime.Month**](swbemdatetime-month.md) es para un mes de menos de 31 días (febrero, abril, junio, septiembre, noviembre).

El valor predeterminado de **Day** es 01.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Después de obtener o establecer la **propiedad Day,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.

<dl> <dt>

**wbemErrValueOutOfRange:** 2147749931 (0x8004102B)
</dt> <dd>

Si [**IsInterval es**](swbemdatetime-isinterval.md) **TRUE y** el intervalo de valores correctos supera de 0 a 99999999.

</dd> </dl>

## <a name="examples"></a>Ejemplos

Para obtener ejemplos de cómo usar el objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores [**DATETIME**](datetime.md) de CIM a y desde el formato **FILETIME** o el formato **VT \_ DATE,** vea [Wmi Tasks: Dates and Times](wmi-tasks--dates-and-times.md). Para obtener una descripción del formato **DATETIME de** CIM, vea [Formato de fecha y hora](date-and-time-format.md).

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

[**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

