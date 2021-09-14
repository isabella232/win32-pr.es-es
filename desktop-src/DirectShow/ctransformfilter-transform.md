---
description: El método Transform transforma un ejemplo de entrada para generar un ejemplo de salida.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: Método CTransformFilter.Transform (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246633"
---
# <a name="ctransformfiltertransform-method"></a>Método CTransformFilter.Transform

El `Transform` método transforma un ejemplo de entrada para generar un ejemplo de salida.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*anclar* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo de entrada.

</dd> <dt>

*Puchero* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La clase base devuelve E \_ UNEXPECTED.

La clase derivada debe devolver un **valor HRESULT,** lo que indica que se ha hecho correctamente o no. Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | No entregue este ejemplo.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                    |



 

## <a name="remarks"></a>Observaciones

Invalide este método para generar datos de salida. Lea los datos de entrada del ejemplo especificado por el parámetro *pIn* y escriba los nuevos datos en el ejemplo especificado por el *parámetro pOut.*

Antes de que el filtro llame a este método, copia las propiedades del ejemplo de entrada al ejemplo de salida. El método debe establecer las propiedades que difieren entre los dos ejemplos, mediante métodos `Transform` **IMediaSample** o la [**interfaz IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) (si está disponible).

Si el filtro no debe entregar este ejemplo (por ejemplo, para admitir el control de calidad), el método debe devolver S \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




