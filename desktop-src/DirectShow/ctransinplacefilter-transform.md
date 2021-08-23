---
description: El método Transform transforma un ejemplo en su lugar.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Método CTransInPlaceFilter.Transform (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224052bc882792f57eedf9ea58842b953e5853012d3581ef14cad58467b614b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953404"
---
# <a name="ctransinplacefiltertransform-method"></a>Método CTransInPlaceFilter.Transform

El `Transform` método transforma un ejemplo en su lugar.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | No entregue este ejemplo.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                    |



 

## <a name="remarks"></a>Comentarios

La clase derivada debe implementar este método. Transforme los datos de ejemplo en su lugar. Si el filtro usa dos asignadores, copia los datos del ejemplo de entrada en un nuevo ejemplo y pasa la copia a este método.

Si el filtro no debe entregar este ejemplo (por ejemplo, para admitir el control de calidad), el método debe devolver S \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




