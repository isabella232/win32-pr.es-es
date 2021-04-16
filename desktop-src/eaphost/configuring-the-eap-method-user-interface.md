---
title: Configuración de la interfaz de usuario del método EAP
description: Explica cómo configurar el suplicante proporcionando una configuración de método EAP a EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105714317"
---
# <a name="configuring-the-eap-method-user-interface"></a>Configuración de la interfaz de usuario del método EAP

En este tema se explica cómo configurar el suplicante proporcionando una configuración de método EAP a EAPHost.

Para que un solicitante realice una autenticación basada en EAP mediante EAPHost, un suplicante debe proporcionar una configuración de método EAP a EAPHost a través de la función [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) .

1.  Para obtener la configuración del método EAP, un suplicante normalmente consulta a EAPHost mediante [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) para obtener información sobre el conjunto completo de métodos EAP que están disponibles e instalados en el equipo local. La lista de métodos normalmente se presenta al usuario en un cuadro combinado u otro control de la interfaz de usuario que permite al usuario seleccionar el método que deseen.
    > [!Note]  
    > El suplicante puede elegir filtrar la lista de métodos mostrada en función de los bits de propiedad de método indicados en el **método de EAP \_ \_ info. eapProperties**. Algunos métodos pueden no ser adecuados para las características de seguridad del transporte proporcionado por el suplicante, por ejemplo.

     

2.  Una vez que el control de IU se rellena con el conjunto de posibles métodos EAP, el usuario selecciona el método que desea configurar. Normalmente, el solicitante proporciona un botón de **configuración** o de **propiedades** para que el usuario tenga acceso a las propiedades de configuración del método EAP seleccionado.
    > [!Note]
    > El suplicante es consciente de que hay propiedades configurables por el usuario basadas en el bit **eapPropSupportsConfig** que se está habilitando en la **información del \_ método EAP \_ . eapProperties**.
    >
    > Para obtener más información, vea [**propiedades del método EAP**](eap-method-properties.md).

     

3.  Cuando el usuario hace clic en el control de IU adecuado, el solicitante llama a [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), pasando la función el valor **hWnd** para la interfaz de usuario propia del suplicante, la estructura de [**\_ \_ tipo del método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) obtenida de la consulta a la estructura de [**\_ \_ información del método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) y otros parámetros necesarios.
4.  La llamada a [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invoca la interfaz de usuario de configuración de un método EAP. En la devolución de **EapHostPeerInvokeConfigUI**, la función devolverá un BLOB de configuración del método EAP como parámetro out.
5.  El suplicante almacena el BLOB de configuración, junto con la estructura de [**\_ \_ tipo de método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) para su uso con [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).
6.  El método preciso para almacenar el BLOB configuración es totalmente el solicitante. Sin embargo, el suplicante siempre debe almacenar la configuración de forma adecuada y segura adecuada para los datos de configuración de autenticación del sistema y del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar directiva de grupo](enabling-group-policy.md)
</dt> <dt>

[Implementación de la compatibilidad de In-Band NAP con métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementación de la compatibilidad de NAP con métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferencia de datos entre el suplicante y los métodos EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Suplicantes de EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




