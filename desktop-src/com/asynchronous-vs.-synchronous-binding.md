---
title: Enlace asincrónico y sincrónico
description: Enlace asincrónico y sincrónico
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb498d083260db087e9f32cd3f24b67f03f9a788c0add2592dde36fe7a7905e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048863"
---
# <a name="asynchronous-and-synchronous-binding"></a>Enlace asincrónico y sincrónico

El cliente puede comprobar si el moniker es asincrónico llamando a la [**función IsAsyncMoniker.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) Si el cliente devuelve la marca BINDF ASYNCHRONOUS, en lugar de devolver un puntero de objeto o un puntero de almacenamiento de llamadas posteriores \_ a [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) o [**IMoniker::BindToObject,**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)el moniker devuelve MK S ASYNCHRONOUS en lugar del puntero de objeto y NULL en lugar del puntero \_ de \_ almacenamiento.  En respuesta, el cliente debe esperar para recibir el objeto o almacenamiento solicitado durante la implementación de [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) e [**IBindStatusCallBack::OnObjectAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85)).

El objeto de devolución de llamada también recibe la notificación de progreso a través de [**IBindStatusCallback::OnProgress,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85))la notificación de disponibilidad de datos a través de [**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))y otras notificaciones del moniker sobre el estado de la operación de enlace.

Si el cliente no devuelve la marca BINDF ASYNCHRONOUS de la llamada del \_ moniker a [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)), la operación de enlace continuará sincrónicamente y el objeto o almacenamiento deseado se devolverá de las llamadas posteriores a [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) [**o BindToStorage.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) Del mismo modo, si el cliente desea una operación sincrónica y no desea recibir ninguna notificación de progreso o devoluciones de llamada, puede solicitar un moniker asincrónico para que se comporte sincrónicamente al no implementar [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)). En tales casos, el moniker asincrónico se comportará como un moniker sincrónico estándar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers asincrónicos](asynchronous-monikers.md)
</dt> </dl>

 

 