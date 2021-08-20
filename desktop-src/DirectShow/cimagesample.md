---
description: La clase CImageSample implementa un ejemplo multimedia que administra un mapa de bits independiente del dispositivo GDI (DIB).
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: CImageSample (clase, Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afd19b6aba7546ec420985adf6d58d3f7acc7546913ec8f1c168c80ad3b7ffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402417"
---
# <a name="cimagesample-class"></a>CImageSample (clase)

![Jerarquía de clases cimagesample](images/wutil03.png)

La clase implementa un ejemplo multimedia que administra un mapa de bits independiente `CImageSample` del dispositivo GDI (DIB). Esta clase se deriva de la [**clase CMediaSample.**](cmediasample.md) Está pensado para usarse con la [**clase CImageAllocator.**](cimageallocator.md) La **clase CImageAllocator** proporciona un asignador que crea `CImageSample` objetos .



| Variables miembro protegidas                        | Descripción                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [**m \_ DibData**](cimagesample-m-dibdata.md)      | Contiene información sobre la DIB que este objeto está administrando.  |
| [**m \_ bInit**](cimagesample-m-binit.md)          | Indica si el objeto se ha inicializado.                |
| Métodos públicos                                    | Descripción                                                       |
| [**CImageSample**](cimagesample-cimagesample.md) | Método constructor.                                               |
| [**GetDIBData**](cimagesample-getdibdata.md)     | Recupera información sobre la DIB que este objeto está administrando. |
| [**SetDIBData**](cimagesample-setdibdata.md)     | Establece información sobre la DIB que este objeto está administrando.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




