---
description: 'Método CTransInPlaceFilter.DecideBufferSize: el método DecideBufferSize establece los requisitos de búfer del pin de salida.'
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Método CTransInPlaceFilter.DecideBufferSize (Transip.h)
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
ms.openlocfilehash: 5ea1034db2965e736224348707bfc9c3d7dcd27fd37fa5c511d147635b9d51cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831375"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a>Método CTransInPlaceFilter.DecideBufferSize

El `DecideBufferSize` método establece los requisitos de búfer del pin de salida.

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

Puntero al objeto [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usado por el pin de salida.

</dd> <dt>

*pProperties* 
</dt> <dd>

Puntero a las propiedades de asignador solicitadas para el recuento, el tamaño y la alineación, tal y como especifica la [**estructura ALLOCATOR \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-allocator_properties)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                            | Descripción        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Error<br/> |



 

## <a name="remarks"></a>Comentarios

Se llama a este método cuando **la clase CTransInPlaceFilter** necesita proporcionar un tamaño de búfer al filtro de nivel inferior. Si el **filtro CTransInPlaceFilter** ya está conectado en sentido ascendente, usa las propiedades del asignador en la conexión de pin ascendente. De lo contrario, establece el tamaño del búfer en 1 byte como un valor de posición temporal. Cuando se conecta el filtro ascendente, la **clase CTransInPlaceFilter** vuelve a negociar el asignador de nivel inferior. Para obtener más información sobre el proceso de conexión de anclar en esta clase, vea [**CTransInPlaceFilter (Clase).**](ctransinplacefilter.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




