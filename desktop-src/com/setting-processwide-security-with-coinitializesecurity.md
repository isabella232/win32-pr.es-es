---
title: Establecer Process-Wide seguridad con CoInitializeSecurity
description: La función CoInitializeSecurity permite controlar escenarios de seguridad complejos estableciendo la seguridad de una aplicación mediante programación.
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c3e601897e9f2313682a3474c1760bc211285d8fa81a82f67d114681a7a57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610895"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>Establecer Process-Wide seguridad con CoInitializeSecurity

La [**función CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) permite controlar escenarios de seguridad complejos estableciendo la seguridad de una aplicación mediante programación. En este tema se describen los escenarios en los que podría usar **CoInitializeSecurity** y se proporcionan algunos detalles sobre cómo se usa.

Hay varias razones por las que es posible que quiera usar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad de todo el proceso dentro del programa. Por ejemplo, aunque puede establecer el nivel de autenticación y los permisos de acceso para la aplicación mediante dcomcnfg.exe, es posible que el nivel de suplantación predeterminado del equipo no sea el que desea para el proceso. La única manera de cambiar esta configuración para el proceso es llamar a **CoInitializeSecurity**.

Si desea usar el proveedor de seguridad de Schannel, debe especificarlo como un servicio de autenticación en una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Otro escenario común en el que podría establecer la seguridad de todo el proceso mediante programación es cuando desea establecer la seguridad predeterminada para todo el proceso, pero tiene uno o varios objetos dentro de ese proceso que exponen interfaces con requisitos de seguridad especiales. En este caso, puede llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad del proceso, lo que permite a COM controlar la mayoría de las comprobaciones de seguridad, y puede llamar a otros métodos para establecer la seguridad de los objetos con necesidades de seguridad especiales. La llamada a estos métodos y funciones se describe [en Establecer la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md).

Si la aplicación tiene requisitos de seguridad muy especializados, como permitir que determinados grupos accedan a distintos objetos en función de la hora del día, es posible que quiera controlar toda la seguridad mediante programación, asegurándose de que COM no realiza ninguna comprobación automática por usted. Para ello, debe llamar a [**CoInitializeSecurity,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)estableciendo el parámetro *dwAuthnLevel* en none y el *parámetro pVoid* en **NULL.** Si tiene su propio paquete de seguridad, también tendría que registrarlo en el *parámetro pAuthnSvc.* A continuación, puede controlar toda su propia seguridad mediante programación a través de llamadas a la interfaz de nivel de proxy y a las funciones descritas en Establecer la seguridad en el [nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md).

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ofrece un amplio conjunto de funcionalidades. Si llama a **CoInitializeSecurity**, los valores del Registro se omiten y en su lugar se usan los valores de inicialización de seguridad que pasa a la llamada. En función del resultado que desee, el primer parámetro, *pVoid*, puede apuntar a tres tipos diferentes de valores: un DESCRIPTOR DE [**\_ SEGURIDAD,**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) un objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) o un puntero a un AppID. En la mayoría de los casos, usará Windows para crear un **DESCRIPTOR DE \_ SEGURIDAD** al que *apuntará pVoid.*

Sin embargo, *pVoid* también puede apuntar a un [**objeto IAccessControl.**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol)

Para indicar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) que está pasando un objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) a *pVoid*, debe pasar el valor de ACCESS CONTROL de EOAC al \_ parámetro \_ *dwCapabilities.* Puesto **que CoInitializeSecurity** almacena en caché los resultados de las comprobaciones de acceso, no se debe cambiar la lista de control de acceso después de llamar a **CoInitializeSecurity**.

Otro tipo de valor que puede pasar al *parámetro pVoid* es un puntero a un GUID, que es el AppID de la aplicación. Si *pVoid* es un puntero a un AppID, debe especificar EOAC APPID en el \_ parámetro *pCapabilities* para que la función sepa qué valor esperar en *pVoid*. Si *pVoid* apunta a un AppID, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) solo usa el Registro para los valores de autenticación y omite todos los demás parámetros a **CoInitializeSecurity**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de Process-Wide seguridad](setting-processwide-security.md)
</dt> </dl>

 

 