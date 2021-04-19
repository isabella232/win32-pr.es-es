---
description: Un proveedor de eventos puede dedicar mucho tiempo a la creación de eventos.
ms.assetid: 5cf414f0-b3a8-4623-9aaa-08e2a28b40c0
ms.tgt_platform: multiple
title: Optimizar un proveedor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70eaabfbbd462b831059b10590d7959bdef05cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707210"
---
# <a name="optimizing-an-event-provider"></a>Optimizar un proveedor de eventos

Un proveedor de eventos puede dedicar mucho tiempo a la creación de eventos. Si ninguna aplicación cliente usa los eventos creados, el proveedor desperdicia recursos del sistema. Además, WMI dedica una cantidad considerable de recursos al análisis y el envío de consultas complejas al proveedor adecuado. Para evitar la pérdida de recursos del sistema y mejorar el rendimiento del proveedor de eventos, puede implementar la interfaz [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) . **IWbemEventProviderQuerySink** supervisa las consultas que las aplicaciones cliente registran con WMI mediante los métodos [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) y [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) . Mediante la supervisión de las consultas de cliente registradas, el proveedor puede determinar qué sucede si se deben enviar mensajes a WMI.

WMI llama a [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) en un proveedor de eventos cuando un consumidor de cliente registra una consulta de filtro de eventos que contiene referencias a eventos admitidos por ese proveedor de eventos. Por lo tanto, el proveedor de eventos responsable de los eventos de modificación de instancias de la clase **EmailClass** puede configurarse para generar notificaciones solo para el **remitente**. Cuando el proveedor recibe una consulta que solicita la notificación de los cambios en la propiedad de **asunto** , el proveedor puede empezar a generar esas notificaciones. En este escenario, no se requiere WMI para descartar las notificaciones que solo notifican los cambios de **destinatarios** .

Del mismo modo, WMI llama a [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) en un proveedor de eventos cuando un consumidor del cliente anula el registro de una consulta de filtro de eventos que contiene referencias a eventos admitidos por el proveedor de eventos. El propósito de **CancelQuery** es que el proveedor de eventos actualice la lista de los eventos que se deben enviar.

> [!Note]  
> Si el proveedor es compatible con [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) y [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink), asegúrese de que la implementación del método **IUnknown:: QueryInterface** devuelve punteros a ambas interfaces.

 

 

 



