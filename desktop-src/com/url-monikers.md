---
title: URL Monikers
description: La arquitectura de moniker OLE proporciona un modelo de programación práctico para trabajar con direcciones URL.
ms.assetid: 8e0e2bad-9275-4b96-a96b-35d9c933ae31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2a63f63d14dfe51c0b8c5c3727637e12a51356
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358926"
---
# <a name="url-monikers"></a>URL Monikers

La arquitectura de moniker OLE proporciona un modelo de programación práctico para trabajar con direcciones URL. La arquitectura del moniker admite el análisis extensible y completo de nombres a través de la función [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) y las interfaces [**IParseDisplayName**](/windows/desktop/api/OleIdl/nn-oleidl-iparsedisplayname) e [**IMoniker,**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) así como nombres imprimibles a través del método [**IMoniker::GetDisplayName.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) La **interfaz IMoniker** es la manera en que realmente se usan las direcciones URL que encuentra y la creación de componentes que se ajustan a la arquitectura del moniker es la manera de ampliar realmente los espacios de nombres de dirección URL en la práctica.

Una clase de moniker proporcionada por el sistema, el moniker de dirección URL, proporciona un marco para compilar y usar determinadas direcciones URL. Dado que las direcciones URL suelen ver recursos en redes de alta latencia, el moniker de dirección URL admite el enlace asincrónico y sincrónico. El moniker de dirección URL no admite actualmente [el almacenamiento asincrónico](/windows/desktop/Stg/asynchronous-storage).

En el diagrama siguiente se muestran los componentes implicados en el uso de monikers de dirección URL. Todos estos componentes deben estar familiarizados. (Vea [Monikers asincrónicos).](asynchronous-monikers.md)

![Diagrama que muestra los componentes implicados en el uso de monikers de U R L.](images/bb10975a-9cb5-418e-872e-1e1add0b58ed.png)

Al igual que todos los clientes de moniker, un usuario de Monikers de url normalmente crea y contiene una referencia al moniker, así como al contexto de enlace que se va a usar durante el enlace ([**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) o [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)). Para admitir el enlace asincrónico, el cliente puede implementar un objeto bind-status-callback, que implementa la interfaz [**IBindStatusCallback,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) y registrarlo con el contexto de enlace mediante la [**función RegisterBindStatusCallback.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) Este objeto recibirá la interfaz [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) del transporte durante las llamadas a [**IBindStatusCallback::OnStartBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)).

El Moniker de dirección URL identifica el protocolo que se usa analizando el prefijo de dirección URL y, a continuación, recupera la [**interfaz IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) de la capa de transporte. El cliente usa **IBinding para** admitir la pausa, cancelación y priorización de la operación de enlace. El objeto de devolución de llamada también recibe la notificación de progreso a través de [**IBindStatusCallback::OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), la notificación de disponibilidad de datos a través de [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))y otras notificaciones de la capa de transporte sobre el estado del enlace. El moniker de dirección URL o las capas de transporte específicas también pueden solicitar información extendida del cliente a través de **IBindStatusCallback::QueryInterface**, lo que permite al cliente proporcionar información específica del protocolo que afectará a la operación de enlace.

Para obtener más información, vea los temas siguientes:

-   [Sincronización de devolución de llamada](callback-synchronization.md)
-   [Negociación de tipo multimedia](media-type-negotiation.md)
-   [Funciones de Moniker de dirección URL](url-moniker-api-functions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers asincrónicos](asynchronous-monikers.md)
</dt> <dt>

[Acerca de los monikers de url](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775149(v=vs.85))
</dt> </dl>

 

 