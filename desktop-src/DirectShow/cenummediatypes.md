---
description: La clase CEnumMediaTypes implementa un enumerador para los tipos de medios preferidos.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: Clase CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671157"
---
# <a name="cenummediatypes-class"></a>Clase CEnumMediaTypes

![jerarquía de clases cenummediatypes](images/filter04.png)

La `CEnumMediaTypes` clase implementa un enumerador para los tipos de medios preferidos.

Esta clase implementa la interfaz [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) . Llama a los siguientes métodos [**CBasePin**](cbasepin.md) :

-   [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md): recupera un tipo de medio, al que hace referencia un índice basado en cero.
-   [**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): determina si ha cambiado el conjunto de tipos preferidos.

Cada vez que un PIN modifica su lista de tipos de medios preferidos, el PIN incrementa el número de versión del tipo de medio. Cuando esto sucede, el objeto de enumerador ya no se sincroniza con el PIN y los métodos de clase devuelven la \_ \_ enumeración VFW E enum \_ \_ \_ . Llame al método [**CEnumMediaTypes:: RESET**](cenummediatypes-reset.md) para volver a sincronizar el enumerador.



| Métodos públicos                                               | Descripción                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [**CEnumMediaTypes**](cenummediatypes-cenummediatypes.md)   | Método de constructor.                                             |
| [**~ CEnumMediaTypes**](cenummediatypes--cenummediatypes.md) | Método de destructor. Virtualiza.                                     |
| Métodos IEnumMediaTypes                                      | Descripción                                                     |
| [**Clonar**](cenummediatypes-clone.md)                       | Realiza una copia del enumerador con el mismo estado de enumeración. |
| [**Next**](cenummediatypes-next.md)                         | Recupera un número especificado de tipos de medios.                    |
| [**Reset**](cenummediatypes-reset.md)                       | Restablece la secuencia de enumeración al principio.               |
| [**Omitir**](cenummediatypes-skip.md)                         | Omite un número especificado de tipos de medios.                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




