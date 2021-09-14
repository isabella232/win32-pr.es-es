---
description: La clase CMediaEvent proporciona la implementación de clase base de los métodos IDispatch de la interfaz dual IMediaEvent. Deja como virtuales puras las propiedades y los métodos de la interfaz IMediaEvent.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: CMediaEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062467"
---
# <a name="cmediaevent-class"></a>CMediaEvent (clase)

![Jerarquía de clases cmediaevent](images/cutil03.png)

La `CMediaEvent` clase proporciona la implementación de clase base de los **métodos IDispatch** de la interfaz dual [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent). Deja como virtuales puras las propiedades y los métodos de la **interfaz IMediaEvent.**

La `CMediaEvent` clase también proporciona la implementación de clase base de la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) que se deriva de [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).

Las funciones miembro [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent::GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)y [**CMediaEvent::Invoke**](cmediaevent-invoke.md) son implementaciones estándar de la interfaz **IDispatch** mediante la clase [**CBaseDispatch**](cbasedispatch.md) (y una biblioteca de tipos) para analizar los comandos y pasarlos a los métodos virtuales puros de la interfaz [**IMediaEvent.**](/windows/desktop/api/Control/nn-control-imediaevent)



| Funciones de miembro                                         | Descripción                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaEvent**](cmediaevent-cmediaevent.md)           | Construye un **objeto CMediaEvent.**                                                                                                                                                          |
| Métodos IDispatch                                        | Descripción                                                                                                                                                                                   |
| [**GetIDsOfNames**](cmediaevent-getidsofnames.md)       | Mapas un único miembro y un conjunto opcional de parámetros en un conjunto correspondiente de identificadores de distribución de enteros, que se pueden usar durante las llamadas posteriores al **método IDispatch::Invoke.** |
| [**GetTypeInfo**](cmediaevent-gettypeinfo.md)           | Recupera un objeto de información de tipos, que recupera la información de tipo de una interfaz.                                                                                                   |
| [**GetTypeInfoCount**](cmediaevent-gettypeinfocount.md) | Recupera el número de interfaces de información de tipos proporcionadas por un objeto .                                                                                                                    |
| [**Invocar**](cmediaevent-invoke.md)                     | Proporciona acceso a las propiedades y los métodos expuestos por un objeto.                                                                                                                               |



 

 

 



