---
description: El método get \_ DestinationHeight recupera el alto del rectángulo de destino actual.
ms.assetid: 0001d98a-3a5c-47f1-8f5e-ce464d64131a
title: CBaseControlVideo.get_DestinationHeight método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57e2eb96a36f0902dccbba052080fa27b5e61f96b852bf44bd1a238d59010145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057285"
---
# <a name="cbasecontrolvideoget_destinationheight-method"></a>Método CBaseControlVideo.get \_ DestinationHeight

El `get_DestinationHeight` método recupera el alto del rectángulo de destino actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DestinationHeight(
   long *pDestinationHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestinationHeight* 
</dt> <dd>

Puntero al alto de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT** que depende de la implementación; puede ser uno de los siguientes valores u otros valores no enumerados.



| Código devuelto                                                                                           | Descripción                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Error.<br/>                                                              |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>             | Argumento de puntero **NULL.**<br/>                                            |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | No se puede realizar la operación porque los pines no están conectados.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Correcto.<br/>                                                              |



 

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IBasicVideo::get \_ DestinationHeight.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight)

Una aplicación puede cambiar los rectángulos de origen y destino del vídeo a través de la [**interfaz IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla; el rectángulo de destino afecta a dónde se reproducirá. El rectángulo de destino es relativo al área de cliente de la ventana en la que se reproduce. La esquina superior izquierda de la ventana es coordenada (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




