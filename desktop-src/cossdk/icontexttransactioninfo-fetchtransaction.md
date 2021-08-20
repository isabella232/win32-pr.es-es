---
description: Recupera la transacción o el proxy de transacción asociado al contexto actual, si existe.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: IContextTransactionInfo::FetchTransaction (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d673483118feb02ec2f1172640b9972d883505f48bc1fd8d8803844b963b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991065"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>IContextTransactionInfo::FetchTransaction (método)

Recupera la transacción o el proxy de transacción asociado al contexto actual, si existe.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pUnk* \[ out, retval\]
</dt> <dd>

El proxy de transacción o transacción asociado al contexto actual; de lo contrario, **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED y S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




