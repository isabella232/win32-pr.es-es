---
description: Los criterios de filtro que rigen la suscripción.
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: IEventSubscription2::FilterCriteria, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1443a89433cff91a298e8c390fce8f1f64b99f1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072987"
---
# <a name="ieventsubscription2filtercriteria-property"></a>IEventSubscription2::FilterCriteria, propiedad

Los criterios de filtro que rigen la suscripción.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a>Valor de propiedad

Criterios de filtro o CLSID para una clase que implementa [**IPublisherFilter.**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter)

## <a name="error-codes"></a>Códigos de error

Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL y S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




