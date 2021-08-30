---
description: Solicitud asincrónica para obtener información especificada sobre un único marco especificado.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameEventsRequest::RequestAsync (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 821E7674-A960-46F6-A7AF-386298902ED6
api_name:
- IFrameEventsRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d2299a63b7613aaa6875211149cbce1f47308a8f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630816"
---
# <a name="span-idvspixengineiframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspaniframeeventsrequestrequestasync-method"></a><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest::RequestAsync (método)

Solicitud asincrónica para obtener información especificada sobre un único marco especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

*frameNumber*   
Marco especificado.

*numColumns*   
Las columnas especificadas (campos).

*columnas \_ count1*   
Dirección de devolución de llamada utilizada para notificar al host de resultados.

*requestCallback*   
Dirección de devolución de llamada utilizada para notificar al host de resultados.

*requestCookie*   
Cookie que identifica de forma única la solicitud y se puede usar para indicar que se cancele.

*progressIntervalMsecs*   
No se utiliza.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IFrameEventsRequest**](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
