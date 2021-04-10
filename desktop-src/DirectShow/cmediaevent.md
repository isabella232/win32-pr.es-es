---
description: La clase CMediaEvent proporciona la implementación de la clase base de los métodos IDispatch del IMediaEvent de interfaz dual. Deja como virtual pura las propiedades y los métodos de la interfaz IMediaEvent.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: Clase CMediaEvent
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
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279830"
---
# <a name="cmediaevent-class"></a>Clase CMediaEvent

![jerarquía de clases cmediaevent](images/cutil03.png)

La `CMediaEvent` clase proporciona la implementación de la clase base de los métodos **IDispatch** del [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)de interfaz dual. Deja como virtual pura las propiedades y los métodos de la interfaz **IMediaEvent** .

La `CMediaEvent` clase también proporciona la implementación de la clase base de la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) que se deriva de [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).

Las funciones miembro [**CMediaEvent:: GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent:: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent:: GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)y [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) son implementaciones estándar de la interfaz **IDispatch** mediante la clase [**CBaseDispatch**](cbasedispatch.md) (y una biblioteca de tipos) para analizar los comandos y pasarlos a los métodos virtuales puros de la interfaz [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .



| Funciones de miembro                                         | Descripción                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaEvent**](cmediaevent-cmediaevent.md)           | Construye un objeto **CMediaEvent** .                                                                                                                                                          |
| Métodos IDispatch                                        | Descripción                                                                                                                                                                                   |
| [**GetIDsOfNames**](cmediaevent-getidsofnames.md)       | Asigna un solo miembro y un conjunto opcional de parámetros a un conjunto correspondiente de identificadores de envío enteros, que se puede usar durante las llamadas subsiguientes al método **IDispatch:: Invoke** . |
| [**GetTypeInfo**](cmediaevent-gettypeinfo.md)           | Recupera un objeto de información de tipo, que recupera la información de tipo de una interfaz.                                                                                                   |
| [**GetTypeInfoCount**](cmediaevent-gettypeinfocount.md) | Recupera el número de interfaces de información de tipo proporcionado por un objeto.                                                                                                                    |
| [**Invocar**](cmediaevent-invoke.md)                     | Proporciona acceso a las propiedades y los métodos expuestos por un objeto.                                                                                                                               |



 

 

 



