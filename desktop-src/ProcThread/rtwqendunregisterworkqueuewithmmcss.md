---
description: Completa una solicitud asincrónica para anular el registro de una cola de trabajo con una tarea del Servicio programador de clases multimedia (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: Función RtwqEndUnregisterWorkQueueWithMMCSS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: 083f0ca787bb842850320b9dd1d320ef4d5b172ee0b6d9b117296e58b991bd0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793405"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a>Función RtwqEndUnregisterWorkQueueWithMMCSS

Completa una solicitud asincrónica para anular el registro de una cola de trabajo con una tarea del Servicio programador de clases multimedia (MMCSS).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pResult* 
</dt> <dd>

Puntero a [**la interfaz IMFAsyncResult.**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) Pase el mismo puntero que el objeto de devolución de llamada recibido en el [**método IRtwqAsyncCallback::Invoke.**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>None</dt> </dl>        |
| Biblioteca<br/>                  | <dl> <dt>Rtworkq.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
