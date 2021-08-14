---
description: Solicita una lista de los resultados del historial de píxeles en el píxel especificado, represente tartget /UAV y frame.
MS-HAID: vspixengine.IPixelHistoryRequest\_RequestAsync\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryRequest::RequestAsync (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 00A90033-FC57-4BEE-B950-82E678437F2A
api_name:
- IPixelHistoryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6aaeda3ae71880c3789d7fc0833b82403b8c6798fca5fef2ab475b57a29b0f71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283079"
---
# <a name="span-idvspixengineipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dwordspanipixelhistoryrequestrequestasync-method"></a><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest::RequestAsync (método)

Solicita una lista de los resultados del historial de píxeles en el píxel especificado, represente tartget /UAV y frame.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestAsync(
   DWORD                   frameNumber,
   Point2D                 pixel,
   DWORD                   renderTargetPtr,
   IPixelHistoryCallback * requestCallback,
   DWORD                   requestCookie,
   DWORD                   progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

*frameNumber*   
Marco especificado.

*Pixel*   
Píxel especificado.

*renderTargetPtr*   
Destino de representación especificado.

*requestCallback*   
Dirección de una devolución de llamada utilizada para indicar el host de resultados.

*requestCookie*   
Cookie que identifica de forma única la solicitud y se puede usar para indicar que se cancele.

*progressIntervalMsecs*   
No se usa.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPixelHistoryRequest**](/windows/desktop/direct3dtools/ipixelhistoryrequest)

 

 
