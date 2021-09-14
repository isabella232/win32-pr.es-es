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
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266503"
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

 

 




