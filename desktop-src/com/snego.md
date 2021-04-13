---
title: Snego
description: Snego, cuyo identificador de servicio de autenticación es la autenticación \_ \_ de GSS de RPC C authn \_ \_ , no proporciona realmente servicios de autenticación.
ms.assetid: 2087a84c-d302-4511-9f02-2d20ee9e0d8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676b6428d6b7e79893214c2d234dcfc43992e190
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421449"
---
# <a name="snego"></a>Snego

Snego, cuyo identificador de servicio de autenticación es la autenticación \_ \_ de GSS de RPC C authn \_ \_ , no proporciona realmente servicios de autenticación. En su lugar, toma una lista de servicios de autenticación y negocia un servicio que funcionará entre el cliente y el servidor. Los parámetros de autenticación no se usan en Snego, pero se pasan al servicio de autenticación elegido, que realiza la autenticación real. Snego fue estandarizado por Internet Engineering Task Force (IETF) en diciembre de 1998, en el documento [RFC 2478](https://www.ietf.org/rfc/rfc2478.txt).

Snego es útil cuando no se sabe qué servicios de autenticación puede proporcionar el equipo remoto.

Para usar Snego, tanto el cliente como el servidor deben especificar Snego como servicio de autenticación. El servidor especifica el de RPC \_ C \_ authn \_ GSS \_ Negotiate como el miembro **dwAuthnSvc** de una de las estructuras de [**servicio de \_ autenticación \_ único**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) en el parámetro de matriz *asAuthSvc* que se pasa a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). El cliente puede especificar Snego mediante una llamada a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) y pasar \_ el parámetro de GSS de autenticación de RPC C \_ \_ \_ Negotiate Negotiate como parámetro *dwAuthnSvc* . El cliente también debe proporcionar una lista de los servicios de autenticación posibles para Snego a través del miembro **PackageList** de la estructura de [**\_ \_ \_ identidad \_ de autenticación WinNT**](/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa) de la SEC que se pasa al parámetro *pAuthInfo* en la llamada a **CoSetProxyBlanket**. Si *pAuthInfo* es **null**, Snego compone una lista de servicios de autenticación de los paquetes de seguridad instalados en el equipo. A continuación, Snego envía la lista de servicios de autenticación al servidor, compara la lista con los servicios de autenticación disponibles del servidor y elige un servicio de autenticación que se usará para la conexión.

> [!Note]  
> Schannel no puede estar en la lista de servicios de autenticación que usa Snego.

 

Los clientes también pueden especificar Snego cuando llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Los parámetros *dwAuthnSvc* y *pAuthInfo* de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) se convierten en miembros de una única estructura de [**\_ \_ información de autenticación**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) que se pasa a **CoInitializeSecurity** a través de su parámetro *pAuthList* . Los detalles de los valores de esos miembros son los mismos que los descritos en el párrafo anterior.

Si se usa Snego, las llamadas a [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) o [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) devolverán Snego como servicio de autenticación, en lugar del servicio de autenticación real que Snego seleccionado para establecer la conexión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[COM y paquetes de seguridad](com-and-security-packages.md)
</dt> </dl>

 

 