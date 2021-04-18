---
title: Establecimiento de la seguridad en el nivel de proxy de interfaz
description: A veces, el cliente necesita un control específico sobre la seguridad en las llamadas a interfaces determinadas.
ms.assetid: 72925ca2-78c9-47d9-8760-63f6379326d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b38fe83e8ce8841cc9029808a6947ec67d4eaf4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705037"
---
# <a name="setting-security-at-the-interface-proxy-level"></a>Establecimiento de la seguridad en el nivel de proxy de interfaz

A veces, el cliente necesita un control específico sobre la seguridad en las llamadas a interfaces determinadas. Por ejemplo, la seguridad se podría establecer en un nivel bajo para el proceso, pero las llamadas a una interfaz determinada podrían requerir un nivel de autenticación superior, como el cifrado. Los métodos de la interfaz [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) permiten al cliente cambiar la configuración de seguridad asociada a las llamadas a una interfaz determinada mediante el control de la configuración de seguridad en el nivel de proxy de interfaz.

El cliente puede consultar un objeto existente para [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) y, a continuación, llamar al método [**IClientSecurity:: QueryBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-queryblanket) para averiguar cuál es la configuración de seguridad actual para un proxy de interfaz determinado. El método [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) se puede usar para modificar la configuración de seguridad de un proxy de interfaz individual en el objeto antes de llamar a uno de los métodos de la interfaz. La nueva configuración se aplica a todos los llamadores futuros de esta interfaz concreta. El método [**IClientSecurity:: CopyProxy**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-copyproxy) proporciona una manera para que el cliente Copie un proxy de interfaz de modo que las llamadas subsiguientes a **SetBlanket** en la copia no afecten a los llamadores del proxy original.

[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) se suele usar para elevar el nivel de autenticación de un proxy de interfaz determinado a un nivel más alto de protección de seguridad. Sin embargo, en algunas situaciones, también puede resultar útil reducir el nivel de autenticación de un proxy de interfaz determinado. Por ejemplo, supongamos que el nivel de autenticación predeterminado para el proceso es un valor que no es el nivel ninguno de autenticación RPC \_ C \_ \_ \_ y el cliente y el servidor están en dominios independientes que no confían entre sí. En este caso, se producirá un error en las llamadas al servidor a menos que el cliente llame a **SetBlanket** para reducir el nivel de autenticación a \_ \_ \_ nivel none de autenticación de RPC C \_ .

Los clientes que usan la implementación predeterminada de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) que proporciona el administrador del proxy pueden llamar a las funciones auxiliares [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)y [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) en lugar de llamar a métodos **IClientSecurity** directamente. Las funciones auxiliares simplifican el código pero son ligeramente menos eficientes que llamar directamente a los métodos **IClientSecurity** correspondientes.

El administrador del proxy implementa la interfaz [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) localmente para el cliente. Es posible que algunos objetos personalizados de serialización no admitan **IClientSecurity**.

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) funciona con todos los servicios de autenticación admitidos (actualmente NTLMSSP, Schannel y el protocolo Kerberos V5).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad de las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 