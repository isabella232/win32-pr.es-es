---
description: El monitor debe implementar el método OnStop. MSCVC llama a este método para notificar al monitor que se detendrán las capturas.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: Método IMonitor::OnStop (Netmon.h)
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
ms.openlocfilehash: cb81042395de2a2381921cfd0b30c18af22df320b8ce8db228cf65743b1fe334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778995"
---
# <a name="imonitoronstop-method"></a>IMonitor::OnStop (método)

El monitor debe implementar el método **OnStop.** MSCVC llama a este método para notificar al monitor que se detendrán las capturas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnStop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es S \_ OK (que es igual que NOERROR).

Si el método no es correcto, el valor devuelto es un código de error. Cuando se devuelve un código de error, no se puede reiniciar el monitor.

## <a name="remarks"></a>Comentarios

McSVC llama a este método después de [llamar a IRTC::Stop.](irtc-stop.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




