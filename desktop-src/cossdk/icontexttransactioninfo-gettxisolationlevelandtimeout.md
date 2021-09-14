---
description: Recupera el nivel de aislamiento y el valor de tiempo de espera de una transacción hospedada en el contexto de transacción raíz.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: IContextTransactionInfo::GetTxIsolationLevelAndTimeout (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063896"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a>IContextTransactionInfo::GetTxIsolationLevelAndTimeout (método)

Recupera el nivel de aislamiento y el valor de tiempo de espera de una transacción hospedada en el contexto de transacción raíz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIsoLevel* \[ out\]
</dt> <dd>

Valor [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) de la transacción.

</dd> <dt>

*dwTime* \[ out\]
</dt> <dd>

Tiempo de espera de la transacción, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED y S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

