---
description: Devolución de llamada que notifica al host una solicitud cancelada.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCallback\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: INewFramesCallback::CancelUsingCallback (Método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 291B2F85-1437-4704-8971-4B7C25B693F8
api_name:
- INewFramesCallback.CancelUsingCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6a78f769e443e6870e93de56bbc8fb8b5a669c6108bb78e950e1c12fc160cddc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119369235"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcallback_iunknown_ptrspaninewframescallbackcancelusingcallback-method"></a><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>INewFramesCallback::CancelUsingCallback (Método)

Devolución de llamada que notifica al host una solicitud cancelada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a>Parámetros

*requestCallback*   
Dirección de la solicitud cancelada.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**INewFramesCallback**](/windows/desktop/direct3dtools/inewframescallback)

 

 
