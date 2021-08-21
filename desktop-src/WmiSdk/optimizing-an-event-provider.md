---
description: Un proveedor de eventos puede dedicar una gran cantidad de tiempo a crear eventos.
ms.assetid: 5cf414f0-b3a8-4623-9aaa-08e2a28b40c0
ms.tgt_platform: multiple
title: Optimización de un proveedor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613fa6b054f979d0f7d1a33a87f927df9ef129a280cf7cd1675cbe0cf9818473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923412"
---
# <a name="optimizing-an-event-provider"></a>Optimización de un proveedor de eventos

Un proveedor de eventos puede dedicar una gran cantidad de tiempo a crear eventos. Si ninguna aplicación cliente usa los eventos creados, el proveedor está desa partir de los recursos del sistema. Además, WMI dedica una cantidad considerable de recursos a analizar y enviar consultas complejas al proveedor adecuado. Para evitar la pérdida de recursos del sistema y mejorar el rendimiento del proveedor de eventos, puede implementar la [**interfaz IWbemEventProviderQuerySink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) **IWbemEventProviderQuerySink** supervisa las consultas que las aplicaciones cliente registran con WMI mediante los [**métodos NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) [**y CancelQuery.**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) Mediante la supervisión de las consultas de cliente registradas, el proveedor puede determinar qué ocurre si se deben enviar mensajes a WMI.

WMI llama [**a NewQuery en**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) un proveedor de eventos cuando un consumidor cliente registra una consulta de filtro de eventos que contiene referencias a eventos admitidos por ese proveedor de eventos. Por lo tanto, el proveedor de eventos responsable de los eventos de modificación de instancias de la **clase EmailClass** se puede configurar para generar notificaciones solo para el **remitente.** Cuando el proveedor recibe una consulta que solicita la notificación de cambios en la propiedad **de** asunto, el proveedor puede empezar a generar esas notificaciones. En este escenario, WMI no es necesario para descartar las notificaciones que solo informan **de los cambios del** destinatario.

De forma similar, WMI llama a [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) en un proveedor de eventos cuando un consumidor cliente anula el registro de una consulta de filtro de eventos que contiene referencias a eventos admitidos por el proveedor de eventos. El propósito de **CancelQuery** es que el proveedor de eventos actualice la lista de los eventos que se deben enviar.

> [!Note]  
> Si el proveedor admite [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) e [**IWbemEventProviderQuerySink,**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)asegúrese de que la implementación del método **IUnknown::QueryInterface** devuelve punteros a ambas interfaces.

 

 

 



