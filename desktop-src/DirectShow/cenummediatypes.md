---
description: La clase CEnumMediaTypes implementa un enumerador para los tipos de medios preferidos.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: CEnumMediaTypes (clase, Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973882"
---
# <a name="cenummediatypes-class"></a>CEnumMediaTypes (clase)

![cenummediatypes (jerarquía de clases)](images/filter04.png)

La `CEnumMediaTypes` clase implementa un enumerador para los tipos de medios preferidos.

Esta clase implementa la [**interfaz IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) Llama a los métodos [**CBasePin**](cbasepin.md) siguientes:

-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md):Recupera un tipo de medio al que hace referencia un índice de base cero.
-   [**CBasePin::GetMediaTypeVersion:**](cbasepin-getmediatypeversion.md)determina si el conjunto de tipos preferidos ha cambiado.

Cada vez que un pin modifica su lista de tipos de medios preferidos, el pin incrementa el número de versión del tipo de medio. Cuando esto sucede, el objeto enumerador ya no se sincroniza con el pin y los métodos de clase devuelven VFW \_ E \_ ENUM \_ OUT OF \_ \_ SYNC. Llame al [**método CEnumMediaTypes::Reset**](cenummediatypes-reset.md) para volver a sincronizar el enumerador.



| Métodos públicos                                               | Descripción                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [**CEnumMediaTypes**](cenummediatypes-cenummediatypes.md)   | Método constructor.                                             |
| [**~CEnumMediaTypes**](cenummediatypes--cenummediatypes.md) | Método destructor. Virtual.                                     |
| Métodos IEnumMediaTypes                                      | Descripción                                                     |
| [**Clonar**](cenummediatypes-clone.md)                       | Realiza una copia del enumerador con el mismo estado de enumeración. |
| [**Next**](cenummediatypes-next.md)                         | Recupera un número especificado de tipos de medios.                    |
| [**Reset**](cenummediatypes-reset.md)                       | Restablece la secuencia de enumeración al principio.               |
| [**Saltar**](cenummediatypes-skip.md)                         | Omite un número especificado de tipos de medios.                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




