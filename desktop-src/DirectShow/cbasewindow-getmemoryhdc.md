---
description: El método GetMemoryHDC recupera un identificador en el contexto del dispositivo de memoria (DC).
ms.assetid: 2c22015f-5948-4e1a-92c7-36f232816175
title: Método CBaseWindow.GetMemoryHDC (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetMemoryHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36874817d2e1dd13c00577a91cff7f059c1f2441701012af202c4765cb23088a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016663"
---
# <a name="cbasewindowgetmemoryhdc-method"></a>Método CBaseWindow.GetMemoryHDC

El `GetMemoryHDC` método recupera un identificador para el contexto del dispositivo de memoria (DC).

## <a name="syntax"></a>Sintaxis


```C++
virtual HDC GetMemoryHDC();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador al controlador de dominio de memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




