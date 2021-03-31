---
description: Completa una solicitud asincrónica para anular el registro de una cola de trabajo con una tarea del servicio de programador de clases multimedia (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: RtwqEndUnregisterWorkQueueWithMMCSS función)
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
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910354"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a>RtwqEndUnregisterWorkQueueWithMMCSS función)

Completa una solicitud asincrónica para anular el registro de una cola de trabajo con una tarea del servicio de programador de clases multimedia (MMCSS).

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

Puntero a la interfaz [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) . Pase el mismo puntero que el objeto de devolución de llamada recibido en el método [**IRtwqAsyncCallback:: Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>None</dt> </dl>        |
| Biblioteca<br/>                  | <dl> <dt>Rtworkq. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
