---
title: Enlace asincrónico y sincrónico
description: Enlace asincrónico y sincrónico
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b022df239221f0a019b972067248225210e585
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794038"
---
# <a name="asynchronous-and-synchronous-binding"></a>Enlace asincrónico y sincrónico

El cliente puede comprobar si el moniker es asincrónico mediante una llamada a la función [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) . Si el cliente devuelve la \_ marca ASINCRÓNICA BINDF, en lugar de devolver un puntero de objeto o un puntero de almacenamiento de las llamadas subsiguientes a [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) o [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject), el moniker devuelve MK \_ S \_ Asynchronous en lugar del puntero de objeto y **null** en lugar del puntero de almacenamiento. En respuesta, el cliente debe esperar para recibir el objeto o almacenamiento solicitado durante la implementación de [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) y [**IBindStatusCallback:: OnObjectAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85)).

El objeto de devolución de llamada también recibe notificaciones de progreso a través de [**IBindStatusCallback:: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), notificación de disponibilidad de datos a través de [**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))y otras notificaciones del moniker sobre el estado de la operación de enlace.

Si el cliente no devuelve la \_ marca ASINCRÓNICA BINDF de la llamada del moniker a [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)), la operación de enlace se realizará de forma sincrónica y se devolverá el objeto o almacenamiento deseado de las llamadas subsiguientes a [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) o [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage). Del mismo modo, si el cliente desea una operación sincrónica y no quiere recibir notificaciones de progreso o devoluciones de llamada, puede solicitar que un moniker asincrónico se comporte de forma sincrónica si no implementa [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)). En tales casos, el moniker asincrónico se comportará como un moniker sincrónico estándar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers asincrónicos](asynchronous-monikers.md)
</dt> </dl>

 

 