---
description: Obtiene o establece la fecha CIM sin formato en el formato DMTF (Distributed Management Task Force).
ms.assetid: 426a60d5-c364-406e-8346-049a13d59c7f
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime.Value (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Value
- ISWbemDateTime.Value
- ISWbemDateTime.get_Value
- ISWbemDateTime.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2ecb3a42a865559ba9b3c3e5fbec7302f975fa0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359418"
---
# <a name="swbemdatetimevalue-property"></a>Propiedad SWbemDateTime.Value

La **propiedad Value** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece la fecha CIM sin formato en el formato DMTF (Distributed Management Task Force). El formato DMTF es una representación de cadena del [**valor DATETIME.**](datetime.md) Esta propiedad es la propiedad predeterminada para **los objetos SWbemDateTime.** La **propiedad Value** tiene un valor predeterminado de 00000101000000.000000+000.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.Value As String
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Después de obtener o establecer la **propiedad Value,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.

<dl> <dt>

**wbemErrInvalidSyntax:** 2147749921 (0x80041021)
</dt> <dd>

El formato *de strValue* no es válido.

</dd> </dl>

## <a name="examples"></a>Ejemplos

Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores [**DATETIME**](datetime.md) de CIM a y desde el formato **FILETIME** o el formato **VT \_ DATE,** vea [Tareas wmi:](wmi-tasks--dates-and-times.md)fechas y horas. Para obtener una descripción del formato **CIM DATETIME,** vea [Formato de fecha y hora](date-and-time-format.md).

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

