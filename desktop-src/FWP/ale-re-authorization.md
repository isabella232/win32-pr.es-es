---
title: Reautorización de ALE
description: El tráfico de red en las capas de cumplimiento de capa de aplicación (ALE) de la plataforma de filtrado de Windows (WFP) se filtra mediante flujos de ALE.
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05c4c0767d449ec128250f852c365455bd0dc7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791409"
---
# <a name="ale-reauthorization"></a>Reautorización de ALE

El tráfico de red en las capas de cumplimiento de capa de aplicación (ALE) de la plataforma de filtrado de Windows (WFP) se filtra mediante [flujos de Ale](ale-stateful-filtering.md). Una vez que se ha permitido un flujo ALE, se permite todo el tráfico que forma parte del flujo de ALE. La reautorización es una solicitud para validar los permisos del flujo ALE, normalmente debido a un cambio en la Directiva de red.

A los flujos ALE se les asigna una dirección, entrante o saliente, en función de la dirección del primer paquete que desencadenó la creación y autorización del flujo. Los flujos de ALE de entrada se crean y autorizan en el nivel de aceptación de recepción de FWPM de Ale de la capa de la [**\_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) . Los flujos de ALE de salida se crean y autorizan en la capa de FWPM de la **\_ autenticación Ale de capa de \_ \_ \_ conexión \_ V {4 \| 6}** . La dirección del flujo de ALE no limita la dirección de los paquetes que pertenecen al flujo. Los flujos ALE contienen paquetes entrantes y salientes, independientemente de la dirección del flujo de ALE.

La reautorización de un flujo ALE se desencadena mediante:

-   Cambio de directiva en la capa en la que se autorizó o creó originalmente el flujo ALE.
-   Una interfaz de llegada diferente de la interfaz en la que se autorizó o creó originalmente el flujo ALE.
-   Una conexión pendiente.

La reautorización se diferencia de la autorización inicial por la presencia de la marca de condición de FWP en la marca de [**\_ \_ \_ \_ reautorización**](filtering-condition-flags-.md) .

La reautorización solo puede llevarse a cabo en las capas de FWPM de recepción de autenticación Ale de la versión de [**\_ \_ \_ \_ \_ aceptación \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) y de **FWPM de \_ \_ \_ autenticación Ale \_ \_ v {4 \| 6}** .

### <a name="policy-change-reauthorization"></a>Directiva: cambiar la reautorización

Un cambio de Directiva se implementa como una adición o eliminación de filtro en una capa ALE. Una vez que se detecta un cambio en la Directiva, se especifica el primer paquete que atraviesa un flujo ALE creado en la capa afectada para la reautorización de la capa. Por lo tanto, para volver a autorizar, es posible que un paquete de salida se clasifique en la capa de FWPM de recepción Ale de aceptación de la recepción de la capa [**\_ \_ \_ \_ \_ \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) y que un paquete de entrada se clasifique en la capa **FWPM de \_ \_ \_ autenticación Ale \_ \_ v {4 \| 6}** de la capa de.

Una razón para esta clasificación de dirección mixta es que puede que no haya más tráfico de red de la dirección original (por ejemplo, un paquete de entrada para el flujo de ALE de entrada). Un ejemplo de este tipo es la transmisión por secuencias de UDP unidireccional después de un protocolo de enlace bidireccional inicial. En este caso, es más conveniente destruir el streaming lo antes posible.

### <a name="arrival-interface-reauthorization"></a>Reautorización de la interfaz de llegada

La reautorización de la interfaz de llegada está disponible a partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

Los paquetes que pertenecen al mismo flujo de ALE pueden llegar desde varias interfaces. Se vuelve a autorizar el primer paquete que se encuentra en una interfaz diferente de la interfaz original del flujo de ALE.

En un modelo de host seguro, que es el modelo de seguridad predeterminado para la pila TCP/IP, una conexión en una interfaz de red solo acepta los paquetes que se encuentran en la misma interfaz. Por lo tanto, la reautorización de la interfaz de llegada no se utiliza en un equipo host seguro.

En un modelo de host no seguro, una conexión en una interfaz de red permite que los paquetes lleguen a cualquier otra interfaz de red. La reautorización de la interfaz de llegada se usa en un equipo host no seguro para implementar directivas específicas de la interfaz. Para obtener más información, vea ["The cable Guy: strong and Weak host models".](/previous-versions/technet-magazine/cc137807(v=msdn.10))

Algunos [campos clasificables](filtering-conditions.md) pueden ser desconocidos durante la reautorización. Por ejemplo, si se está reautorizando un paquete de salida en el nivel de FWPM de recepción de autenticación Ale de la capa de la aceptación de la recepción de la versión [**\_ \_ \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , se desconocerán todos los campos relacionados con la interfaz de llegada. En ese caso, los valores de los campos desconocidos se indican como [**FWP \_ vacío**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).

Los campos de tipo [**FWP \_ Empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) pueden coincidir con el valor de la [**\_ coincidencia \_ de FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type). Por lo tanto, se puede establecer una directiva para bloquear las reautorizaciones y anular un flujo ALE cuando lleguen las solicitudes de reautorización del flujo ALE.

## <a name="pending-connection-reauthorization"></a>Reautorización de conexión pendiente

Un controlador de llamada puede posponer una operación de clasificación en niveles ALE y completarla más adelante, cuando se pueda realizar la decisión de filtrado de forma segura. La funcionalidad de posponer/completar de ALE se admite a través de las funciones de modo kernel [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) y [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0).

La reautorización se desencadena inmediatamente después de la llamada a FwpsCompleteOperation0 y permite que el controlador de llamada permita o bloquee el flujo.

Solo se puede posponer una autorización inicial. Una llamada a FwpsPendOperation0 producirá un error si se establece la [**\_ marca de condición de \_ \_ \_ FWP**](filtering-condition-flags-.md) .

Para obtener más información, consulte la documentación del [Kit de controladores de Windows](/windows-hardware/drivers/ddi/_netvista/) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación del nivel de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Niveles ALE](ale-layers.md)
</dt> <dt>

[Filtrado con estado ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfico de multidifusión/difusión ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Personalización del flujo ALE](ale-flow-customization.md)
</dt> </dl>

 

 