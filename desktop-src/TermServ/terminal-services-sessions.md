---
title: Sesiones de Escritorio remoto
description: Dado que cada inicio de sesión en un cliente de Conexión a Escritorio remoto (RDC) recibe un identificador de sesión independiente, la experiencia del usuario es similar a iniciar sesión en varios equipos al mismo tiempo. por ejemplo, un equipo de Office y un equipo doméstico.
ms.assetid: 09a990cd-7590-4d73-b1f5-8736f0b4f17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb99f9745e382bdff1099eabae9a8e8ef0b8333
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676403"
---
# <a name="remote-desktop-sessions"></a>Sesiones de Escritorio remoto

Cuando un usuario inicia sesión en un equipo habilitado para Servicios de Escritorio remoto, se inicia una sesión para el usuario. Cada sesión se identifica mediante un identificador de sesión único. Dado que cada inicio de sesión en un cliente de Conexión a Escritorio remoto (RDC) recibe un identificador de sesión independiente, la experiencia del usuario es similar a iniciar sesión en varios equipos al mismo tiempo. por ejemplo, un equipo de Office y un equipo doméstico.

Cada sesión de escritorio remoto está asociada a una estación de ventana interactiva. El único nombre de estación de ventana admitido para una estación de ventana interactiva es "WinSta0"; por lo tanto, cada sesión está asociada a su propia estación de ventana "WinSta0". Hay tres escritorios estándar para cada estación de ventana: el escritorio Winlogon, el escritorio del protector de pantalla y el escritorio interactivo.

El usuario asociado a la estación de ventana interactiva para una sesión se conoce como *usuario interactivo*. En un cliente Conexión a Escritorio remoto (RDC) puede haber varios usuarios interactivos además del usuario interactivo en la consola de Servicios de Escritorio remoto. Para recuperar el identificador de la sesión asociada actualmente a la consola, use la función [**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid) .

Cuando un usuario cierra sesión en un cliente de Conexión a Escritorio remoto (RDC), se elimina la sesión que tiene el cliente en el servidor de host de sesión Escritorio remoto (host de sesión de escritorio remoto) (anteriormente conocido como servidor de Terminal Server) y se quitan las estaciones de ventana y los escritorios asociados a esa sesión. Sin embargo, dado que la sesión de consola de Servicios de Escritorio remoto nunca se elimina, las estaciones de ventana asociadas a la sesión de consola no se eliminan. Esto afecta a cómo se comportan las aplicaciones en un entorno de Servicios de Escritorio remoto cuando están configuradas para ejecutarse en el contexto de seguridad del usuario interactivo, también conocido como el modo de activación de objetos de "usuario interactivo de runas".

Para obtener más información acerca de cómo iniciar un proceso de servidor local en una sesión especificada, consulte [activación de sesión en sesión con un moniker](session-to-session-activation-with-a-session-moniker.md) de sesión y [uso de un moniker de sesión](using-a-session-moniker.md). Para obtener más información sobre los contextos de seguridad, vea [el contexto de seguridad del cliente](/windows/desktop/SecAuthZ/the-client-security-context).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesiones secundarias](child-sessions.md)
</dt> </dl>

 

 