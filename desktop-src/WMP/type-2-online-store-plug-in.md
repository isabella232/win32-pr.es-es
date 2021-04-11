---
title: Complemento de la tienda en línea de tipo 2
description: Complemento de la tienda en línea de tipo 2
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Windows Media Player tiendas en línea, Complementos
- tiendas en línea, Complementos
- tipo 2 tiendas en línea, Complementos
- Windows Media Player tiendas en línea, interfaz IWMPSubscriptionService
- tiendas en línea, interfaz IWMPSubscriptionService
- tipo 2 tiendas en línea, interfaz IWMPSubscriptionService
- complementos, Windows Media Player tiendas en línea
- complementos, tiendas en línea
- complementos, tipo 2 tiendas en línea
- complementos, interfaz IWMPSubscriptionService
- Complementos de Windows Media Player, escriba 2 tiendas en línea
- Complementos de Windows Media Player, tiendas en línea
- Complementos de Windows Media Player, Windows Media Player tiendas en línea
- Complementos de Media Player de Windows, interfaz IWMPSubscriptionService
- IWMPSubscriptionService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d2f3aeeaa7456c3452b498a1a728e24c96783c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149131"
---
# <a name="type-2-online-store-plug-in"></a>Complemento de la tienda en línea de tipo 2

Un complemento de la tienda en línea de tipo 2 es un componente COM que implementa la interfaz [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) y, opcionalmente, la interfaz [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) . Windows Media Player 9 llama a los métodos de la interfaz **IWMPSubscriptionService** . Windows Media Player 10 o posterior llama a los métodos de las interfaces **IWMPSubscriptionService** y **IWMPSubscriptionService2** .

Un complemento de la tienda en línea de tipo 2 se empaqueta como un servidor COM en proceso. Es decir, el complemento se implementa en un archivo. dll que se asigna al proceso de Media Player de Windows.

Windows Media Player activa los complementos de la tienda en línea de tipo 2 según sea necesario. Por ejemplo, supongamos que el usuario intenta reproducir una canción protegida y no hay ninguna licencia actual para reproducirla. En ese caso, Windows Media Player inspecciona el atributo **ContentDistributor** en el encabezado de archivo o en el encabezado de DRM. Si existe un valor que coincide con el nombre de clave de una tienda en línea, Windows Media Player comprueba el registro para ver si la tienda en línea ha proporcionado un complemento de tipo 2. Si el complemento existe, Windows Media Player carga el complemento y llama a sus métodos para determinar si el usuario tiene derechos para reproducir la canción.

En la lista siguiente se describen algunos de los escenarios en los que Windows Media Player llama a un complemento de almacén en línea de tipo 2.

-   **El usuario intenta reproducir el contenido de la tienda en línea.** Cuando esto sucede, Windows Media Player llama al método [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) del complemento, pasando un puntero al elemento multimedia digital que el usuario está intentando reproducir. La tienda en línea puede utilizarla como una oportunidad para actualizar la licencia del usuario para reproducir el contenido o para no permitir la reproducción. Si el complemento devuelve **true** en el parámetro *pfAllowPlay* , Windows Media Player intenta reproducir el contenido. Se producirá un error en la reproducción si no existe una licencia válida; Este proceso no elude la administración de derechos digitales (DRM).
-   **El usuario solicita permiso para grabar contenido en un CD o DVD.** Cuando esto sucede, Windows Media Player llama al método [IWMPSubscriptionService:: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn) del complemento.
-   **El usuario intenta sincronizar el contenido de la tienda en línea con un dispositivo o Windows Media Player está listo para sincronizar automáticamente el contenido de la tienda en línea con un dispositivo.** Cuando esto sucede, Windows Media Player llama al método [IWMPSubscriptionService2::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync) del complemento para avisar a la tienda en línea de que un elemento multimedia está a punto de sincronizarse con un dispositivo determinado, identificado por su nombre canónico. Esta es una oportunidad para que la tienda en línea determine si el usuario puede sincronizar el elemento multimedia con el dispositivo. También es una oportunidad para que la tienda en línea Prepare el dispositivo para la sincronización y para actualizar registros, como los recuentos de sincronización, asociados con el dispositivo o el elemento multimedia. El complemento debe pasar las tareas de permiso, preparación y conservación de registros a un subproceso independiente y volver inmediatamente desde **prepareForSync**. Cuando el subproceso independiente ha finalizado su trabajo, debe notificar a Windows Media Player llamando a [IWMPSubscriptionServiceCallback:: alcomplete](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete).
-   **Un dispositivo está disponible para el procesamiento en segundo plano.** Cuando se conecta un dispositivo, Windows Media Player alerta a la tienda en línea de que el dispositivo está disponible y está inactivo mediante una llamada a [IWMPSubscriptionService2::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).
-   **El usuario hace clic en un botón para activar una tienda en línea en Windows Media Player.** Cuando esto ocurre, Windows Media Player llama al método [IWMPSubscriptionService2:: serviceEvent](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent) del complemento. Windows Media Player también llama a este método cuando el usuario cambia a otro servicio.
-   **Windows Media Player entra en un estado de baja actividad.** Cuando esto sucede, el reproductor llama al método [IWMPSubscriptionService:: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) del complemento. La tienda en línea puede utilizar esta oportunidad para iniciar o reactivar los subprocesos que realizan tareas en segundo plano, como renovar licencias expiradas o compilar datos de recuento de la reproducción.
-   **Windows Media Player entra en un estado de alta actividad.** Cuando esto sucede, Windows Media Player llama al método [IWMPSubscriptionService2:: stopBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing) del complemento. Esto informa al complemento de que debe suspender los subprocesos que realizan tareas en segundo plano.

Windows Media Player libera el componente de la tienda en línea cuando finaliza la sesión del reproductor. En el momento de la versión, el componente debe interrumpir cualquier procesamiento en segundo plano en curso y, a continuación, cerrar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMPSubscriptionService**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interfaz IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> <dt>

[**Interfaz IWMPSubscriptionServiceCallback**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)
</dt> <dt>

[**Ejemplos de la tienda en línea de tipo 2**](type-2-online-store-samples.md)
</dt> </dl>

 

 




