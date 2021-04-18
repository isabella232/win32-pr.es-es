---
title: Aplicación del nivel de aplicación (ALE)
description: ALE es un conjunto de niveles de modo kernel de la plataforma de filtrado de Windows (WFP) que se usan para el filtrado con estado.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420666"
---
# <a name="application-layer-enforcement-ale"></a>Aplicación del nivel de aplicación (ALE)

ALE es un conjunto de niveles de modo kernel de la plataforma de filtrado de Windows (WFP) que se usan para el filtrado con estado.

El filtrado con estado realiza un seguimiento del estado de las conexiones de red y solo permite los paquetes que coinciden con un estado de conexión conocido. Por ejemplo, el filtrado con estado para una conexión TCP iniciada desde detrás de un Firewall puede permitir que solo los paquetes entrantes que coincidan con los paquetes salientes anteriores enviados por la entidad protegida.

Los filtros de las capas ALE autorizan la creación de conexiones entrantes y salientes, las asignaciones de puerto, las operaciones de socket como [**Listen ()**](/windows/desktop/api/winsock2/nf-winsock2-listen), la creación de sockets sin formato y la recepción en modo promiscuo.

El tráfico que se encuentra en los niveles de ALE se clasifica en función de la conexión o del socket. En las capas que no son ALE, los filtros solo pueden clasificar el tráfico por paquete.

Los niveles ALE son los únicos niveles de WFP en los que se puede filtrar el tráfico de red en función de la identidad de la aplicación, mediante un nombre de archivo normalizado, y según la identidad del usuario, mediante un descriptor de seguridad. (Consulte FLT \_ \_Información sobre \_ el nombre de archivo en la documentación del kit de controladores de Windows (WDK), para obtener más información sobre los nombres de archivo normalizados.

Además, cuando se usa IPsec para proteger la conexión, el filtrado en las capas de ALE también puede realizarse en la identidad del equipo remoto y en la identidad del usuario remoto. Las identidades de usuario y equipo remoto se obtienen a partir de las credenciales usadas en la creación de una sesión de IPsec.

Por este motivo, las directivas que aplican quién (por ejemplo, "administrador") o la aplicación (por ejemplo, "Internet Explorer") pueden realizar las operaciones de red mencionadas anteriormente se crean en los niveles de ALE.

ALE permite el cumplimiento de directivas como "permitir que Windows Messenger todo el acceso a la red mientras se bloquea el resto de las aplicaciones". En este ejemplo, cuando la aplicación "Messenger" se conecta a través de la red, ALE captura el evento, determina que se inició mediante Messenger y consulta el motor de filtros de WFP para determinar si se debe permitir que el socket continúe.

> [!Note]  
> Debido a la naturaleza de los verdaderos sockets de dos IP, es posible que no se produzcan clasificaciones en la capa de ALE de IPv4. Esto es así por diseño, ya que para todos los fines y propósitos, el socket es un socket IPv6. Para ver el tráfico V4 para este tipo de socket, cree filtros en la capa V6 mediante la dirección asignada por IPv6.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Niveles ALE](ale-layers.md)
</dt> <dt>

[Filtrado con estado ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfico de multidifusión/difusión ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalización del flujo ALE](ale-flow-customization.md)
</dt> </dl>

 

 