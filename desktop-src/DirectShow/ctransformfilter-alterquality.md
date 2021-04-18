---
description: El método AlterQuality notifica al filtro que se ha solicitado un cambio de calidad.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Método CTransformFilter. AlterQuality (Transfrm. h)
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
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660305"
---
# <a name="ctransformfilteralterquality-method"></a>CTransformFilter. AlterQuality, método

El `AlterQuality` método notifica al filtro que se ha solicitado un cambio de calidad.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*respuestas* 
</dt> <dd>

Estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | No controló el mensaje de calidad. El mensaje se debe pasar al nivel superior.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Controló el mensaje de calidad. No es necesario realizar ninguna acción.<br/>               |



 

## <a name="remarks"></a>Observaciones

Invalide este método si el filtro puede realizar el control de calidad. Para obtener más información, vea [Administración de control de calidad](quality-control-management.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




