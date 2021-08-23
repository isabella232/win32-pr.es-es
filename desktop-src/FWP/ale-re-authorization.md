---
title: Reautorización de ALE
description: Los flujos de ALE filtran el tráfico de red en las capas de aplicación de cumplimiento de la capa de aplicación (ALE) de Windows Filtering Platform (WFP).
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850cd7f789c1fb1222a0d6820e84a42cf41763dac4e57b96667e7feda364374c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582695"
---
# <a name="ale-reauthorization"></a>Reautorización de ALE

Los flujos de [ALE](ale-stateful-filtering.md)filtran el tráfico de red en las capas de cumplimiento de la capa de aplicación (ALE) de Windows Filtering Platform (WFP). Una vez que se ha permitido un flujo de ALE, se permite todo el tráfico que forma parte del flujo de ALE. La reautorización es una solicitud para validar los permisos del flujo de ALE, normalmente debido a un cambio en la directiva de red.

A los flujos de ALE se les asigna una dirección, entrante o saliente, en función de la dirección del primer paquete que desencadenó la creación y autorización del flujo. Los flujos de ALE entrantes se crean y autorizan en la capa [**FWPM \_ LAYER \_ ALE \_ \_ AUTH RECV \_ ACCEPT \_ V{4 \| 6}.**](management-filtering-layer-identifiers-.md) Los flujos de ALE salientes se crean y autorizan en la capa **FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}.** La dirección del flujo ALE no limita la dirección de los paquetes que pertenecen al flujo. Los flujos de ALE contienen paquetes entrantes y salientes, independientemente de la dirección del propio flujo de ALE.

La reautorización de un flujo de ALE se desencadena mediante:

-   Un cambio de directiva en la capa donde se autorizó o creó originalmente el flujo de ALE.
-   Interfaz de llegada diferente de la interfaz en la que se autorizó o creó originalmente el flujo de ALE.
-   Una conexión pendiente.

La reautorización se distingue de la autorización inicial por la presencia de la marca [**FWP \_ CONDITION FLAG IS \_ \_ \_ REAUTHORIZE.**](filtering-condition-flags-.md)

La reautorización solo puede realizarse en las capas [**FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) y **FWPM LAYER \_ \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}.**

### <a name="policy-change-reauthorization"></a>Reautorización de cambio de directiva

Un cambio de directiva se implementa como adición o eliminación de filtros en una capa de ALE. Una vez detectado un cambio de directiva, se especificará el primer paquete que atraviesa un flujo de ALE creado en la capa afectada para la reautorización en la capa. Por lo tanto, para la reautorización es totalmente posible que un paquete saliente se clasifique en la capa [**FWPM \_ LAYER \_ ALE \_ \_ AUTH RECV \_ ACCEPT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) y que un paquete entrante se clasifique en la capa **FWPM LAYER \_ \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}.**

Una razón para esta clasificación de dirección mixta es que es posible que no haya más tráfico de red desde la dirección original (por ejemplo, paquete de entrada para el flujo ALE entrante). Uno de estos ejemplos es el streaming UDP un solo sentido después de un protocolo de enlace de dos vías inicial. En este caso, es más conveniente que se desmonte el streaming lo antes posible.

### <a name="arrival-interface-reauthorization"></a>Reautorización de la interfaz de llegada

La reautorización de la interfaz de llegada está disponible a partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

Los paquetes que pertenecen al mismo flujo de ALE pueden llegar desde varias interfaces. El primer paquete que entra en una interfaz diferente de la interfaz original del flujo de ALE se vuelve a autorización.

En un modelo de host seguro, que es el modelo de seguridad predeterminado para la pila TCP/IP, una conexión en una interfaz de red solo acepta paquetes que se incluyen en la misma interfaz. Por lo tanto, la reautorización de la interfaz de llegada no se usa en un equipo host fuerte.

En un modelo de host débil, una conexión en una interfaz de red permite que los paquetes entren en cualquier otra interfaz de red. La reautorización de la interfaz de llegada se usa en un equipo host débil para implementar directivas específicas de la interfaz. Para obtener más información, [vea "The Cable Guy: Strong and Weak Host Models".](/previous-versions/technet-magazine/cc137807(v=msdn.10))

Algunos [campos clasificables pueden](filtering-conditions.md) ser desconocidos durante la reautorización. Por ejemplo, si se vuelve a autorizar un paquete saliente en la capa [**FWPM \_ LAYER \_ ALE \_ \_ AUTH RECV \_ ACCEPT \_ V{4 \| 6},**](management-filtering-layer-identifiers-.md) se desconocen todos los campos que pertenecen a la interfaz de llegada. En ese caso, los valores de los campos desconocidos se indican como [**FWP \_ EMPTY.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)

Los campos de [**tipo FWP \_ EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) pueden coincidir con [**FWP \_ MATCH \_ EQUAL.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) Por lo tanto, se puede establecer una directiva para bloquear las reautorizaciones y desmontar un flujo de ALE cuando llegan solicitudes de reautorización para el flujo de ALE.

## <a name="pending-connection-reauthorization"></a>Reautorización de conexión pendiente

Un controlador de llamada puede posponer una operación de clasificación en capas de ALE y completarla más adelante, cuando la decisión de filtrado se puede tomar de forma segura. La funcionalidad ALE postpone/complete se admite a través de las funciones en modo kernel [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) y [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0).

La reautorización se desencadena inmediatamente después de la llamada FwpsCompleteOperation0 y permite que el controlador de llamada permita o bloquee el flujo.

Solo se puede posponer una autorización inicial. Se producirá un error en una llamada a FwpsPendOperation0 si se establece la marca [**\_ FWP CONDITION \_ FLAG IS \_ \_ REAUTHORIZE.**](filtering-condition-flags-.md)

Para más información, consulte la [documentación Windows Driver Kit.](/windows-hardware/drivers/ddi/_netvista/)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación de la capa de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Capas de ALE](ale-layers.md)
</dt> <dt>

[Filtrado con estado de ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfico de multidifusión/difusión de ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Personalización de Flow ALE](ale-flow-customization.md)
</dt> </dl>

 

 