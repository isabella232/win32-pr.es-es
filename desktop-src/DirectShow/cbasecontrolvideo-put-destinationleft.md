---
description: El método put \_ DestinationLeft establece la coordenada izquierda del rectángulo de destino.
ms.assetid: 5d61d41c-3935-4637-b092-f508ea0508d3
title: CBaseControlVideo.put_DestinationLeft método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cccbba728e8a76024f79bf95711de11573e84310a463680b29ca91dbeafd00c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983715"
---
# <a name="cbasecontrolvideoput_destinationleft-method"></a>Método CBaseControlVideo.put \_ DestinationLeft

El `put_DestinationLeft` método establece la coordenada izquierda del rectángulo de destino.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_DestinationLeft(
   long DestinationLeft
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DestinationLeft* 
</dt> <dd>

Nueva coordenada izquierda del rectángulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT** que depende de la implementación; puede ser uno de los siguientes valores u otros valores no enumerados.



| Código devuelto                                                                                           | Descripción                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Error.<br/>                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Argumento no válido.<br/>                                                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>             | **Argumento de** puntero NULL.<br/>                                            |
| <dl> <dt>**NOERROR**</dt> </dl>                | Correcto.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | No se puede realizar la operación porque las clavijas no están conectadas.<br/> |



 

## <a name="remarks"></a>Comentarios

Una aplicación puede cambiar los rectángulos de origen y destino del vídeo a través de la [**interfaz IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) El rectángulo de origen afecta a la sección del origen de vídeo nativo que aparecerá en la pantalla; el rectángulo de destino afecta a dónde aparecerá el vídeo cuando se reproduce. El rectángulo de destino es relativo al área de cliente de la ventana en la que se reproduce. La esquina superior izquierda de la ventana es coordenada (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




