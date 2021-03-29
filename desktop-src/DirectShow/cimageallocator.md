---
description: La clase CImageAllocator implementa un asignador que administra mapas de bits independientes del dispositivo GDI (DIB). Esta clase se deriva de la clase CBaseAllocator. Crea ejemplos de medios que se implementan mediante la clase CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Clase CImageAllocator (Winutil. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679087"
---
# <a name="cimageallocator-class"></a>Clase CImageAllocator

![jerarquía de clases cimageallocator](images/wutil04.png)

La `CImageAllocator` clase implementa un asignador que administra los mapas de bits independientes del dispositivo GDI (DIB). Esta clase se deriva de la clase [**CBaseAllocator**](cbaseallocator.md) . Crea ejemplos de medios que se implementan mediante la clase [**CImageSample**](cimagesample.md) .

Dos clavijas conectadas comparten un asignador, pero siempre pertenece a uno de los filtros de la conexión. Un filtro que utiliza `CImageAllocator` debe realizar un seguimiento de si el asignador se proporcionó por sí solo o por el otro filtro. Si el asignador se proporcionó por sí solo, el filtro propietario puede basarse en el hecho de que todos los ejemplos de medios del asignador son objetos **CImageSample** . Por tanto, puede usar el objeto **CImageSample** para obtener información sobre el DIB, que se almacena en una estructura [**DIBDATA**](dibdata.md) .

El filtro propietario debe llamar a **NotifyMediaType** cada vez que cambie el tipo de medio.



| Variables de miembro protegidas                                     | Descripción                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pFilter**](cimageallocator-m-pfilter.md)                | Puntero al filtro propietario.                                            |
| [**m \_ pMediaType**](cimageallocator-m-pmediatype.md)          | Puntero al tipo de medio actual.                                       |
| Métodos protegidos                                              | Descripción                                                              |
| [**Alloc**](cimageallocator-alloc.md)                         | Asigna memoria a los búferes.                                        |
| [**CheckSizes**](cimageallocator-checksizes.md)               | Comprueba las propiedades del asignador con el tipo de medio actual.              |
| [**CreateDIB**](cimageallocator-createdib.md)                 | Crea un DIB.                                                           |
| [**CreateImageSample**](cimageallocator-createimagesample.md) | Crea un ejemplo multimedia. Virtualiza.                                         |
| [**Gratuito**](cimageallocator-free.md)                           | Libera toda la memoria del búfer.                                       |
| Métodos públicos                                                 | Descripción                                                              |
| [**CImageAllocator**](cimageallocator-cimageallocator.md)     | Método de constructor.                                                      |
| [**NotifyMediaType**](cimageallocator-notifymediatype.md)     | Informa al objeto del tipo de medio actual.                            |
| Métodos IMemAllocator                                          | Descripción                                                              |
| [**SetProperties**](cimageallocator-setproperties.md)         | Especifica el número de búferes que se van a asignar y el tamaño de cada búfer. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




