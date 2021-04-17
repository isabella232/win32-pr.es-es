---
description: El monitor debe implementar el método OnStop. MSCVC llama a este método para notificar al monitor que se va a detener la captura.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'IMonitor:: OnStop (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677274"
---
# <a name="imonitoronstop-method"></a>IMonitor:: OnStop (método)

El monitor debe implementar el método **OnStop** . MSCVC llama a este método para notificar al monitor que se va a detener la captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnStop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError).

Si el método no se realiza correctamente, el valor devuelto es un código de error. Cuando se devuelve un código de error, el monitor no se puede reiniciar.

## <a name="remarks"></a>Observaciones

MCSVC llama a este método después de llamar a [IRTC:: Stop](irtc-stop.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




