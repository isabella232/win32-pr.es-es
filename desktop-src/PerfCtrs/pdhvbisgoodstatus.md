---
description: La función PdhVbIsStatusStatus prueba un valor de estado para determinar si se trata de un código correcto o de error. Si el valor de estado es correcto, el valor devuelto será distinto de cero. Si se trata de un código de estado de error, el valor devuelto será cero.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: Función PdhVbIsStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: e0b142da988143d7304a6b9b01bc5163e741fdaff77d7e0d796882607fc73044
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683775"
---
# <a name="pdhvbisgoodstatus-function"></a>Función PdhVbIsStatus

La **función PdhVbIsStatusStatus prueba** un valor de estado para determinar si se trata de un código correcto o de error. Si el valor de estado es correcto, el valor devuelto será distinto de cero. Si se trata de un código de estado de error, el valor devuelto será cero.

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbIsStatusStatus( \_ ByVal StatusValue As Long \_ ) As Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*StatusValue* 
</dt> <dd>

Valor de estado devuelto por otra función PDH que se va a probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve cero si el código de estado es un código de estado de error. Devuelve distinto de cero si el código de estado es un código de estado correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




