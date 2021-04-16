---
description: La clase CImageSample implementa un ejemplo multimedia que administra un mapa de bits independiente del dispositivo GDI (DIB).
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: Clase CImageSample (Winutil. h)
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
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679031"
---
# <a name="cimagesample-class"></a>Clase CImageSample

![jerarquía de clases cimagesample](images/wutil03.png)

La `CImageSample` clase implementa un ejemplo multimedia que administra un mapa de bits independiente del dispositivo GDI (DIB). Esta clase se deriva de la clase [**CMediaSample**](cmediasample.md) . Está diseñado para usarse con la clase [**CImageAllocator**](cimageallocator.md) . La clase **CImageAllocator** proporciona un asignador que crea `CImageSample` objetos.



| Variables de miembro protegidas                        | Descripción                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [**m \_ DibData**](cimagesample-m-dibdata.md)      | Contiene información sobre el DIB que está administrando este objeto.  |
| [**m \_ bInit**](cimagesample-m-binit.md)          | Indica si el objeto se ha inicializado.                |
| Métodos públicos                                    | Descripción                                                       |
| [**CImageSample**](cimagesample-cimagesample.md) | Método de constructor.                                               |
| [**GetDIBData**](cimagesample-getdibdata.md)     | Recupera información sobre el DIB que está administrando este objeto. |
| [**SetDIBData**](cimagesample-setdibdata.md)     | Establece información sobre el DIB que está administrando este objeto.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




