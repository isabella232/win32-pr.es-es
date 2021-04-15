---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105695770"
---
# <a name="ntlmssp"></a>NTLMSSP

NTLMSSP, cuyo identificador de servicio de autenticación es RPC \_ C \_ authn \_ WinNT, es un proveedor de compatibilidad para seguridad que está disponible en todas las versiones de DCOM. Usa el protocolo NTLM para la autenticación. NTLM nunca transmite realmente la contraseña del usuario al servidor durante la autenticación. Por lo tanto, el servidor no puede usar la contraseña durante la suplantación para tener acceso a los recursos de red a los que el usuario tendría acceso. Solo se puede tener acceso a los recursos locales.

NTLM funciona tanto de forma local como entre equipos. Es decir, si el cliente y el servidor se encuentran en equipos diferentes, NTLM todavía puede asegurarse de que el cliente es quien dice ser.

Con NTLM, la identidad del cliente se representa mediante un nombre de dominio, un nombre de usuario y una contraseña o un token. Cuando un servidor llama a [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), se devuelven el nombre de dominio y el nombre de usuario del cliente. Sin embargo, cuando un servidor llama a [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), se devuelve el token del cliente. Si no hay ninguna relación de confianza entre el cliente y el servidor, y si el servidor tiene una cuenta local con el mismo nombre y la misma contraseña que el cliente, esa cuenta se usará para representar al cliente.

NTLM admite la autenticación mutua entre subprocesos y procesos cruzados (solo localmente). Si el cliente especifica el nombre principal del servidor con el formato usuario del dominio \\ en una llamada a [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), la identidad del servidor debe coincidir con el nombre de la entidad de seguridad o se producirá un error en la llamada. Si el cliente especifica **null**, no se comprobará la identidad del servidor.

NTLM también admite el nivel de suplantación de delegado entre subprocesos y procesos cruzados (solo localmente).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[COM y paquetes de seguridad](com-and-security-packages.md)
</dt> </dl>

 

 