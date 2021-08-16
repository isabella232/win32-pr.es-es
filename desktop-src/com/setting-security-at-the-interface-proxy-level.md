---
title: Establecer la seguridad en el nivel de proxy de interfaz
description: A veces, el cliente necesita un control específico sobre la seguridad en las llamadas a interfaces concretas.
ms.assetid: 72925ca2-78c9-47d9-8760-63f6379326d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef969039dcfdc12449b7a8d0a3d63729ab5f84061ade1a743d21a1b6b34331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309100"
---
# <a name="setting-security-at-the-interface-proxy-level"></a>Establecer la seguridad en el nivel de proxy de interfaz

A veces, el cliente necesita un control específico sobre la seguridad en las llamadas a interfaces concretas. Por ejemplo, la seguridad se puede establecer en un nivel bajo para el proceso, pero las llamadas a una interfaz determinada pueden requerir un nivel de autenticación superior, como el cifrado. Los métodos de la [**interfaz IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) permiten al cliente cambiar la configuración de seguridad asociada a las llamadas a una interfaz determinada mediante el control de la configuración de seguridad en el nivel de proxy de interfaz.

El cliente puede consultar un objeto existente para [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) y, a continuación, llamar al método [**IClientSecurity::QueryBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-queryblanket) para averiguar cuál es la configuración de seguridad actual para un proxy de interfaz determinado. El [**método IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) se puede usar para modificar la configuración de seguridad de un proxy de interfaz individual en el objeto antes de llamar a uno de los métodos de la interfaz. La nueva configuración se aplica a cualquier llamador futuro de esta interfaz concreta. El [**método IClientSecurity::CopyProxy**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-copyproxy) proporciona una manera de que el cliente copie un proxy de interfaz para que las llamadas posteriores a **SetBlanket** en la copia no afecten a los autores de llamadas del proxy original.

[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) se usa normalmente para elevar el nivel de autenticación de un proxy de interfaz determinado a un nivel superior de protección de seguridad. Sin embargo, en algunas situaciones, también puede resultar útil reducir el nivel de autenticación para un proxy de interfaz determinado. Por ejemplo, suponga que el nivel de autenticación predeterminado para el proceso es un valor distinto de RPC C AUTHN LEVEL NONE y el cliente y el servidor están en dominios independientes que no confían \_ \_ entre \_ \_ sí. En este caso, se producirá un error en las llamadas al servidor a menos que el cliente llame a **SetBlanket** para reducir el nivel de autenticación a RPC \_ C \_ AUTHN \_ LEVEL \_ NONE.

Los clientes que usan la implementación predeterminada de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) proporcionada por el administrador de proxy pueden llamar a las funciones auxiliares [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)y [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) en lugar de llamar directamente a los métodos **IClientSecurity.** Las funciones auxiliares simplifican el código, pero son ligeramente menos eficaces que llamar directamente a los métodos **IClientSecurity** correspondientes.

El administrador de proxy implementa localmente la interfaz [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) para el cliente. Es posible que algunos objetos serializados personalizados **no admitan IClientSecurity.**

[**IClientSecurity funciona**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) con todos los servicios de autenticación admitidos (actualmente NTLMSSP, Schannel y el protocolo Kerberos v5).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad para las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 