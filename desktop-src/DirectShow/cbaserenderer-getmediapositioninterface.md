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
ms.openlocfilehash: 12e15b297f78b3386ae9ad31e749858bad14b87e59e938ac02a3cf3a9ca002a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872335"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>Método CBaseRenderer.GetMediaPositionInterface

El método recupera los punteros de interfaz `GetMediaPositionInterface` [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro.

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
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | No se admite la interfaz .<br/> |



 

## <a name="remarks"></a>Comentarios

El filtro delega todos los comandos de búsqueda en un [**objeto CRendererPosPassThru,**](crendererpospassthru.md) que los pasa de nivel superior. Este método crea el **objeto CRendererPosPassThru,** si aún no existe, y lo consulta para la interfaz solicitada.

La variable [**miembro CBaseRenderer::m \_ pPosition**](cbaserenderer-m-pposition.md) almacena un puntero al objeto **CRendererPosPassThru.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




