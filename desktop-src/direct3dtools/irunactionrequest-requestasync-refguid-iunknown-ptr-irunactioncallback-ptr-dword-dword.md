---
description: Una solicitud asincrónica para iniciar una acción (por ejemplo, capturar un fotograma) en el motor.
MS-HAID: vspixengine.IRunActionRequest\_RequestAsync\_REFGUID\_IUnknown\_ptr\_IRunActionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IRunActionRequest::RequestAsync (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4A4DF4BE-383D-4B36-9195-61720C3B4D97
api_name:
- IRunActionRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d63816133dfcf8270de41481e1c99e3d691d51c3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627330"
---
# <a name="span-idvspixengineirunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dwordspanirunactionrequestrequestasync-method"></a><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest::RequestAsync (método)

Una solicitud asincrónica para iniciar una acción (por ejemplo, capturar un fotograma) en el motor.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestAsync(
   REFGUID              action,
   IUnknown *           actionPayload,
   IRunActionCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

*Acción*   
Acción especificada.

*actionPayload*   
Carga útil de la acción especificada.

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

[**IRunActionRequest**](/windows/desktop/direct3dtools/irunactionrequest)

 

 
