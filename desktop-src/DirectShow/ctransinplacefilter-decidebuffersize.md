---
description: El método DecideBufferSize establece los requisitos de búfer del terminal de salida.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Método CTransInPlaceFilter. DecideBufferSize (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679291"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a>CTransInPlaceFilter. DecideBufferSize, método

El `DecideBufferSize` método establece los requisitos de búfer del terminal de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAlloc* 
</dt> <dd>

Puntero al objeto [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usado por el PIN de salida.

</dd> <dt>

*pProperties* 
</dt> <dd>

Puntero a las propiedades de asignador solicitadas para el recuento, el tamaño y la alineación, tal y como especifica la estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                            | Descripción        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Error<br/> |



 

## <a name="remarks"></a>Observaciones

Se llama a este método cuando la clase **CTransInPlaceFilter** debe proporcionar un tamaño de búfer al filtro de nivel inferior. Si el filtro **CTransInPlaceFilter** ya está conectado al nivel superior, usa las propiedades de asignador en la conexión de PIN de nivel superior. De lo contrario, establece el tamaño del búfer en 1 byte como un valor de marcador de posición temporal. Cuando se conecta el filtro de nivel superior, la clase **CTransInPlaceFilter** vuelve a negociar el asignador de bajada. Para obtener más información sobre el proceso de conexión de PIN en esta clase, vea [**CTransInPlaceFilter (clase**](ctransinplacefilter.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




