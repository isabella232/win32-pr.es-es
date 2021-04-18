---
description: Obtiene o establece un valor que representa el componente de minutos del valor de fecha y hora.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. minutes (Wbemdisp. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707350"
---
# <a name="swbemdatetimeminutes-property"></a>Propiedad SWbemDateTime. minutes

La propiedad **minutes** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente de minutos del valor DateTime.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Después de obtener o establecer la propiedad **minutes** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

El valor no estaba en el intervalo comprendido entre 0 y 59.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si la propiedad **SWbemDateTime. minutes** está establecida en 1, la propiedad [**SWbemDateTime. seconds**](swbemdatetime-seconds.md) contiene un valor que se desplaza por un segundo un error de redondeo que se produce cuando un valor **DateTime** de CIM se convierte en un valor de **\_ fecha de VT** . Si en su lugar la propiedad **minutes** está establecida en 0, la propiedad **seconds** devuelve el valor correcto.

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

[**SWbemDateTime.MinutesSpecified**](swbemdatetime-minutesspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

