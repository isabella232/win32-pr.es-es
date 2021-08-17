---
title: Snego
description: Snego, cuyo identificador de servicio de autenticación es RPC \_ C \_ AUTHN GSS NEGOTIATE, no proporciona realmente los propios \_ servicios de \_ autenticación.
ms.assetid: 2087a84c-d302-4511-9f02-2d20ee9e0d8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82f8da58cc77ebfd4debd0763ad4af6e1c96d3e88d9ede69ff82a28e3d8a5ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129817"
---
# <a name="snego"></a>Snego

Snego, cuyo identificador de servicio de autenticación es RPC \_ C \_ AUTHN GSS NEGOTIATE, no proporciona realmente los propios \_ servicios de \_ autenticación. En su lugar, toma una lista de servicios de autenticación y negocia un servicio que funcionará entre el cliente y el servidor. Snego no usa los parámetros de autenticación, pero se pasan al servicio de autenticación elegido, que realiza la autenticación real. Snego fue estandarizado por el IETF (Internet Engineering Task Force) en diciembre de 1998, en el documento [RFC 2478](https://www.ietf.org/rfc/rfc2478.txt).

Snego es útil cuando no se sabe qué servicios de autenticación puede proporcionar el equipo remoto.

Para usar Snego, tanto el cliente como el servidor deben especificar Snego como servicio de autenticación. El servidor especifica RPC \_ C \_ AUTHN GSS NEGOTIATE como miembro \_ \_ **dwAuthnSvc** [**\_ \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)  de una de las estructuras SOLE AUTHENTICATION SERVICE en el parámetro de matriz asAuthSvc que se pasa a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). El cliente puede especificar Snego llamando a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) y pasando RPC \_ C \_ AUTHN GSS NEGOTIATE como parámetro \_ \_ *dwAuthnSvc.* El cliente también debe proporcionar una lista de los posibles servicios de autenticación para Snego a través del miembro **PackageList** de la estructura [**SEC \_ WINNT \_ AUTH \_ IDENTITY \_ EX**](/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa) que se pasa al *parámetro pAuthInfo* en la llamada a **CoSetProxyBlanket**. Si *pAuthInfo* es **NULL,** Snego crea una lista de servicios de autenticación a partir de los paquetes de seguridad instalados en el equipo. A continuación, Snego envía la lista de servicios de autenticación al servidor, compara la lista con los servicios de autenticación disponibles del servidor y elige un servicio de autenticación que se usará para la conexión.

> [!Note]  
> Schannel no puede estar en la lista de servicios de autenticación que usa Snego.

 

Los clientes también pueden especificar Snego cuando llaman a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) Los *parámetros dwAuthnSvc* y *pAuthInfo* de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) se convierten en miembros de una estructura [**SOLE AUTHENTICATION \_ \_ INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) que se pasa a **CoInitializeSecurity** a través de su *parámetro pAuthList.* Los detalles de los valores de esos miembros son los mismos que se describen en el párrafo anterior.

Si se usa Snego, las llamadas a [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) o [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) devolverán Snego como servicio de autenticación, en lugar del servicio de autenticación real que Snego ha elegido para establecer la conexión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[COM y paquetes de seguridad](com-and-security-packages.md)
</dt> </dl>

 

 