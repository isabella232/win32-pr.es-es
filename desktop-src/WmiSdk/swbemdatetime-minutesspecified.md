---
description: Indica si el componente minutes del valor datetime de CIM contiene un intervalo o un valor comodín.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime.MinutesSpecified (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a780d9bed3224e1b9be006a2bdf94b2b411951ceb3ef4d82a439ba5ec451fd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992195"
---
# <a name="swbemdatetimeminutesspecified-property"></a>Propiedad SWbemDateTime.MinutesSpecified

La **propiedad MinutesSpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente minutes del valor datetime de CIM contiene un intervalo o un valor comodín. Si **MinutesSpecified** es **TRUE** e [**IsInterval**](swbemdatetime-isinterval.md) es **FALSE** (lo que indica que el valor datetime de CIM no tiene caracteres comodín), [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) contiene un valor de fecha. Un valor datetime que contiene un intervalo no se puede convertir al formato **\_ VT DATE** o **FILETIME.** Si [**HoursSpecified**](swbemdatetime-hoursspecified.md) es **FALSE e** **IsInterval** es **TRUE,** **SWbemDateTime.Minutes** contiene un intervalo.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a>Valor de propiedad

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemDateTime.Minutes**](swbemdatetime-minutes.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




