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
ms.openlocfilehash: 41888a859b6b665390290ba66bed69418cbddd9b708355dc78cc2670ba4d240f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896085"
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
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

