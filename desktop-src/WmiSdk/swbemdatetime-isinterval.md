---
description: Valor booleano que indica si cualquier campo de un valor DateTime de CIM debe interpretarse como un intervalo.
ms.assetid: ba5fcf17-7c26-4960-9da9-e380d90e5f3e
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. IsInterval (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.IsInterval
- ISWbemDateTime.IsInterval
- ISWbemDateTime.get_IsInterval
- ISWbemDateTime.put_IsInterval
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 468ea16de4f1206a9a15c58c2c7891df8afd4c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279292"
---
# <a name="swbemdatetimeisinterval-property"></a>Propiedad SWbemDateTime. IsInterval

La propiedad **IsInterval** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si cualquier campo de un valor DateTime de CIM debe interpretarse como un intervalo.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.IsInterval As boolean
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y hora de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md). Para obtener una descripción del formato de fecha y hora de CIM, consulte [formato de fecha y hora](date-and-time-format.md).

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

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Formato de fecha y hora](date-and-time-format.md)
</dt> </dl>

 

 




