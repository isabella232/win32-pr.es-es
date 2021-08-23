---
description: La clase CMediaPosition controla los métodos IDispatch de la interfaz dual IMediaPosition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: CMediaPosition (clase, Ctlutil.h)
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
ms.openlocfilehash: 7305d5eded589e167352ce7ff13194b52965b939daf907e8381b64684a03d1bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634855"
---
# <a name="cmediaposition-class"></a>CMediaPosition (clase)

![Jerarquía de clases cmediaposition](images/cutil14.png)

La **clase CMediaPosition** controla los métodos **IDispatch** de la interfaz dual [**IMediaPosition.**](/windows/desktop/api/Control/nn-control-imediaposition)

Esta clase hereda la [**interfaz IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) pero no la implementa. Implementa **IDispatch a través** de la [**clase CBaseDispatch**](cbasedispatch.md) y la DirectShow de tipos. No use esta clase directamente. En su lugar, use una de las clases siguientes:

-   Filtros de origen: use la clase base [**CSourceSeeking**](csourceseeking.md) para implementar la búsqueda.
-   Filtros de transformación: use la [**clase CPosPassThru para**](cpospassthru.md) pasar los comandos de búsqueda ascendentes.
-   Representadores: use la [**clase CRendererPosPassThru para**](crendererpospassthru.md) pasar los comandos de búsqueda ascendentes.



| Métodos públicos                                              | Descripción                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CMediaPosition**](cmediaposition-cmediaposition.md)     | Método constructor.                                                                                                 |
| Métodos IDispatch                                           | Descripción                                                                                                         |
| [**GetIDsOfNames**](cmediaposition-getidsofnames.md)       | Mapas un conjunto de nombres a un conjunto correspondiente de DISPID.                                                              |
| [**GetTypeInfo**](cmediaposition-gettypeinfo.md)           | Recupera la información de tipo del objeto , que se puede usar para obtener la información de tipo de una interfaz. |
| [**GetTypeInfoCount**](cmediaposition-gettypeinfocount.md) | Recupera el número de interfaces de información de tipo que proporciona el objeto .                                            |
| [**Invocar**](cmediaposition-invoke.md)                     | Proporciona acceso a las propiedades y los métodos expuestos por el objeto .                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Clases base](directshow-base-classes.md)
</dt> </dl>

 

 




