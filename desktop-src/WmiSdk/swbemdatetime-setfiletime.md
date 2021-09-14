---
description: Convierte una fecha en el formato FILETIME de cadena al formato datetime cim.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Método SWbemDateTime.SetFileTime (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073055"
---
# <a name="swbemdatetimesetfiletime-method"></a>Método SWbemDateTime.SetFileTime

El **método SetFileTime** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte una fecha en el formato **FILETIME** de cadena al [formato datetime cim.](date-and-time-format.md)

El **formato FILETIME** es una estructura datetime de 64 bits que representa el número de unidades de 100 nanosegundos desde el 1 de enero de 1601. Windows Instrumental de administración (WMI) trata los valores **FILETIME** como representaciones de cadena de números de 64 bits sin signo.

Para obtener la explicación de la sintaxis, [vea Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strFileTime* \[ En\]
</dt> <dd>

**Valor FILETIME** usado para establecer el objeto.

</dd> <dt>

*bIsLocal* \[ in, opcional\]
</dt> <dd>

Si **es TRUE,** *strFileTime* se interpreta como una hora local. La propiedad Hora universal coordinada (UTC) contiene la hora local convertida al desplazamiento UTC correcto. Cuando *bIsLocal* es **FALSE,** *strFileTime* se convierte directamente en un valor UTC con un desplazamiento de 0 (cero).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método SetFileTime,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error en la lista siguiente.

<dl> <dt>

**wbemErrInvalidSyntax:** 2147749921 (0x80041021)
</dt> <dd>

El formato *de strFileTime* no es válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Después de una llamada correcta a **SetFileTime**, el valor [**datetime**](datetime.md) siempre se interpreta como un valor absoluto **(datetime**) e [**IsInterval**](swbemdatetime-isinterval.md) se establece en **FALSE.**

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemDateTime.SetVarDate**](swbemdatetime-setvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

