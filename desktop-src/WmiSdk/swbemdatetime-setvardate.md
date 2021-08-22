---
description: Convierte una fecha en el formato \_ VT DATE al formato datetime de CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Método SWbemDateTime.SetVarDate (Wbemdisp.h)
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
ms.openlocfilehash: 56d193bd2faffd51507ec4a913c7ee068b055dcf45ca756e801431659768c47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050103"
---
# <a name="swbemdatetimesetvardate-method"></a>Método SWbemDateTime.SetVarDate

El **método SetVarDate** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte una fecha en el formato **VT \_ DATE** al [formato datetime cim.](date-and-time-format.md)

Un **valor \_ VT DATE** es un valor datetime de variante que Visual Basic y ActiveX usar.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vdate* \[ En\]
</dt> <dd>

Valor de fecha de variante para establecer el objeto. Este parámetro debe tener el formato **\_ VT DATE.**

</dd> <dt>

*bIsLocal* \[ en, opcional\]
</dt> <dd>

Si **es TRUE,** *vdate* se interpreta como una hora local y la propiedad Hora universal coordinada (UTC) contiene la hora local que se convierte al desplazamiento UTC correcto. Cuando *bIsLocal* es **FALSE,** *vdate* se convierte directamente en un valor UTC con un desplazamiento de cero (0).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método SetVarDate,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error en la lista siguiente.

<dl> <dt>

**wbemErrInvalidSyntax:** 2147749921 (0x80041021)
</dt> <dd>

El formato *de vdate* no es válido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Después de una llamada correcta a **SetVarDate**, el valor DATETIME se interpreta como un valor [**datetime**](datetime.md) absoluto en lugar de un intervalo, y la propiedad [**IsInterval**](swbemdatetime-isinterval.md) se establece en **FALSE.**

La función Visual Basic o VBScript [CDate](/previous-versions//2dt118h2(v=vs.85)) proporciona un valor [**datetime**](datetime.md) en el formato **VT \_ DATE** para la entrada **a SetVarDate**.

## <a name="examples"></a>Ejemplos

Para obtener ejemplos de cómo usar el objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores [**DATETIME**](datetime.md) de CIM a y desde el formato **FILETIME** o el formato **VT \_ DATE,** vea [Wmi Tasks: Dates and Times](wmi-tasks--dates-and-times.md). Para obtener una descripción del formato **DATETIME de** CIM, vea [Formato de fecha y hora](date-and-time-format.md).

El ejemplo de código DE VBScript Convert [Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) de la Galería de TechNet usa SetVarDate para convertir un valor de fecha y hora normal al formato de fecha y hora UTC.

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

[**SWbemDateTime.SetFileTime**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

