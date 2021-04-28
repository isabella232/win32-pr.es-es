---
description: 'Método CBaseInputPin.NotifyAllocator: el método NotifyAllocator especifica un asignador para la conexión. Este método implementa el método IMemInputPin::NotifyAllocator.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Método CBaseInputPin.NotifyAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c63e448d0cf2d287a441a4983f6a2e06bd9b8151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099722"
---
# <a name="cbaseinputpinnotifyallocator-method"></a>CBaseInputPin.NotifyAllocator (método)

El `NotifyAllocator` método especifica un asignador para la conexión. Este método implementa el [**método IMemInputPin::NotifyAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAllocator* 
</dt> <dd>

Puntero a la interfaz [**IMemAllocator del asignador.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Marca que especifica si los ejemplos de este asignador son de solo lectura. Si **es TRUE,** los ejemplos son de solo lectura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Durante la conexión de anclado, el pin de salida elige un asignador y llama a este método para notificar al pin de entrada. El pin de salida puede usar el asignador que el pin de entrada propuesto en el método [**IMemInputPin::GetAllocator,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) o puede proporcionar su propio asignador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




