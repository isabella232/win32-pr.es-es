---
title: Escritorio remoto sesiones
description: Dado que cada inicio de sesión en un cliente Conexión a Escritorio remoto (RDC) recibe un identificador de sesión independiente, la experiencia del usuario es similar a iniciar sesión en varios equipos al mismo tiempo. por ejemplo, un equipo de oficina y un equipo principal.
ms.assetid: 09a990cd-7590-4d73-b1f5-8736f0b4f17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5093e9da70301fc4258ce2df88527c87940e455050a0673ac36d2fb04a8cd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987165"
---
# <a name="remote-desktop-sessions"></a>Escritorio remoto sesiones

Cuando un usuario inicia sesión en un equipo Servicios de Escritorio remoto, se inicia una sesión para el usuario. Cada sesión se identifica mediante un identificador de sesión único. Dado que cada inicio de sesión en un cliente Conexión a Escritorio remoto (RDC) recibe un identificador de sesión independiente, la experiencia del usuario es similar a iniciar sesión en varios equipos al mismo tiempo. por ejemplo, un equipo de oficina y un equipo principal.

Cada sesión de Escritorio remoto está asociada a una estación de ventana interactiva. El único nombre de estación de ventana compatible para una estación de ventana interactiva es "WinSta0"; por lo tanto, cada sesión está asociada a su propia estación de ventana "WinSta0". Hay tres escritorios estándar para cada estación de ventana: el escritorio Winlogon, el escritorio de protector de pantalla y el escritorio interactivo.

El usuario asociado a la estación de ventana interactiva para una sesión se conoce como *el usuario interactivo*. En un Conexión a Escritorio remoto remoto (RDC) puede haber varios usuarios interactivos además del usuario interactivo en la Servicios de Escritorio remoto cliente. Para recuperar el identificador de la sesión asociada actualmente a la consola, use la [**función WTSGetActiveConsoleSessionId.**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)

Cuando un usuario cierra sesión desde un cliente de Conexión a Escritorio remoto (RDC), se elimina la sesión que tiene el cliente en el servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) (anteriormente conocido como servidor terminal) y se quitan las estaciones de ventana y los escritorios asociados a esa sesión. Sin embargo, dado que Servicios de Escritorio remoto sesión de consola nunca se elimina, no se eliminan las estaciones de ventana asociadas a la sesión de consola. Esto afecta al comportamiento de las aplicaciones en un entorno de Servicios de Escritorio remoto cuando están configuradas para ejecutarse en el contexto de seguridad del usuario interactivo, también conocido como modo de activación de objetos "RunAs Interactive User".

Para obtener más información sobre cómo iniciar un proceso de servidor local en una sesión especificada, vea Activación de sesión a sesión con un [Moniker](session-to-session-activation-with-a-session-moniker.md) de sesión y Uso de un [Moniker de sesión](using-a-session-moniker.md). Para obtener más información sobre los contextos de seguridad, vea [Contexto de seguridad del cliente.](/windows/desktop/SecAuthZ/the-client-security-context)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesiones secundarias](child-sessions.md)
</dt> </dl>

 

 