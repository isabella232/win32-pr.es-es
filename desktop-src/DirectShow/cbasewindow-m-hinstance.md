---
description: Identificador de la instancia de módulo.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Miembro CBaseWindow:: m_hInstance (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660323"
---
# <a name="cbasewindowm_hinstance-member"></a>Miembro hInstance CBaseWindow:: m \_

Identificador de la instancia de módulo.

## <a name="syntax"></a>Sintaxis


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>Observaciones

La función de punto de entrada de DLL establece una variable global con un identificador para la instancia de módulo. La clase **CBaseWindow** almacena este identificador en su método constructor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




