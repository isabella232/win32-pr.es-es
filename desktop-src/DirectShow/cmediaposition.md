---
description: La clase CMediaPosition controla los métodos IDispatch de la interfaz dual IMediaPosition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: Clase CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679298"
---
# <a name="cmediaposition-class"></a>Clase CMediaPosition

![jerarquía de clases cmediaposition](images/cutil14.png)

La clase **CMediaPosition** controla los métodos **IDispatch** de la interfaz dual [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .

Esta clase hereda la interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) , pero no la implementa. Implementa **IDispatch** a través de la clase [**CBaseDispatch**](cbasedispatch.md) y la biblioteca de tipos de DirectShow. No utilice esta clase directamente. En su lugar, utilice una de las clases siguientes:

-   Filtros de origen: Use la clase base [**CSourceSeeking**](csourceseeking.md) para implementar operaciones de búsqueda.
-   Filtros de transformación: Use la clase [**CPosPassThru**](cpospassthru.md) para pasar los comandos de búsqueda ascendentes.
-   Representadores: Use la clase [**CRendererPosPassThru**](crendererpospassthru.md) para pasar comandos de búsqueda ascendentes.



| Métodos públicos                                              | Descripción                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CMediaPosition**](cmediaposition-cmediaposition.md)     | Método de constructor.                                                                                                 |
| Métodos IDispatch                                           | Descripción                                                                                                         |
| [**GetIDsOfNames**](cmediaposition-getidsofnames.md)       | Asigna un conjunto de nombres a un conjunto correspondiente de DispId.                                                              |
| [**GetTypeInfo**](cmediaposition-gettypeinfo.md)           | Recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz. |
| [**GetTypeInfoCount**](cmediaposition-gettypeinfocount.md) | Recupera el número de interfaces de información de tipo que proporciona el objeto.                                            |
| [**Invocar**](cmediaposition-invoke.md)                     | Proporciona acceso a las propiedades y los métodos expuestos por el objeto.                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases base de DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




