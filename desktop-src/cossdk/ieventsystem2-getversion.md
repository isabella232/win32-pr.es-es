---
description: Recupera el número de versión del sistema de eventos.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'IEventSystem2:: GetVersion (método)'
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
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496655"
---
# <a name="ieventsystem2getversion-method"></a>IEventSystem2:: GetVersion (método)

Recupera el número de versión del sistema de eventos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pnVersion* \[ enuncia\]
</dt> <dd>

Número de versión del sistema de eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ FAIL y S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




