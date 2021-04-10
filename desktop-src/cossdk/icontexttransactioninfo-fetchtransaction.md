---
description: Recupera el proxy de transacción o de transacción asociado al contexto actual, si existe.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'IContextTransactionInfo:: FetchTransaction (método)'
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
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153203"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>IContextTransactionInfo:: FetchTransaction (método)

Recupera el proxy de transacción o de transacción asociado al contexto actual, si existe.

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

El proxy de transacción o transacción asociado al contexto actual; de lo contrario, **es null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperados y S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




