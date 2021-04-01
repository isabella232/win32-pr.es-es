---
description: La clase CMediaControl proporciona el control de clases base de los métodos IDispatch de la interfaz dual IMediaControl. Deja como virtual pura las propiedades y los métodos de la interfaz IMediaControl.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: Clase CMediaControl
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
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914213"
---
# <a name="cmediacontrol-class"></a>Clase CMediaControl

![jerarquía de clases cmediacontrol](images/cutil02.png)

La `CMediaControl` clase proporciona el control de clases base de los métodos [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) de la interfaz dual [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol). Deja como virtual pura las propiedades y los métodos de la interfaz **IMediaControl** .

Normalmente, el administrador de gráficos de filtros es el único objeto que implementa la interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) . (los filtros implementan la interfaz [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) , heredada por [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), para recibir comandos de control del administrador de gráficos de filtros). Por lo tanto, esta biblioteca de clases es de uso limitado para filtrar a los desarrolladores.

Las funciones miembro [**CMediaControl:: GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl:: GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl:: GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)y [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) son implementaciones estándar de los métodos [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) mediante la clase [**CBaseDispatch**](cbasedispatch.md) (y una biblioteca de tipos) para analizar los comandos y pasarlos a los métodos virtuales puros de la interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .

Los métodos [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) , definidos en control. ODL, se dejan como virtuales puros.



| Funciones de miembro                                           | Descripción                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaControl**](cmediacontrol-cmediacontrol.md)       | Construye un objeto **CMediaControl** .                                                                                                                                                                                                  |
| Métodos IDispatch                                          | Descripción                                                                                                                                                                                                                             |
| [**GetIDsOfNames**](cmediacontrol-getidsofnames.md)       | Asigna un solo miembro y un conjunto opcional de parámetros a un conjunto correspondiente de identificadores de envío enteros (DISPID), que se puede usar en las llamadas subsiguientes al método [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) . |
| [**GetTypeInfo**](cmediacontrol-gettypeinfo.md)           | Recupera un objeto de información de tipo, que puede recuperar la información de tipo de una interfaz.                                                                                                                                          |
| [**GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md) | Recupera el número de interfaces de información de tipo proporcionado por un objeto.                                                                                                                                                              |
| [**Invocar**](cmediacontrol-invoke.md)                     | Proporciona acceso a las propiedades y los métodos expuestos por un objeto.                                                                                                                                                                         |



 

 

 
