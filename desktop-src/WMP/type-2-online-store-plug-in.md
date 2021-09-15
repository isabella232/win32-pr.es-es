---
title: Complemento de la tienda en línea de tipo 2
description: Complemento de la tienda en línea de tipo 2
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Reproductor de Windows Media en línea, complementos
- tiendas en línea, complementos
- tiendas en línea de tipo 2, complementos
- Reproductor de Windows Media en línea, interfaz IWMPSubscriptionService
- tiendas en línea, interfaz IWMPSubscriptionService
- tipo 2 tiendas en línea, interfaz IWMPSubscriptionService
- complementos, Reproductor de Windows Media tiendas en línea
- complementos, tiendas en línea
- complementos, escriba 2 tiendas en línea
- complementos, interfaz IWMPSubscriptionService
- Reproductor de Windows Media complementos, escriba 2 tiendas en línea
- Reproductor de Windows Media complementos,tiendas en línea
- Reproductor de Windows Media complementos, Reproductor de Windows Media tiendas en línea
- Reproductor de Windows Media complementos, interfaz IWMPSubscriptionService
- IWMPSubscriptionService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d2f3aeeaa7456c3452b498a1a728e24c96783c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465817"
---
# <a name="type-2-online-store-plug-in"></a>Complemento de la tienda en línea de tipo 2

Un complemento de tienda en línea de tipo 2 es un componente COM que implementa la interfaz [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) y, opcionalmente, la [interfaz IWMPSubscriptionService2.](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) Reproductor de Windows Media 9 llama a los métodos de la **interfaz IWMPSubscriptionService.** Reproductor de Windows Media 10 o posterior llama a los métodos de las interfaces **IWMPSubscriptionService** e **IWMPSubscriptionService2.**

Un complemento de tienda en línea de tipo 2 se empaqueta como un servidor COM en proceso. Es decir, el complemento se implementa en un archivo .dll que se asigna al proceso Reproductor de Windows Media aplicación.

Reproductor de Windows Media activa complementos de tienda en línea de tipo 2 según sea necesario. Por ejemplo, suponga que el usuario intenta reproducir una canción protegida y no hay ninguna licencia actual para reproducirla. En ese caso, Reproductor de Windows Media el atributo **ContentDistributor** en el encabezado de archivo o en el encabezado DRM. Si existe un valor que coincide con el nombre de clave de una tienda en línea, Reproductor de Windows Media comprueba el registro para ver si esa tienda en línea ha proporcionado un complemento de tipo 2. Si el complemento existe, Reproductor de Windows Media carga el complemento y llama a sus métodos para determinar si el usuario tiene los derechos para reproducir la canción.

En la lista siguiente se describen algunos de los escenarios en los que Reproductor de Windows Media llama a un complemento de tienda en línea de tipo 2.

-   **El usuario intenta reproducir contenido de la tienda en línea.** Cuando esto sucede, Reproductor de Windows Media llama al método [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) del complemento, pasando un puntero al elemento multimedia digital que el usuario está intentando reproducir. La tienda en línea puede usarla como una oportunidad para actualizar la licencia del usuario para reproducir el contenido o para no permitir la reproducción. Si el complemento devuelve **TRUE en** el *parámetro pfAllowPlay,* Reproductor de Windows Media intenta reproducir el contenido. La reproducción seguirá sin producirse si no existe una licencia válida. este proceso no evita la administración de derechos digitales (DRM).
-   **El usuario solicita permiso para grabar contenido en un CD o DVD.** Cuando esto sucede, Reproductor de Windows Media llama al método [IWMPSubscriptionService::allowCDAsync del](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn) complemento.
-   **El usuario intenta sincronizar el contenido de la tienda en línea con un dispositivo o Reproductor de Windows Media está listo para sincronizar automáticamente el contenido de la tienda en línea con un dispositivo.** Cuando esto sucede, Reproductor de Windows Media llama al método [IWMPSubscriptionService2::p repareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync) del complemento para alertar al almacén en línea de que un elemento multimedia está a punto de sincronizarse con un dispositivo determinado, que se identifica por su nombre canónico. Esta es una oportunidad para que la tienda en línea determine si el usuario puede sincronizar el elemento multimedia con el dispositivo. También es una oportunidad para que la tienda en línea prepare el dispositivo para la sincronización y actualice los registros, como los recuentos de sincronización, asociados al dispositivo o al elemento multimedia. El complemento debe pasar las tareas de permiso, preparación y mantenimiento de registros a un subproceso independiente y volver inmediatamente de **prepareForSync.** Cuando el subproceso independiente haya finalizado su trabajo, debe notificar a Reproductor de Windows Media mediante una llamada a [IWMPSubscriptionServiceCallback::onComplete](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete).
-   **Un dispositivo está disponible para el procesamiento en segundo plano.** Cuando un dispositivo está conectado, Reproductor de Windows Media alerta al almacén en línea de que el dispositivo está disponible e inactivo mediante una llamada a [IWMPSubscriptionService2::d eviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).
-   **El usuario hace clic en un botón para activar una tienda en línea en Reproductor de Windows Media.** Cuando esto sucede, Reproductor de Windows Media llama al método [IWMPSubscriptionService2::serviceEvent del](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent) complemento. Reproductor de Windows Media llama a este método cuando el usuario cambia a otro servicio.
-   **Reproductor de Windows Media entra en un estado de baja actividad.** Cuando esto sucede, el reproductor llama al método [IWMPSubscriptionService::startBackgroundProcessing del](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) complemento. La tienda en línea puede usar esta oportunidad para iniciar o reactivar los subprocesos que realizan tareas en segundo plano, como renovar licencias expiradas o compilar datos de recuento de reproducción.
-   **Reproductor de Windows Media entra en un estado de alta actividad.** Cuando esto sucede, Reproductor de Windows Media llama al método [IWMPSubscriptionService2::stopBackgroundProcessing del](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing) complemento. Esto informa al complemento de que debe suspender los subprocesos que realizan tareas en segundo plano.

Reproductor de Windows Media el componente de la tienda en línea cuando finaliza la sesión del reproductor. Tras la versión, el componente debe interrumpir cualquier procesamiento en segundo plano en curso y, a continuación, apagar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMPSubscriptionService (interfaz)**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**IWMPSubscriptionService2 (Interfaz)**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> <dt>

[**IWMPSubscriptionServiceCallback (Interfaz)**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)
</dt> <dt>

[**Ejemplos de tienda en línea de tipo 2**](type-2-online-store-samples.md)
</dt> </dl>

 

 




