---
description: Valor booleano que indica si el filtro está quitando fotogramas actualmente. Si este valor es TRUE, el filtro continúa colocando fotogramas hasta que alcanza el siguiente fotograma clave o hasta que recibe 30 fotogramas delta en una fila sin un fotograma clave.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: CVideoTransformFilter::m_bSkipping miembro (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f865bdc707b206a8528413a357a4e14bcfe88fff813e1f62a44d30e6f4843ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821920"
---
# <a name="cvideotransformfilterm_bskipping-member"></a>Miembro CVideoTransformFilter::m \_ bSkipping

Valor booleano que indica si el filtro está quitando fotogramas actualmente. Si este valor es **TRUE,** el filtro continúa colocando fotogramas hasta que alcanza el siguiente fotograma clave o hasta que recibe 30 fotogramas delta en una fila sin un fotograma clave.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CVideoTransformFilter (clase)**](cvideotransformfilter.md)
</dt> </dl>

 

 




