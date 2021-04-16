---
description: Recupera el nivel de aislamiento y el valor de tiempo de espera de una transacción hospedada en el contexto de la transacción raíz.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'IContextTransactionInfo:: GetTxIsolationLevelAndTimeout (método)'
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696134"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a>IContextTransactionInfo:: GetTxIsolationLevelAndTimeout (método)

Recupera el nivel de aislamiento y el valor de tiempo de espera de una transacción hospedada en el contexto de la transacción raíz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIsoLevel* \[ enuncia\]
</dt> <dd>

Valor [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) de la transacción.

</dd> <dt>

*dwTime* \[ enuncia\]
</dt> <dd>

Tiempo de espera de la transacción, en segundos.

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

 

