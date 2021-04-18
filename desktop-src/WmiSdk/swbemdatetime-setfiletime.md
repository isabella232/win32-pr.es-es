---
description: Convierte una fecha en el formato de cadena FILETIME en el formato de fecha y hora de CIM.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Método SWbemDateTime. SetFileTime (Wbemdisp. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155840"
---
# <a name="swbemdatetimesetfiletime-method"></a>SWbemDateTime. SetFileTime, método

El método **SetFileTime** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte una fecha en el formato de cadena **FILETIME** al formato de [fecha y hora de CIM](date-and-time-format.md) .

El formato **FILETIME** es una estructura datetime de 64 bits que representa el número de unidades de 100-nanosegundos desde el comienzo del 1 de enero de 1601. Instrumental de administración de Windows (WMI) trata los valores de **FILETIME** como representaciones de cadena de números de bits 64 sin signo.

Para ver la explicación de la sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strFileTime* \[ de\]
</dt> <dd>

Valor de **FILETIME** que se usa para establecer el objeto.

</dd> <dt>

*bIsLocal* \[ en, opcional\]
</dt> <dd>

Si es **true**, *strFileTime* se interpreta como una hora local. La propiedad hora universal coordinada (UTC) contiene la hora local convertida en el desplazamiento UTC correcto. Cuando *bIsLocal* es **false**, *strFileTime* se convierte directamente en un valor UTC con un desplazamiento de 0 (cero).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **SetFileTime** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error de la lista siguiente.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

El formato de *strFileTime* no es válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Después de una llamada correcta a **SetFileTime**, el valor [**DateTime**](datetime.md) siempre se interpreta como un valor absoluto (**DateTime**) y [**IsInterval**](swbemdatetime-isinterval.md) se establece en **false**.

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

[**SWbemDateTime.SetVarDate**](swbemdatetime-setvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

