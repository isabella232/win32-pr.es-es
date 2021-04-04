---
title: Credenciales de autenticación del cliente
description: Cada cliente autenticado debe proporcionar las credenciales de autenticación al servidor.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076299"
---
# <a name="client-authentication-credentials"></a>Credenciales de autenticación del cliente

Cada cliente autenticado debe proporcionar las credenciales de autenticación al servidor. En RPC, el cliente almacena sus credenciales de autenticación en el enlace entre el cliente y el servidor. Para ello, el cliente llama a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).

Hay dos tipos de credenciales: implícitas y explícitas:

-   Las credenciales explícitas existen cuando el cliente suministra el nombre de usuario, la contraseña y el dominio.
-   Las credenciales implícitas existen cuando el cliente usa las credenciales del subproceso o el token de proceso que llama a las funciones **RpcBindingSetAuthInfo** o **RpcBindingSetAuthInfoEx** .

Los clientes deben abstenerse de proporcionar credenciales explícitas porque almacenar, manipular y recuperar una contraseña de usuario puede introducir una vulnerabilidad de seguridad en un sistema distribuido si se usan credenciales explícitas.

Para usar credenciales IMPLÍCITAS, el cliente llama a **RpcBindingSetAuthInfo**(*ex*). El sistema de seguridad y RPC obtienen credenciales del subproceso o el token del proceso para su uso en la sesión de autenticación.

Si el cliente usa credenciales explícitas, el quinto parámetro de estas dos funciones es del tipo [**identificador de identidad de autenticación de RPC \_ \_ \_**](rpc-auth-identity-handle.md). Se trata de un tipo flexible que es un puntero a una estructura de datos. El contenido de la estructura de datos puede diferir con cada servicio de autenticación. Actualmente, el SSP que admite RPC requiere que la aplicación establezca **el \_ \_ \_ identificador de identidad de autenticación de RPC** para que apunte a una estructura de [**\_ \_ \_ identidad de autenticación de WinNT**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) . La estructura de **\_ identidad de \_ autenticación \_ de WinNT** de la SEC contiene campos para un nombre de usuario, dominio y contraseña.

 

 




