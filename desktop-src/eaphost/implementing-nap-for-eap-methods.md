---
title: Implementación de la compatibilidad de NAP con métodos EAP
description: Obtenga información sobre cómo implementar la compatibilidad de NAP para un suplicante de EAPHost. Vea los temas NAP relacionados con EAPHost y ver recursos adicionales disponibles.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5f0bc8900ee3d9cb01edb79b64b8ef5a68df4c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104078641"
---
# <a name="implementing-nap-support-for-eap-methods"></a>Implementación de la compatibilidad de NAP con métodos EAP

En este tema se explica cómo implementar NAP para un suplicante de EAPHost. En Windows Vista y Windows Server 2008, hay un cliente de cumplimiento NAP (NAP EC) disponible para las conexiones autenticadas de [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .

## <a name="implementing-network-access-protection-nap"></a>Implementación de protección de acceso a redes (NAP)

Para admitir NAP, un suplicante de EAPHost implementa una función de devolución de llamada que coincide con el prototipo de devolución de llamada [**NotificationHandler**](/previous-versions/windows/desktop/api) y debe proporcionar un puntero a esta función de devolución de llamada al llamar a [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).

La función de devolución de llamada toma dos parámetros.

-   GUID que identifica de forma única la interfaz asociada a la autenticación.
-   Puntero VOID a una estructura de datos opaca suministrada por el solicitante.

EAPHost llamará a la función de devolución de llamada proporcionada por el suplicante con el GUID de la interfaz única y el puntero VOID cuando cambie el estado de cuarentena del equipo. Cuando EAPHost llama a la función de devolución de llamada proporcionada por el suplicante, el suplicante responde cerrando la conexión de red lógica identificada por el puntero de interfaz GUID/VOID y comienza de nuevo la autenticación mediante **EapHostPeerBeginSession**.

EAPHost puede llamar a la función de devolución de llamada proporcionada por el suplicante en cualquier momento: antes, durante una autenticación activa o después de que se haya completado la autenticación (después de que se haya llamado a [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) pero no antes de que se haya llamado a [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ). El suplicante siempre debe responder si se anula la conexión de red lógica y se vuelve a autenticar.

Si el solicitante se está cerrando o está eligiendo dejar de recibir una notificación de cambios de estado de aislamiento, el solicitante debe llamar a [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) y especificar el GUID de interfaz adecuado. Si el solicitante desea determinar el aislamiento de la conexión de red lógica, el solicitante puede obtener esa información de **EapHostPeerMethodResult. isolationState** cuando [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) se obtiene de [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).

## <a name="eaphost-related-nap-information"></a>Información de NAP relacionada con EAPHost

Para información sobre NAP relacionada con la API de EAPHost, consulte los temas siguientes.

-   [**\_tipo de atributo EAP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**ERROR de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [Preguntas más frecuentes sobre el suplicante de EAPHost](eaphost-supplicant-frequently-asked-questions.md)
-   [**Propiedades del método EAP**](eap-method-properties.md)
-   [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**Constantes de información y errores relacionados con EAP**](eap-related-error-and-information-constants.md)
-   [**Estado de aislamiento \_**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**NotificationHandler**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>Recursos adicionales


-   Para obtener una lista de recursos de NAP, consulte [protección de acceso a redes](https://go.microsoft.com/fwlink/p/?linkid=84107).
-   Para obtener información sobre el informe de mantenimiento, consulte [mensajes de informe de mantenimiento (SOH) de protección de acceso a redes (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83918).
-   Para la página web del grupo de redes empresariales y el blog, consulte [protección de acceso a redes (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).
-   Para obtener información sobre la API de NAP, consulte [protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page).


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la interfaz de usuario del método EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitar directiva de grupo](enabling-group-policy.md)
</dt> <dt>

[Implementación de la compatibilidad de In-Band NAP con métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Transferencia de datos entre el suplicante y los métodos EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Suplicantes de EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 