---
description: El \_ método get SourceLeft recupera la coordenada izquierda del rectángulo de origen actual.
ms.assetid: dbfb1850-6e49-481c-b26a-22ccb9e4455a
title: Método CBaseControlVideo.get_SourceLeft (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2b7ff62617b9fa378511dba2838f0dcbdb25dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660516"
---
# <a name="cbasecontrolvideoget_sourceleft-method"></a>CBaseControlVideo. Get \_ SourceLeft (método)

El `get_SourceLeft` método recupera la coordenada izquierda del rectángulo de origen actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SourceLeft(
   long *pSourceLeft
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSourceLeft* 
</dt> <dd>

Puntero a la coordenada izquierda del rectángulo de origen actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.



| Código devuelto                                                                                           | Descripción                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Error.<br/>                                                              |
| <dl> <dt>**\_puntero E**</dt> </dl>             | Argumento de puntero **nulo** .<br/>                                            |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | No se puede realizar la operación porque los PIN no están conectados.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Correcto.<br/>                                                              |



 

## <a name="remarks"></a>Observaciones

Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca. El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce. La esquina superior izquierda de la ventana es la coordenada (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




