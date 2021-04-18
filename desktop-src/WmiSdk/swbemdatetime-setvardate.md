---
description: Convierte una fecha del formato de fecha de VT \_ al formato de fecha y hora de CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Método SWbemDateTime. SetVarDate (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361376"
---
# <a name="swbemdatetimesetvardate-method"></a>SWbemDateTime. SetVarDate, método

El método **SetVarDate** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte una fecha en el formato de fecha de VT al formato de **\_ fecha** [y hora de CIM](date-and-time-format.md) .

Un valor de **\_ fecha de VT** es un valor de fecha y hora Variant que Visual Basic y el uso de ActiveX.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vdate* \[ de\]
</dt> <dd>

Valor de fecha Variant para establecer el objeto. Este parámetro debe estar en el formato de **\_ fecha VT** .

</dd> <dt>

*bIsLocal* \[ en, opcional\]
</dt> <dd>

Si es **true**, *vdate* se interpreta como una hora local y la propiedad hora universal coordinada (UTC) contiene la hora local que se convierte en el desplazamiento UTC correcto. Cuando *bIsLocal* es **false**, *vdate* se convierte directamente en un valor UTC con un desplazamiento de cero (0).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **SetVarDate** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error de la lista siguiente.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

El formato de *vdate* no es válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Después de una llamada correcta a **SetVarDate**, el valor de [**fecha y hora**](datetime.md) se interpreta como un valor de fecha y hora absoluto en lugar de un intervalo, y la propiedad [**IsInterval**](swbemdatetime-isinterval.md) se establece en **false**.

Las funciones intrínsecas Visual Basic o VBScript [CDate](/previous-versions//2dt118h2(v=vs.85)) proporcionan un valor [**DateTime**](datetime.md) en el formato de **\_ fecha de VT** para la entrada en **SetVarDate**.

## <a name="examples"></a>Ejemplos

Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md). Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).

El código de ejemplo de [conversión de fecha a WMI Date-Time formato](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) de VBScript de la galería de TechNet usa SetVarDate para convertir un valor de fecha y hora normal en el formato de fecha y hora UTC.

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

[**SWbemDateTime.SetFileTime**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

