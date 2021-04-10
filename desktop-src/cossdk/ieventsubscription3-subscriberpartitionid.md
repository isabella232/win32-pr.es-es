---
description: GUID de partición del suscriptor.
ms.assetid: 0b2411d3-cdc1-492c-a54f-ca3d3bd8b953
title: 'IEventSubscription3:: SubscriberPartitionID (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberPartitionID
- IEventSubscription3.get_SubscriberPartitionID
- IEventSubscription3.put_SubscriberPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: b09c41ac1b3a90c3275daf7afa0cd90fe2bb905c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275090"
---
# <a name="ieventsubscription3subscriberpartitionid-property"></a>IEventSubscription3:: SubscriberPartitionID (propiedad)

GUID de partición del suscriptor.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_SubscriberPartitionID(
  [in]          BSTR bstrSubscriberPartitionID
);

HRESULT get_SubscriberPartitionID(
  [out, retval] BSTR *pbstrSubscriberPartitionID
);
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene el GUID de la partición del suscriptor.

## <a name="error-codes"></a>Códigos de error

Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ FAIL y S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEventSubscription3**](ieventsubscription3.md)
</dt> </dl>

 

 




