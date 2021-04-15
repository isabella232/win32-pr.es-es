---
description: GUID de la partición del objeto de la clase de evento.
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: 'IEventSubscription3:: EventClassPartitionID (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassPartitionID
- IEventSubscription3.get_EventClassPartitionID
- IEventSubscription3.put_EventClassPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: d41d3e2a170deffb73f1f533226421d88f150c01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539304"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a>IEventSubscription3:: EventClassPartitionID (propiedad)

GUID de la partición del objeto de la clase de evento.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_EventClassPartitionID(
  [in]          BSTR bstrEventClassPartitionID
);

HRESULT get_EventClassPartitionID(
  [out, retval] BSTR *pbstrEventClassPartitionID
);
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene el GUID de la partición de la clase de eventos.

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

 

 




