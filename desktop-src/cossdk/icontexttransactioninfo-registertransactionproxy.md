---
description: Asocia una implementación de ITransactionProxy al contexto actual.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: IContextTransactionInfo::RegisterTransactionProxy (método)
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
ms.openlocfilehash: 7bdae305fc7dc7ec15c2d140064d7479e4454d1bdb04562f5dd4201a92072425
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954025"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a>IContextTransactionInfo::RegisterTransactionProxy (método)

Asocia una implementación [**de ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) al contexto actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProxy* \[ En\]
</dt> <dd>

Implementación [**de ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) que se asociará al contexto actual.

</dd> <dt>

*pGuid* \[ out\]
</dt> <dd>

GUID que identifica el proxy de transacción. COM+ usa este GUID al llamar a [**ITransactionProxy::Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) en el proxy de transacción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, E \_ OUTOFMEMORY y E UNEXPECTED, así como \_ los valores siguientes.



| Código devuelto                                                                                                     | Descripción                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                            | El método se completó correctamente.<br/>                                                                           |
| <dl> <dt>**CONTEXT \_ E \_ ALREADYINTRANSACTION**</dt> </dl> | El contexto actual ya tiene una implementación [**de ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) asociada.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                       | El contexto actual hospeda una transacción Bring Your Own Transaction (BYOT) o una transacción no raíz.<br/>    |



 

## <a name="remarks"></a>Comentarios

Solo se puede llamar al **método RegisterTransactionProxy** si el contexto actual es un contexto de transacción raíz. No se puede llamar a si el contexto hospeda una transacción BYOT o una transacción no raíz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




