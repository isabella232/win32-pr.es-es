---
description: Identificador de la instancia del módulo.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: CBaseWindow::m_hInstance miembro (Winutil.h)
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
ms.openlocfilehash: ddf1da2d7f947bbaed9972a40a20497a81f84ebda68dba31cd5518b64f6e8434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016533"
---
# <a name="cbasewindowm_hinstance-member"></a>Miembro CBaseWindow::m \_ hInstance

Identificador de la instancia del módulo.

## <a name="syntax"></a>Sintaxis


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>Comentarios

La función de punto de entrada dll establece una variable global con un identificador para la instancia del módulo. La **clase CBaseWindow** almacena este identificador en su método de constructor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




