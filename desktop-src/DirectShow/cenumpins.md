---
description: La clase CEnumPins implementa un enumerador para los pin.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Clase CEnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660856"
---
# <a name="cenumpins-class"></a>Clase CEnumPins

![jerarquía de clases cenumpins](images/filter03.png)

La `CEnumPins` clase implementa un enumerador para los pin.

Esta clase implementa la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) . Llama a los siguientes métodos [**CBaseFilter**](cbasefilter.md) :

-   [**CBaseFilter:: GetPin**](cbasefilter-getpin.md): recupera un PIN en el filtro, al que hace referencia un índice basado en cero.
-   [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md): recupera el número total de clavijas del filtro.
-   [**CBaseFilter:: GetPinVersion**](cbasefilter-getpinversion.md): determina si los pin han cambiado.

Si el filtro crea o destruye dinámicamente los pin, incrementa la versión del PIN cada vez que cambian los pin. Si el número de versión cambia, el objeto de enumerador ya no se sincroniza con el filtro. Una vez que el enumerador no está sincronizado, los métodos de `CEnumPins` devuelven la \_ enumeración VFW E no \_ \_ \_ \_ sincronizada. Llame al método [**CEnumPins:: RESET**](cenumpins-reset.md) para volver a sincronizar el enumerador.



| Métodos públicos                             | Descripción                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [**CEnumPins**](cenumpins-cenumpins.md)   | Método de constructor.                                             |
| [**~ CEnumPins**](cenumpins--cenumpins.md) | Método de destructor. Virtualiza.                                     |
| Métodos IEnumPins                          | Descripción                                                     |
| [**Clonar**](cenumpins-clone.md)           | Realiza una copia del enumerador con el mismo estado de enumeración. |
| [**Next**](cenumpins-next.md)             | Recupera un número especificado de clavijas.                           |
| [**Reset**](cenumpins-reset.md)           | Restablece la secuencia de enumeración al principio.               |
| [**Omitir**](cenumpins-skip.md)             | Omite un número especificado de clavijas.                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




