---
description: La función PdhVbIsGoodStatus comprueba un valor de estado para determinar si es un código de error o correcto. Si el valor de estado es correcto, el valor devuelto será distinto de cero. Si se trata de un código de estado de error, el valor devuelto será cero.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: PdhVbIsGoodStatus función)
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
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667307"
---
# <a name="pdhvbisgoodstatus-function"></a>PdhVbIsGoodStatus función)

La función **PdhVbIsGoodStatus** comprueba un valor de estado para determinar si es un código de error o correcto. Si el valor de estado es correcto, el valor devuelto será distinto de cero. Si se trata de un código de estado de error, el valor devuelto será cero.

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbIsGoodStatus ( \_ ByVal StatusValue as Long \_ ) as Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*StatusValue* 
</dt> <dd>

Valor de estado devuelto por otra función de PDH que se va a probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve cero si el código de estado es un código de estado de error. Devuelve un valor distinto de cero si el código de estado es un código de estado correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




