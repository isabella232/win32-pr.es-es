---
description: La clase CImageAllocator implementa un asignador que administra mapas de bits independientes del dispositivo (DIB) de GDI. Esta clase se deriva de la clase CBaseAllocator. Crea ejemplos multimedia que se implementan mediante la clase CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: CImageAllocator (clase, Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251169"
---
# <a name="cimageallocator-class"></a>CImageAllocator (clase)

![jerarquía de clases cimageallocator](images/wutil04.png)

La clase implementa un asignador que administra mapas de bits independientes del dispositivo `CImageAllocator` GDI (DIB). Esta clase se deriva de la [**clase CBaseAllocator.**](cbaseallocator.md) Crea ejemplos multimedia que se implementan mediante la [**clase CImageSample.**](cimagesample.md)

Dos pines conectados comparten un asignador, pero siempre es propiedad de uno de los filtros de la conexión. Un filtro que usa debe realizar un seguimiento de si el asignador se proporcionó por sí mismo `CImageAllocator` o por el otro filtro. Si el asignador se proporcionó por sí mismo, el filtro propietario puede basarse en el hecho de que todos los ejemplos multimedia del asignador son **objetos CImageSample.** Por lo tanto, puede usar **el objeto CImageSample** para obtener información sobre la DIB, que se almacena en una [**estructura DIBDATA.**](dibdata.md)

El filtro propietario debe llamar a **NotifyMediaType cada** vez que cambie el tipo de medio.



| Variables de miembro protegido                                     | Descripción                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pFilter**](cimageallocator-m-pfilter.md)                | Puntero al filtro propietario.                                            |
| [**m \_ pMediaType**](cimageallocator-m-pmediatype.md)          | Puntero al tipo de medio actual.                                       |
| Métodos protegidos                                              | Descripción                                                              |
| [**Alloc**](cimageallocator-alloc.md)                         | Asigna memoria para los búferes.                                        |
| [**CheckSizes**](cimageallocator-checksizes.md)               | Comprueba las propiedades del asignador con el tipo de medio actual.              |
| [**CreateDIB**](cimageallocator-createdib.md)                 | Crea una DIB.                                                           |
| [**CreateImageSample**](cimageallocator-createimagesample.md) | Crea un ejemplo multimedia. Virtual.                                         |
| [**Gratuito**](cimageallocator-free.md)                           | Libera toda la memoria del búfer.                                       |
| Métodos públicos                                                 | Descripción                                                              |
| [**CImageAllocator**](cimageallocator-cimageallocator.md)     | Método constructor.                                                      |
| [**NotifyMediaType**](cimageallocator-notifymediatype.md)     | Informa al objeto del tipo de medio actual.                            |
| Métodos IMemAllocator                                          | Descripción                                                              |
| [**SetProperties**](cimageallocator-setproperties.md)         | Especifica el número de búferes que se asignarán y el tamaño de cada búfer. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 




