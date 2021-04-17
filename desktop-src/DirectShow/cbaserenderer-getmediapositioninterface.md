---
description: El método GetMediaPositionInterface recupera los punteros de interfaz IMediaPosition y IMediaSeeking del filtro.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Método CBaseRenderer. GetMediaPositionInterface (Renbase. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670561"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>CBaseRenderer. GetMediaPositionInterface, método

El `GetMediaPositionInterface` método recupera los punteros de interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) y [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro.

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

*PPV* 
</dt> <dd>

Dirección de una variable que recibe el puntero de interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>     |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | No se admite la interfaz.<br/> |



 

## <a name="remarks"></a>Observaciones

El filtro delega todos los comandos de búsqueda en un objeto [**CRendererPosPassThru**](crendererpospassthru.md) , que los pasa arriba. Este método crea el objeto **CRendererPosPassThru** , si aún no existe, y lo consulta para la interfaz solicitada.

La variable miembro [**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md) almacena un puntero al objeto **CRendererPosPassThru** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




