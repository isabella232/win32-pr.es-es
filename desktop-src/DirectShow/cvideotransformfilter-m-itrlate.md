---
description: Indica el nivel de finalización de las muestras en el representador, en unidades de tiempo de referencia. Sintáctica.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Miembro CVideoTransformFilter:: m_itrLate (Vtrans. h)'
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
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660927"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>Miembro itrLate CVideoTransformFilter:: m \_

Indica el nivel de finalización de las muestras en el representador, en unidades de tiempo de referencia. Sintaxis

## <a name="syntax"></a>Sintaxis


```C++
int m_itrLate;
```



## <a name="remarks"></a>Observaciones

Cuando el filtro recibe un mensaje de calidad de nivel inferior, almacena el valor de retraso en esta variable. A medida que el filtro quita fotogramas, actualiza este valor restando la duración de cada fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




