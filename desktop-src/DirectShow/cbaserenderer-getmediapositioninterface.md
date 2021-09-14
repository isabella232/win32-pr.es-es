---
description: El método GetMediaPositionInterface recupera los punteros de interfaz IMediaPosition e IMediaSeeking del filtro.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Método CBaseRenderer.GetMediaPositionInterface (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061331"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>Método CBaseRenderer.GetMediaPositionInterface

El `GetMediaPositionInterface` método recupera los punteros de interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* 
</dt> <dd>

Identificador de referencia de la interfaz.

</dd> <dt>

*Ppv* 
</dt> <dd>

Dirección de una variable que recibe el puntero de interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>     |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | Interfaz no admitida.<br/> |



 

## <a name="remarks"></a>Observaciones

El filtro delega todos los comandos de búsqueda en un [**objeto CRendererPosPassThru,**](crendererpospassthru.md) que los pasa en sentido ascendente. Este método crea el **objeto CRendererPosPassThru,** si aún no existe, y lo consulta para la interfaz solicitada.

La variable [**miembro CBaseRenderer::m \_ pPosition**](cbaserenderer-m-pposition.md) almacena un puntero al **objeto CRendererPosPassThru.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




