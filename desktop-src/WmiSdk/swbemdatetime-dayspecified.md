---
description: Valor booleano que indica si el componente de día del valor DATETIME de CIM contiene un intervalo o un valor comodín.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime.DaySpecified (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: effa3bcb68351aa754006c143e738443efdb7238129f30847876ad17527ca279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992255"
---
# <a name="swbemdatetimedayspecified-property"></a>SWbemDateTime.DaySpecified, propiedad

La **propiedad DaySpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente day del valor [**DATETIME**](datetime.md) de CIM contiene un intervalo o un valor comodín. Si **DaySpecified** es **TRUE e** [**IsInterval**](swbemdatetime-isinterval.md) es **FALSE,** [**SWbemDateTime.Day**](swbemdatetime-day.md) contiene un valor datetime. Un [**valor DATETIME**](datetime.md) que contiene un intervalo no se puede convertir al formato **VT \_ DATE** o **FILETIME.** Si **DaySpecified** es **FALSE** e **IsInterval** **es TRUE,** **SWbemDateTime.Day** contiene un intervalo.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.DaySpecified As BOOLEAN
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

[**SWbemDateTime.Day**](swbemdatetime-day.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

 




