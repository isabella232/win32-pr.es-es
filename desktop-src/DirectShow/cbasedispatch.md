---
description: La clase CBaseDispatch es una clase base para implementar la interfaz IDispatch en un DirectShow filtro.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: CBaseDispatch (clase, Ctlutil.h)
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
ms.openlocfilehash: 1a094ad3b79dbeb8c4dfc2888de01a521738740fc19ad70b521172d3194fd9f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793325"
---
# <a name="cbasedispatch-class"></a>CBaseDispatch (clase)

![Jerarquía de clases cbasedispatch](images/cutil01.png)

La **clase CBaseDispatch** es una clase base para implementar la **interfaz IDispatch** en un DirectShow filtro.

Esta clase se limita a admitir las interfaces compatibles con Automation exportadas por la biblioteca de tipos DirectShow, EltipoTipoLib. Por ejemplo, las [**clases CMediaControl**](cmediacontrol.md) y [**CMediaPosition**](cmediaposition.md) usan **CBaseDispatch** para implementar [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition)respectivamente. Debido a esta limitación, probablemente no haya ninguna razón para usar **CBaseDispatch** directamente en sus propios filtros.

Para usar esta clase, haga lo siguiente:

-   Declare una nueva clase que admita **IDispatch.**
-   Dé a la nueva clase una variable miembro privada de tipo **CBaseDispatch**.
-   Implemente **los métodos IDispatch.**
-   En los **métodos IDispatch,** llame a **los métodos CBaseDispatch.**

Para obtener más información, consulte el código fuente de cualquiera de las clases de ejemplo declaradas en Ctlutil.h.



| Métodos públicos                                             | Descripción                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CBaseDispatch**](cbasedispatch-cbasedispatch.md)       | Método constructor.                                                                                                 |
| [**~CBaseDispatch**](cbasedispatch--cbasedispatch.md)     | Método destructor.                                                                                                  |
| [**GetIDsOfNames**](cbasedispatch-getidsofnames.md)       | Mapas un conjunto de nombres a un conjunto correspondiente de DISPID.                                                              |
| [**GetTypeInfo**](cbasedispatch-gettypeinfo.md)           | Recupera la información de tipo del objeto , que luego se puede usar para obtener la información de tipo de una interfaz. |
| [**GetTypeInfoCount**](cbasedispatch-gettypeinfocount.md) | Recupera el número de interfaces de información de tipo que proporciona el objeto .                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Clases base](directshow-base-classes.md)
</dt> </dl>

 

 




