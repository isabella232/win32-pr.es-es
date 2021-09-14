---
description: GUID de aplicación del suscriptor.
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: Propiedad IEventSubscription3::SubscriberApplicationID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: c2e726d97821a7a7143f4971a4918227235adb9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888953"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a>Propiedad IEventSubscription3::SubscriberApplicationID

GUID de aplicación del suscriptor.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene el GUID de la aplicación de suscriptor.

## <a name="error-codes"></a>Códigos de error

Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL y S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEventSubscription3**](ieventsubscription3.md)
</dt> </dl>

 

 




