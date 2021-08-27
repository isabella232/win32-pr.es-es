---
description: Recupera el número de versión del sistema de eventos.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: IEventSystem2::GetVersion (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 77452ccebac71cb8de8357fee0199bc04b690d59cf8d113d57a5850db0771315
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070625"
---
# <a name="ieventsystem2getversion-method"></a>IEventSystem2::GetVersion (método)

Recupera el número de versión del sistema de eventos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pnVersion* \[ out\]
</dt> <dd>

Número de versión del sistema de eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL y S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




