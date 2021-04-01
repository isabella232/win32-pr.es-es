---
description: Función de devolución de llamada que se usa para notificar al host la información de la pila de llamadas.
MS-HAID: vspixengine.ICallStackCallback\_ResultCallback\_DWORD\_CallStackFrame\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ICallStackCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9C083298-6FD5-4414-8E0C-625F6A144668
api_name:
- ICallStackCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4bd77ea22fd31b31081d72707b1fd7a2efbda607
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906657"
---
# <a name="span-idvspixengineicallstackcallback_resultcallback_dword_callstackframe_arrspanicallstackcallbackresultcallback-method"></a><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback:: ResultCallback (método)

Función de devolución de llamada que se usa para notificar al host la información de la pila de llamadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResultCallback(
   DWORD             count,
   CallStackFrame [] count0_callStackFrameBuffer
);
```

## <a name="parameters"></a>Parámetros

*contabiliza*   
Número de framebuffers de pila de llamadas devueltos.

*count0 \_ callStackFrameBuffer*   
Información de la pila de llamadas.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**ICallStackCallback**](/windows/desktop/direct3dtools/icallstackcallback)

 

 
