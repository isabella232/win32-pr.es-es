---
description: Comprueba la existencia de todos los suscriptores transitorios en el almacén de datos. Al llamar a este método, puede asegurarse de que todos los suscriptores transitorios enumerados en el almacén de datos están activos.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: IEventSystem2::VerifyTransientSubscribers (método)
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
ms.openlocfilehash: 9b147a8910ef3574b93389088af798a84265dd7f929b458e9bd94232cc586a17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070615"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a>IEventSystem2::VerifyTransientSubscribers (método)

Comprueba la existencia de todos los suscriptores transitorios en el almacén de datos. Al llamar a este método, puede asegurarse de que todos los suscriptores transitorios enumerados en el almacén de datos están activos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

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

 

 




