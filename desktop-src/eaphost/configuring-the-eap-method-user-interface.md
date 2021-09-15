---
title: Configuración del método EAP Interfaz de usuario
description: Explica cómo configurar el suplicante mediante el suministro de una configuración de método EAP a EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568812"
---
# <a name="configuring-the-eap-method-user-interface"></a>Configuración del método EAP Interfaz de usuario

En este tema se explica cómo configurar el suplicante mediante el suministro de una configuración de método EAP a EAPHost.

Para que un suplicante realice una autenticación basada en EAP mediante EAPHost, un suplicante debe proporcionar una configuración de método EAP a EAPHost a través de la [**función EapHostPeerBeginSession.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)

1.  Para obtener la configuración del método EAP, un suplicante consulta normalmente EAPHost mediante [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) para obtener información sobre el conjunto completo de métodos EAP que están disponibles e instalados en el equipo local. La lista de métodos se presenta normalmente al usuario en un cuadro de combinación u otro control de interfaz de usuario que permite al usuario seleccionar el método que desea.
    > [!Note]  
    > El suplicante puede optar por filtrar la lista de métodos mostrada en función de los bits de propiedad del método indicados en **EAP \_ METHOD \_ INFO.eapProperties**. Algunos métodos pueden no ser adecuados para las características de seguridad del transporte proporcionado por el suplicante, por ejemplo.

     

2.  Una vez que el control de interfaz de usuario se rellena con el conjunto de posibles métodos EAP, el usuario selecciona el método que quiere configurar. Normalmente, el suplicante proporciona un botón **Configuración** o **Propiedades para** que el usuario acceda a las propiedades de configuración del método EAP seleccionado.
    > [!Note]
    > El suplicante es consciente de que hay propiedades configurables por el usuario basadas en el bit **eapPropSupportsConfig** que se está habilitando en **EAP METHOD \_ \_ INFO.eapProperties**.
    >
    > Para obtener más información, vea [**Propiedades del método EAP**](eap-method-properties.md).

     

3.  Cuando el usuario hace clic en el control de interfaz de usuario adecuado, el suplicante llama a [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui)y pasa a la función el valor **HWND** de la propia interfaz de usuario del suplicante, la estructura [**EAP METHOD \_ \_ TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) obtenida de la consulta a la estructura [**EAP METHOD \_ \_ INFO**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) y otros parámetros necesarios.
4.  Al [**llamar a EapHostPeerInvokeConfigUI,**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) se invoca la propia interfaz de usuario de configuración de un método EAP. Al devolver desde **EapHostPeerInvokeConfigUI,** la función devolverá un BLOB de configuración del método EAP como parámetro externo.
5.  El suplicante almacena el BLOB de configuración, junto con la estructura [**EAP \_ METHOD \_ TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) para su uso [**con EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).
6.  El método preciso para almacenar el BLOB configurador es totalmente el suplicante. Sin embargo, el suplicante siempre debe almacenar la configuración de una manera adecuada y segura adecuada para los datos de configuración de autenticación del sistema y del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar directiva de grupo](enabling-group-policy.md)
</dt> <dt>

[Implementar la compatibilidad In-Band NAP para métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementación de la compatibilidad de NAP con métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferencia de datos entre los métodos supplicant y EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




