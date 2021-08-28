---
description: Indica la demora con la que llegan los ejemplos al representador, en unidades de tiempo de referencia. Sintaxis.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: CVideoTransformFilter::m_itrLate miembro (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba2d14d19849768538184e54de5ca84b9495371783d57231ab9ad6aa7738718
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075955"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>Miembro itrLate de CVideoTransformFilter::m \_

Indica la demora con la que llegan los ejemplos al representador, en unidades de tiempo de referencia. Syntax

## <a name="syntax"></a>Sintaxis


```C++
int m_itrLate;
```



## <a name="remarks"></a>Comentarios

Cuando el filtro recibe un mensaje de calidad de nivel inferior, almacena el valor de retraso en esta variable. A medida que el filtro quita fotogramas, actualiza este valor restando la duración de cada fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CVideoTransformFilter (clase)**](cvideotransformfilter.md)
</dt> </dl>

 

 




