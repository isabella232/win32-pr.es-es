---
title: Configuración de la seguridad de Process-Wide con CoInitializeSecurity
description: La función CoInitializeSecurity permite controlar escenarios de seguridad complejos estableciendo la seguridad de una aplicación mediante programación.
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567a6dfaf47dbd278fc248558cd25969c733b24a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421473"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>Configuración de la seguridad de Process-Wide con CoInitializeSecurity

La función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) permite controlar escenarios de seguridad complejos estableciendo la seguridad de una aplicación mediante programación. En este tema se describen los escenarios en los que puede usar **CoInitializeSecurity** y se proporcionan algunos detalles sobre su uso.

Hay varias razones por las que podría querer usar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad de todo el proceso en el programa. Por ejemplo, aunque puede establecer el nivel de autenticación y los permisos de acceso para la aplicación mediante dcomcnfg.exe, es posible que el nivel de suplantación predeterminado del equipo no sea el que desee para su proceso. La única manera de cambiar esta configuración para el proceso es llamar a **CoInitializeSecurity**.

Si desea utilizar el proveedor de seguridad Schannel, debe especificarlo como un servicio de autenticación en una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Otro escenario común en el que podría establecer la seguridad de todo el proceso mediante programación es cuando desea establecer la seguridad predeterminada para todo el proceso, pero tiene uno o más objetos dentro de ese proceso que exponen interfaces con requisitos de seguridad especiales. En este caso, puede llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad del proceso, lo que permite a com controlar la mayoría de las comprobaciones de seguridad, y puede llamar a otros métodos para establecer la seguridad de los objetos con necesidades de seguridad especiales. La llamada a estos métodos y funciones se describe en [configuración de la seguridad en el nivel del proxy de la interfaz](setting-security-at-the-interface-proxy-level.md).

Si su aplicación tiene requisitos de seguridad muy especializados, como permitir que determinados grupos tengan acceso a objetos diferentes en función de la hora del día, es posible que desee controlar toda la seguridad mediante programación, asegurándose de que COM no realiza ninguna comprobación automática en absoluto. Para ello, debe llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), establecer el parámetro *dwAuthnLevel* en None y el parámetro *pVoid* en **null**. Si tiene su propio paquete de seguridad, también debe registrarlo en el parámetro *pAuthnSvc* . Después, puede administrar toda su propia seguridad mediante programación a través de llamadas a la interfaz de nivel de proxy y las funciones descritas en [configuración de la seguridad en el nivel de proxy de la interfaz](setting-security-at-the-interface-proxy-level.md).

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ofrece un amplio conjunto de funcionalidades. Si se llama a **CoInitializeSecurity**, se omiten los valores del registro y se usan en su lugar los valores de inicialización de seguridad que se pasan a la llamada. Dependiendo del resultado que desee, el primer parámetro, *pVoid*, puede apuntar a tres tipos diferentes de valores: un [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , un objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) o un puntero a un AppID. En la mayoría de los casos, usará funciones de Windows para crear un **\_ descriptor de seguridad** al que apuntará *pVoid* .

Sin embargo, *pVoid* también puede apuntar a un objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) .

Para indicar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) que está pasando un objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) a *pVoid*, debe pasar el \_ valor de control de acceso EOAC \_ al parámetro *dwCapabilities* . Dado que **CoInitializeSecurity** almacena en caché los resultados de las comprobaciones de acceso, la lista de control de acceso no se debe cambiar después de llamar a **CoInitializeSecurity**.

Otro tipo de valor que se puede pasar al parámetro *pVoid* es un puntero a un GUID, que es el AppID de la aplicación. Si *pVoid* es un puntero a un AppID, debe especificar EOAC \_ AppID en el parámetro *pCapabilities* para que la función sepa qué valor se debe esperar en *pVoid*. Si *pVoid* apunta a un AppID, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) solo usa el registro para los valores de autenticación y omite todos los demás parámetros en **CoInitializeSecurity**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad de Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 