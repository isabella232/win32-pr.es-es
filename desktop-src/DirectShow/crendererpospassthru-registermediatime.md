---
description: El método RegisterMediaTime almacena en caché las marcas de tiempo del ejemplo actual.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Método CRendererPosPassThru.RegisterMediaTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69688bb011fc8a75b0ec52effaef3afd7972fb7a198a4cdedf20c07a40c4fa7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054385"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Método CRendererPosPassThru.RegisterMediaTime (Ctlutil.h)

El **método RegisterMediaTime** almacena en caché las marcas de tiempo del ejemplo actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                                  | Descripción                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Correcto.<br/>                        |
| <dl> <dt>**TIEMPO DE MEDIOS DE VFW \_ E \_ NO \_ \_ \_ ESTABLECIDO**</dt> </dl> | El ejemplo no tiene marca de tiempo.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método almacena las marcas de tiempo del ejemplo actual. El [**método CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) recupera los mismos valores.

El filtro debe llamar a este método para cada muestra que reciba. El método se sobrecarga para aceptar un puntero al ejemplo o los propios valores de marca de tiempo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




