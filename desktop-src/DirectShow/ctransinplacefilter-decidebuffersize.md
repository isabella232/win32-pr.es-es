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
ms.openlocfilehash: b3ffb3ec7b1ef59c6e7f3d49e39fbe69e8cc1c08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255285"
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

Puntero al [**objeto IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usado por el pin de salida.

</dd> <dt>

*pProperties* 
</dt> <dd>

Puntero a las propiedades de asignador solicitadas para count, size y alignment, tal y como especifica la [**estructura ALLOCATOR \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-allocator_properties)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                            | Descripción        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Error<br/> |



 

## <a name="remarks"></a>Observaciones

Se llama a este método cuando **la clase CTransInPlaceFilter** necesita proporcionar un tamaño de búfer al filtro de nivel inferior. Si el **filtro CTransInPlaceFilter** ya está conectado ascendente, usa las propiedades del asignador en la conexión de pin ascendente. De lo contrario, establece el tamaño del búfer en 1 byte como un valor de colocación temporal. Cuando se conecta el filtro ascendente, la **clase CTransInPlaceFilter** vuelve a negociar el asignador de nivel inferior. Para obtener más información sobre el proceso de conexión de anclar en esta clase, vea [**CTransInPlaceFilter (Clase).**](ctransinplacefilter.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




