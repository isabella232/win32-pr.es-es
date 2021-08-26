---
description: Solicitud asincrónica para obtener los fotogramas de lista capturados en el registro de gráficos.
MS-HAID: vspixengine.IFrameListRequest\_RequestAsync\_IFrameListCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameListRequest::RequestAsync (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 309C28F2-CE01-49E7-9A21-5053E3ED7721
api_name:
- IFrameListRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b1161f36a2bb0d1cdc9e1f65fa2ce3fea4984f00
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621981"
---
# <a name="span-idvspixengineiframelistrequest_requestasync_iframelistcallback_ptr_dword_dwordspaniframelistrequestrequestasync-method"></a><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest::RequestAsync (método)

Solicitud asincrónica para obtener los fotogramas de lista capturados en el registro de gráficos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestAsync(
   IFrameListCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

*requestCallback*   
Dirección de devolución de llamada usada para notificar al host de resultados.

*requestCookie*   
Cookie que identifica de forma única la solicitud y se puede usar para indicar que se cancele.

*progressIntervalMsecs*   
No se utiliza.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IFrameListRequest**](/windows/desktop/direct3dtools/iframelistrequest)

 

 
