---
description: Comprueba la existencia de todos los suscriptores transitorios en el almacén de datos. Al llamar a este método, puede asegurarse de que todos los suscriptores transitorios enumerados en el almacén de datos estén activos.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'IEventSystem2:: VerifyTransientSubscribers (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998244"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a>IEventSystem2:: VerifyTransientSubscribers (método)

Comprueba la existencia de todos los suscriptores transitorios en el almacén de datos. Al llamar a este método, puede asegurarse de que todos los suscriptores transitorios enumerados en el almacén de datos estén activos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

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

 

 




