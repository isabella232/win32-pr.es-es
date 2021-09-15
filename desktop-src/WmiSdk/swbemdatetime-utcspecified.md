---
description: Valor booleano que indica si el componente hora universal coordinada (UTC) del valor datetime de CIM contiene un intervalo o un valor comodín.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime.UTCSpecified (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2ada5bbbfa68e6cb63c0e060d6c3a12c0f771a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359422"
---
# <a name="swbemdatetimeutcspecified-property"></a>Propiedad SWbemDateTime.UTCSpecified

La **propiedad UTCSpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente Hora coordinada universal (UTC) del valor datetime de CIM contiene un intervalo o un valor comodín. Si **UTCSpecified es** **TRUE e** [**IsInterval**](swbemdatetime-isinterval.md) **es FALSE,** [**SWbemDateTime.UTC**](swbemdatetime-utc.md) contiene un [**valor DATETIME.**](datetime.md) Un **valor DATETIME** que contiene un intervalo no se puede convertir al formato **VT \_ DATE** ni **al formato FILETIME.** Si **UTCSpecified** es **FALSE e** **IsInterval** es **TRUE,** **SWbemDateTime.UTC** contiene un intervalo.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores [**DATETIME**](datetime.md) de CIM a y desde el formato **FILETIME** o el formato **VT \_ DATE,** vea [Tareas wmi:](wmi-tasks--dates-and-times.md)fechas y horas. Para obtener una descripción del formato de fecha y hora CIM, vea [Formato de fecha y hora.](date-and-time-format.md)

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

[**SWbemDateTime.UTC**](swbemdatetime-utc.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




