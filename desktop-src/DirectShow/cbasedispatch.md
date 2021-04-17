---
description: La clase CBaseDispatch es una clase base para implementar la interfaz IDispatch en un filtro DirectShow.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Clase CBaseDispatch (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660578"
---
# <a name="cbasedispatch-class"></a>Clase CBaseDispatch

![jerarquía de clases cbasedispatch](images/cutil01.png)

La clase **CBaseDispatch** es una clase base para implementar la interfaz **IDispatch** en un filtro DirectShow.

Esta clase se limita a admitir las interfaces compatibles con automatización exportadas por la biblioteca de tipos de DirectShow, QuartzTypeLib. Por ejemplo, las clases [**CMediaControl**](cmediacontrol.md) y [**CMediaPosition**](cmediaposition.md) usan **CBaseDispatch** para implementar [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) y [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectivamente. Debido a esta limitación, probablemente no haya ningún motivo para usar **CBaseDispatch** directamente en sus propios filtros.

Para usar esta clase, haga lo siguiente:

-   Declare una nueva clase que admita **IDispatch**.
-   Asigne a la nueva clase una variable miembro privada de tipo **CBaseDispatch**.
-   Implemente los métodos **IDispatch** .
-   En los métodos **IDispatch** , llame a los métodos **CBaseDispatch** .

Para obtener más información, consulte el código fuente de cualquiera de las clases de ejemplo declaradas en Ctlutil. h.



| Métodos públicos                                             | Descripción                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CBaseDispatch**](cbasedispatch-cbasedispatch.md)       | Método de constructor.                                                                                                 |
| [**~ CBaseDispatch**](cbasedispatch--cbasedispatch.md)     | Método de destructor.                                                                                                  |
| [**GetIDsOfNames**](cbasedispatch-getidsofnames.md)       | Asigna un conjunto de nombres a un conjunto correspondiente de DispId.                                                              |
| [**GetTypeInfo**](cbasedispatch-gettypeinfo.md)           | Recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz. |
| [**GetTypeInfoCount**](cbasedispatch-gettypeinfocount.md) | Recupera el número de interfaces de información de tipo que proporciona el objeto.                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases base de DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




