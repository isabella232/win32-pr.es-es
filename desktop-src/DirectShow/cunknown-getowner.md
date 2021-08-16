---
description: El método GetOwner recupera un puntero a la interfaz IUnknown del componente propietario. Para un componente agregado, el propietario es el componente externo. De lo contrario, el componente se posee a sí mismo.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Método CUnknown.GetOwner (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c741a6820d414d7a00ad0a9fef768d982f2335c9cb9d8417e42376ea243cc58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076045"
---
# <a name="cunknowngetowner-method"></a>Método CUnknown.GetOwner

El `GetOwner` método recupera un puntero a la interfaz **IUnknown** del componente propietario. Para un componente agregado, el propietario es el componente externo. De lo contrario, el componente se posee a sí mismo.

## <a name="syntax"></a>Sintaxis


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la interfaz **IUnknown de** control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




