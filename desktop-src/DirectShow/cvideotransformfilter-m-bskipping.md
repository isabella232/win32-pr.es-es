---
description: Valor booleano que indica si el filtro está quitando actualmente fotogramas. Si este valor es TRUE, el filtro sigue colocando fotogramas hasta que alcanza el siguiente fotograma clave o hasta que recibe 30 fotogramas Delta en una fila sin un fotograma clave.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'Miembro CVideoTransformFilter:: m_bSkipping (Vtrans. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660928"
---
# <a name="cvideotransformfilterm_bskipping-member"></a>Miembro bSkipping CVideoTransformFilter:: m \_

Valor booleano que indica si el filtro está quitando actualmente fotogramas. Si este valor es **true**, el filtro sigue colocando fotogramas hasta que alcanza el siguiente fotograma clave o hasta que recibe 30 fotogramas Delta en una fila sin un fotograma clave.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




