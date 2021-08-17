---
description: El método AlterQuality notifica al filtro que se solicita un cambio de calidad.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Método CTransformFilter.AlterQuality (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b9b136217c23f64bcd779f5c96189ca993646ffb29ce5316cf5913de8c9abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317155"
---
# <a name="ctransformfilteralterquality-method"></a>Método CTransformFilter.AlterQuality

El `AlterQuality` método notifica al filtro que se solicita un cambio de calidad.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Q* 
</dt> <dd>

[**Estructura de**](/windows/win32/api/strmif/ns-strmif-quality) calidad que contiene el mensaje de control de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | No controló el mensaje de calidad. El mensaje debe pasarse en sentido ascendente.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Controló el mensaje de calidad. No es necesario realizar ninguna acción.<br/>               |



 

## <a name="remarks"></a>Comentarios

Invalide este método si el filtro puede realizar el control de calidad. Para obtener más información, vea [Administración de control de calidad.](quality-control-management.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




