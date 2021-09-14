---
description: Obtiene o establece un valor que representa el componente minutes del valor datetime.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime.Minutes (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cce55d731916d0e8180de1bde495566d4ed22c49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965267"
---
# <a name="swbemdatetimeminutes-property"></a>Propiedad SWbemDateTime.Minutes

La **propiedad Minutes** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente minutes del valor datetime.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Después de obtener o establecer la **propiedad Minutes,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.

<dl> <dt>

**wbemErrValueOutOfRange:** 2147749931 (0x8004102B)
</dt> <dd>

El valor no estaba en el intervalo de 0 a 59.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si la propiedad **SWbemDateTime.Minutes** se establece en 1, la propiedad [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) contiene un valor que se desplaza por un segundo, un error de redondeo que se produce cuando un valor **datetime** cim se convierte en un valor **VT \_ DATE.** Si la **propiedad Minutes** se establece en 0 en su lugar, la **propiedad Seconds** devuelve el valor correcto.

## <a name="examples"></a>Ejemplos

Para obtener ejemplos de cómo usar el objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores [**DATETIME**](datetime.md) de CIM a y desde el formato **FILETIME** o el formato **VT \_ DATE,** vea [Wmi Tasks: Dates and Times](wmi-tasks--dates-and-times.md). Para obtener una descripción del formato **DATETIME de** CIM, vea [Formato de fecha y hora](date-and-time-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemDateTime.MinutesSpecified**](swbemdatetime-minutesspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

