---
description: El método get \_ DestinationTop recupera la coordenada superior del rectángulo de destino actual.
ms.assetid: 8d5c1361-18db-4ea1-a507-781397189630
title: CBaseControlVideo.get_DestinationTop método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2c7d450c50b11186546a25ceebd317a308dd805
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255590"
---
# <a name="cbasecontrolvideoget_destinationtop-method"></a>Método CBaseControlVideo.get \_ DestinationTop

El `get_DestinationTop` método recupera la coordenada superior del rectángulo de destino actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DestinationTop(
   long *pDestinationTop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestinationTop* 
</dt> <dd>

Puntero a la coordenada superior del rectángulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT** que depende de la implementación; puede ser uno de los siguientes valores u otros valores no enumerados.



| Código devuelto                                                                                           | Descripción                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Error.<br/>                                                              |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>             | **Argumento de** puntero NULL.<br/>                                            |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | No se puede realizar la operación porque las clavijas no están conectadas.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Correcto.<br/>                                                              |



 

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el [**método IBasicVideo::get \_ DestinationTop.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationtop)

Una aplicación puede cambiar los rectángulos de origen y destino del vídeo a través de la [**interfaz IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla; el rectángulo de destino afecta a dónde aparecerá el vídeo cuando se reproduce. El rectángulo de destino es relativo al área de cliente de la ventana en la que se reproduce. La esquina superior izquierda de la ventana es coordenada (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




