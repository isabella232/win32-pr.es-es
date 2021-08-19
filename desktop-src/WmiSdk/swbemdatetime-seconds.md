---
description: Obtiene o establece un valor que representa el componente de segundos del valor datetime.
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime.Seconds (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4d30095e5464736b3db984b71f94a216c29f4327227a5e5b99becfbcae5e1a58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816202"
---
# <a name="swbemdatetimeseconds-property"></a>Propiedad SWbemDateTime.Seconds

La **propiedad Seconds** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente seconds del valor datetime.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Después de obtener o establecer la **propiedad Seconds,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.

<dl> <dt>

**wbemErrValueOutOfRange:** 2147749931 (0x8004102B)
</dt> <dd>

El valor no estaba en el intervalo de 0 a 59.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **propiedad SWbemDateTime.Seconds** puede contener un valor incorrecto si la propiedad [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) se ha establecido en 1. Contiene un valor que se desplaza un segundo debido a un error de redondeo que se produce cuando un valor [**DATETIME**](datetime.md) de CIM se convierte en un **valor VT \_ DATE.** Si la **propiedad Minutes** se establece en 0 (cero), la **propiedad Seconds** devuelve el valor correcto.

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

[**SWbemDateTime.SecondsSpecified**](swbemdatetime-secondsspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

