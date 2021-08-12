---
title: Implementación de la compatibilidad de NAP con métodos EAP
description: Obtenga información sobre cómo implementar la compatibilidad con NAP para un suplicante EAPHost. Consulte los temas de NAP relacionados con EAPHost y vea los recursos disponibles adicionales.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff84c24aeb475b83146f2c56e9e139fd930eac27656349c594f05d91c1036fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273319"
---
# <a name="implementing-nap-support-for-eap-methods"></a>Implementación de la compatibilidad de NAP con métodos EAP

En este tema se explica cómo implementar NAP para un suplicante EAPHost. En Windows Vista y Windows Server 2008 un cliente de cumplimiento nap (NAP EC) está disponible para las conexiones [autenticadas 802.1X.](/previous-versions/windows/embedded/ms890287(v=msdn.10))

## <a name="implementing-network-access-protection-nap"></a>Implementación de la protección de acceso a redes (NAP)

Para admitir NAP, un suplicante EAPHost implementa una función de devolución de llamada que coincide con el prototipo de devolución de llamada [**NotificationHandler**](/previous-versions/windows/desktop/api) y debe proporcionar un puntero a esta función de devolución de llamada al llamar a [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).

La función de devolución de llamada toma dos parámetros.

-   GUID que identifica de forma única la interfaz asociada a la autenticación.
-   Puntero VOID a una estructura de datos opaca proporcionada por el suplicante.

EAPHost llamará a la función de devolución de llamada proporcionada por el suplicante con el GUID de interfaz única y el puntero VOID cuando cambie el estado de cuarentena de la máquina. Cuando EAPHost llama a la función de devolución de llamada proporcionada por el suplicante, el suplicante responde anulando la conexión de red lógica identificada por el puntero GUID/VOID de la interfaz y comienza la autenticación de nuevo **mediante EapHostPeerBeginSession**.

EAPHost puede llamar a la función de devolución de llamada proporcionada por suplicant en cualquier momento: antes, durante una autenticación activa o después de que se haya completado la autenticación (después de llamar a [**EapHostPeerEndSession,**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) pero no antes de que se haya llamado a [**EapHostPeerClearConnection).**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) El suplicante siempre debe responder si se desmonta la conexión de red lógica y se vuelve a autenticar.

Si el suplicante se está cerrando o decide dejar de recibir notificaciones de cambios de estado de aislamiento, el suplicante debe llamar a [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) y especificar el GUID de interfaz adecuado. Si el suplicante desea determinar el aislamiento de la conexión de red lógica, el suplicante puede obtener esa información de **EapHostPeerMethodResult.isolationState** cuando [**eapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) se obtiene de [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).

## <a name="eaphost-related-nap-information"></a>Información de NAP relacionada con EAPHost

Para obtener información de NAP relacionada con la API de EAPHost, consulte los temas siguientes.

-   [**TIPO DE \_ ATRIBUTO \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**ERROR DE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [Preguntas más frecuentes sobre el suplicante de EAPHost](eaphost-supplicant-frequently-asked-questions.md)
-   [**Propiedades del método EAP**](eap-method-properties.md)
-   [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**Errores relacionados con EAP e constantes de información**](eap-related-error-and-information-constants.md)
-   [**ESTADO DE \_ AISLAMIENTO**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**NotificationHandler**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>Recursos adicionales


-   Para obtener una lista de los recursos nap, consulte [Protección de acceso a redes.](https://go.microsoft.com/fwlink/p/?linkid=84107)
-   Para obtener información sobre la declaración de estado, vea [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).
-   Para la página Enterprise web y el blog del grupo de redes, consulte [Protección de acceso a redes (NAP).](https://go.microsoft.com/fwlink/p/?linkid=83845)
-   Para obtener información sobre la API de NAP, consulte [Protección de acceso a redes.](/windows/desktop/NAP/network-access-protection-start-page)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del método EAP Interfaz de usuario](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitar directiva de grupo](enabling-group-policy.md)
</dt> <dt>

[Implementar la compatibilidad In-Band NAP para los métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Transferencia de datos entre los métodos supplicant y EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Suplicantes de EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 