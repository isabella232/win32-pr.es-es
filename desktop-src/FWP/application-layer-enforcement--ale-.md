---
title: Aplicación de la capa de aplicación (ALE)
description: ALE es un conjunto de capas de modo kernel Windows Filtering Platform (WFP) que se usan para el filtrado con estado.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d74db5fdc231569f65c3b25cb630b306111aa5d6a7e3eb7faad743a5f74db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069475"
---
# <a name="application-layer-enforcement-ale"></a>Aplicación de la capa de aplicación (ALE)

ALE es un conjunto de capas de modo kernel Windows Filtering Platform (WFP) que se usan para el filtrado con estado.

El filtrado con estado realiza un seguimiento del estado de las conexiones de red y solo permite paquetes que coinciden con un estado de conexión conocido. Por ejemplo, el filtrado con estado para una conexión TCP iniciada desde detrás de un firewall solo puede permitir paquetes entrantes que coincidan con paquetes salientes anteriores enviados por la entidad protegida.

Los filtros de las capas de ALE autorizan la creación de conexiones entrantes y salientes, las asignaciones de puertos, las operaciones de socket como [**listen(),**](/windows/desktop/api/winsock2/nf-winsock2-listen)la creación de sockets sin procesar y la recepción en modo promiscuo.

El tráfico en las capas de ALE se clasifica por conexión o por socket. En las capas que no son de ALE, los filtros solo pueden clasificar el tráfico por paquete.

Las capas de ALE son las únicas capas de WFP en las que se puede filtrar el tráfico de red en función de la identidad de la aplicación (mediante un nombre de archivo normalizado) y en función de la identidad del usuario, mediante un descriptor de seguridad. (Consulte FLT \_ FILE \_ NAME INFORMATION en la documentación Windows Driver Kit (WDK), para obtener más información sobre los nombres de archivo \_ normalizados).

Además, cuando se usa IPsec para proteger la conexión, el filtrado en las capas de ALE también se puede realizar en la identidad de la máquina remota y en la identidad del usuario remoto. La máquina remota y las identidades de usuario se obtienen a partir de las credenciales usadas en la creación de una sesión de IPsec.

Por este motivo, las directivas que aplican quién (por ejemplo, "administrador") o qué aplicación (por ejemplo, "Internet Explorer") pueden realizar las operaciones de red mencionadas anteriormente se crearán en las capas de ALE.

ALE proporciona cumplimiento para directivas como "permitir a Windows Messenger todo el acceso a la red mientras se bloquean todas las demás aplicaciones". En este ejemplo, cuando la aplicación "Messenger" se conecta a través de la red, ALE captura el evento, determina que fue iniciado por Messenger y consulta el motor de filtros WFP para determinar si se debe permitir que el socket continúe.

> [!Note]  
> Debido a la naturaleza de los verdaderos sockets de doble IP, es posible que no se produzcan clasificaciones en la capa de ALE IPv4. Esto es así por diseño, porque para todas las intenciones y propósitos, el socket es un socket IPv6. Para ver el tráfico V4 de este tipo de socket, cree filtros en la capa V6 mediante la dirección asignada a IPv6.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capas de ALE](ale-layers.md)
</dt> <dt>

[Filtrado con estado de ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfico de multidifusión/difusión de ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalización de Flow ALE](ale-flow-customization.md)
</dt> </dl>

 

 