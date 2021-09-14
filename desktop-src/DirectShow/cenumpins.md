---
description: La clase CEnumPins implementa un enumerador para los pines.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: CEnumPins (clase, Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255525"
---
# <a name="cenumpins-class"></a>CEnumPins (clase)

![jerarquía de clases cenumpins](images/filter03.png)

La `CEnumPins` clase implementa un enumerador para los pines.

Esta clase implementa la [**interfaz IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) Llama a los métodos [**CBaseFilter**](cbasefilter.md) siguientes:

-   [**CBaseFilter::GetPin:**](cbasefilter-getpin.md)recupera un pin en el filtro al que hace referencia un índice de base cero.
-   [**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md): recupera el número total de pines del filtro.
-   [**CBaseFilter::GetPinVersion:**](cbasefilter-getpinversion.md)determina si los pines han cambiado.

Si el filtro crea o destruye de forma dinámica los pins, incrementa la versión del pin cada vez que cambian. Si cambia el número de versión, el objeto enumerador ya no se sincroniza con el filtro. Una vez que el enumerador no está sincronizado, los métodos de `CEnumPins` devuelven VFW \_ E \_ ENUM \_ OUT OF \_ \_ SYNC. Llame al [**método CEnumPins::Reset**](cenumpins-reset.md) para volver a sincronizar el enumerador.



| Métodos públicos                             | Descripción                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [**CEnumPins**](cenumpins-cenumpins.md)   | Método constructor.                                             |
| [**~CEnumPins**](cenumpins--cenumpins.md) | Método destructor. Virtual.                                     |
| Métodos de IEnumPins                          | Descripción                                                     |
| [**Clonar**](cenumpins-clone.md)           | Realiza una copia del enumerador con el mismo estado de enumeración. |
| [**Next**](cenumpins-next.md)             | Recupera un número especificado de pines.                           |
| [**Reset**](cenumpins-reset.md)           | Restablece la secuencia de enumeración al principio.               |
| [**Saltar**](cenumpins-skip.md)             | Omite un número especificado de pines.                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




