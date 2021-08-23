---
description: El método IsValid determina si se ha asignado un tipo principal a este objeto.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Método CMediaType.IsValid (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611d36cfe19623840f102b820b2b312138b1e116d32fc399927da57e7f47300
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016273"
---
# <a name="cmediatypeisvalid-method"></a>CMediaType.IsValid (método)

El método determina si se ha asignado un tipo `IsValid` principal a este objeto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se ha asignado un tipo principal a este objeto. De lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Comentarios

De forma predeterminada, [**los objetos CMediaType**](cmediatype.md) se inicializan con un tipo principal de GUID \_ NULL. Llame a este método para determinar si el objeto se ha inicializado correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




