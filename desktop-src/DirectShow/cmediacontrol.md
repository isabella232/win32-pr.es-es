---
description: La clase CMediaControl proporciona control de clases base de los métodos IDispatch de la interfaz dual IMediaControl. Deja como virtuales puras las propiedades y los métodos de la interfaz IMediaControl.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: CMediaControl (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: 119ffb93cb307db1da3bc8c7562851d63c5f9eeb8e0e3b80be62c8110181c32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074088"
---
# <a name="cmediacontrol-class"></a>CMediaControl (clase)

![Jerarquía de clases cmediacontrol](images/cutil02.png)

La `CMediaControl` clase proporciona control de clases base de los [**métodos IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) de la interfaz dual [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol). Deja como virtuales puras las propiedades y los métodos de la **interfaz IMediaControl.**

Normalmente, el administrador de gráficos de filtros es el único objeto que implementa la [**interfaz IMediaControl.**](/windows/desktop/api/Control/nn-control-imediacontrol) (los filtros implementan [**la interfaz IMediaFilter,**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) heredada por [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), para recibir comandos de control del administrador de gráficos de filtros). Por lo tanto, esta biblioteca de clases tiene un uso limitado para filtrar a los desarrolladores.

Las funciones miembro [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl::GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)y [**CMediaControl::Invoke**](cmediacontrol-invoke.md) son implementaciones estándar de los métodos [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) mediante la clase [**CBaseDispatch**](cbasedispatch.md) (y una biblioteca de tipos) para analizar los comandos y pasarlos a los métodos virtuales puros de la interfaz [**IMediaControl.**](/windows/desktop/api/Control/nn-control-imediacontrol)

Los [**métodos IMediaControl,**](/windows/desktop/api/Control/nn-control-imediacontrol) definidos en control.odl, se quedan como virtuales puros.



| Funciones de miembro                                           | Descripción                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaControl**](cmediacontrol-cmediacontrol.md)       | Construye un **objeto CMediaControl.**                                                                                                                                                                                                  |
| Métodos IDispatch                                          | Descripción                                                                                                                                                                                                                             |
| [**GetIDsOfNames**](cmediacontrol-getidsofnames.md)       | Mapas un único miembro y un conjunto opcional de parámetros en un conjunto correspondiente de identificadores de distribución de enteros (DISPID), que se pueden usar durante las llamadas posteriores al método [**CMediaControl::Invoke.**](cmediacontrol-invoke.md) |
| [**GetTypeInfo**](cmediacontrol-gettypeinfo.md)           | Recupera un objeto de información de tipo, que puede recuperar la información de tipo de una interfaz.                                                                                                                                          |
| [**GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md) | Recupera el número de interfaces de información de tipos proporcionadas por un objeto .                                                                                                                                                              |
| [**Invocar**](cmediacontrol-invoke.md)                     | Proporciona acceso a las propiedades y los métodos expuestos por un objeto.                                                                                                                                                                         |



 

 

 
