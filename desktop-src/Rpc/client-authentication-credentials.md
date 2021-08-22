---
title: Credenciales de autenticación de cliente
description: Cada cliente autenticado debe proporcionar credenciales de autenticación al servidor.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2410b073886ffd70409cd749ea90305faa8d4635754e8f9596547c47bb976800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932191"
---
# <a name="client-authentication-credentials"></a>Credenciales de autenticación de cliente

Cada cliente autenticado debe proporcionar credenciales de autenticación al servidor. En RPC, el cliente almacena sus credenciales de autenticación en el enlace entre el cliente y el servidor. Para ello, el cliente llama a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)

Hay dos tipos de credenciales: implícitas y explícitas:

-   Existen credenciales explícitas cuando el cliente proporciona el nombre de usuario, la contraseña y el dominio.
-   Las credenciales implícitas existen cuando el cliente usa credenciales del token de subproceso o proceso que llama a las **funciones RpcBindingSetAuthInfo** o **RpcBindingSetAuthInfoEx.**

Los clientes deben evitar proporcionar credenciales explícitas porque almacenar, manipular y recuperar una contraseña de usuario puede introducir una vulnerabilidad de seguridad en un sistema distribuido si se usan credenciales explícitas.

Para usar credenciales implícitas, el cliente llama a **RpcBindingSetAuthInfo***(por ejemplo,*). El sistema de seguridad y RPC obtienen las credenciales del subproceso o token de proceso para su uso en la sesión de autenticación.

Si el cliente usa credenciales explícitas, el quinto parámetro de estas dos funciones es de tipo [**RPC \_ AUTH \_ IDENTITY \_ HANDLE**](rpc-auth-identity-handle.md). Se trata de un tipo flexible que es un puntero a una estructura de datos. El contenido de la estructura de datos puede diferir con cada servicio de autenticación. Actualmente, los SSP que admite RPC requieren que la aplicación establezca **RPC \_ AUTH \_ IDENTITY \_ HANDLE** para que apunte a una estructura DE IDENTIDAD DE [**\_ AUTENTICACIÓN DE WINNT \_ \_ de SEC.**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) La **estructura \_ SEC WINNT \_ AUTH \_ IDENTITY** contiene campos para un nombre de usuario, un dominio y una contraseña.

 

 




