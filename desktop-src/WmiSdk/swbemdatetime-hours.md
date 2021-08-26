---
description: Obtiene o establece un valor que representa el componente hours del valor datetime.
ms.assetid: 83f084fa-57a5-4467-acea-7e19de82a91f
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime.Hours (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Hours
- ISWbemDateTime.Hours
- ISWbemDateTime.get_Hours
- ISWbemDateTime.put_Hours
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4ebe2cf5d25efd474268cea1459718f4741e4c4c698cbdbe65cc765cc17c2ae7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030385"
---
# <a name="swbemdatetimehours-property"></a>Propiedad SWbemDateTime.Hours

La **propiedad Hours** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente hours del valor datetime.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Hours As Long
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Después de obtener o establecer la **propiedad Hours,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.

<dl> <dt>

**wbemErrValueOutOfRange:** 2147749931 (0x8004102B)
</dt> <dd>

El valor no estaba en el intervalo de 0 a 23.

</dd> </dl>

## <a name="examples"></a>Ejemplos

Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores [**DATETIME**](datetime.md) de CIM a y desde el formato **FILETIME** o el formato **VT \_ DATE,** vea [Tareas wmi:](wmi-tasks--dates-and-times.md)fechas y horas. Para obtener una descripción del formato **CIM DATETIME,** vea [Formato de fecha y hora](date-and-time-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**SWbemDateTime.HoursSpecified**](swbemdatetime-hoursspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

