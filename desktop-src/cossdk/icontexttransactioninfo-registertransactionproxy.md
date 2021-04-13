---
description: Asocia una implementación de ITransactionProxy con el contexto actual.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'IContextTransactionInfo:: RegisterTransactionProxy (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360077"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a>IContextTransactionInfo:: RegisterTransactionProxy (método)

Asocia una implementación de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) con el contexto actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProxy* \[ de\]
</dt> <dd>

Implementación de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) que se va a asociar al contexto actual.

</dd> <dt>

*pGuid* \[ enuncia\]
</dt> <dd>

GUID que identifica el proxy de transacción. COM+ usa este GUID al llamar a [**ITransactionProxy:: commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) en el proxy de transacción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY e e \_ inesperados, así como los valores siguientes.



| Código devuelto                                                                                                     | Descripción                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                            | El método se completó correctamente.<br/>                                                                           |
| <dl> <dt>**CONTEXTO \_ E \_ ALREADYINTRANSACTION**</dt> </dl> | El contexto actual ya tiene una implementación de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) asociada.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                       | El contexto actual hospeda una transacción de traiga su propia transacción o una transacción que no es raíz.<br/>    |



 

## <a name="remarks"></a>Observaciones

Solo se puede llamar al método **RegisterTransactionProxy** si el contexto actual es un contexto de transacción raíz. No se puede llamar si el contexto hospeda una transacción de transacciones o no raíz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




