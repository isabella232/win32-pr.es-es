---
title: Uso de Escritorio remoto Virtualization API
description: Los desarrolladores pueden usar esta API para personalizar la lógica que usa el Agente de conexión a Escritorio remoto para determinar el mejor destino para una conexión de cliente entrante.
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto , mediante la API de virtualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7075c3a0cfcabc2df0dcb8438b7de5a748eb2b0340e26bf3d1e51afdb182f81e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423635"
---
# <a name="using-the-remote-desktop-virtualization-api"></a>Uso de Escritorio remoto Virtualization API

El servicio de rol Directorio de sesión de Terminal Services (directorio de sesión de TS) permite a los servidores de terminal almacenar información de usuario y sesión en una base de datos denominada directorio de sesión. Cuando un usuario se conecta a un servidor de terminal server en una granja de servidores, el directorio de sesión de TS determina si el usuario ya tiene una sesión que se ejecuta en un servidor de terminal Server y, si es así, redirige al usuario a ese servidor de terminal Server.

En Windows Server 2008, se expandió el servicio de rol Directorio de sesión de TS y se cambió el nombre del Agente de sesión de Terminal Services (TS Session Broker). Además de mantener un directorio de sesiones existentes, TS Session Broker también puede intermediar las conexiones entrantes. Cuando el Agente de sesión de TS recibe una conexión entrante de un usuario, comprueba su base de datos para determinar si el usuario tiene una sesión existente en un servidor terminal. Si es así, el Agente de sesión de TS redirige la conexión a ese mismo servidor de terminal Server. Si no es así, TS Session Broker determina qué servidor de terminal server tiene el menor número de conexiones y redirige la conexión a ese servidor.

A partir de Windows Server 2008, Microsoft también publicó una interfaz de programación de aplicaciones (API) pública para supervisar e interactuar con sesiones en servidores de terminal Server. Esta API se describe en Conexión a Escritorio remoto [referencia del complemento de Broker](/windows/desktop/TermServ/terminal-services-virtualization-api-reference). Con esta API, los desarrolladores pueden crear complementos de directiva personalizados que invalide la lógica de redireccionamiento estándar de TS Session Broker. Los complementos personalizados pueden redirigir las sesiones a los servidores de terminal, así como a máquinas virtuales, escritorios virtuales, servidores de hoja y escritorios físicos.

En Windows Server 2008 R2, la arquitectura de Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto) (anteriormente conocido como Agente de sesión de TS) se expandió para admitir conexiones a máquinas virtuales. La nueva arquitectura admite la administración de sesiones para máquinas virtuales a través de Escritorio remoto Virtualization API. Los desarrolladores pueden usar esta API para personalizar la lógica que usa el Agente de conexión a Escritorio remoto para determinar el mejor destino para una conexión de cliente entrante.

Escritorio remoto Virtualization API ofrece varias ventajas a los desarrolladores:

-   Las interfaces para trabajar con servidores de terminal físicos son similares a las de trabajar con máquinas virtuales.
-   Los desarrolladores pueden reemplazar todo o parte de la lógica de redireccionamiento estándar. Los desarrolladores pueden compilar en el código que se incluye con el producto y no tienen que escribir todo desde cero.
-   No se requiere ningún agente de administración adicional en el servidor de administración o dentro de la sesión.
-   Todavía se admiten los complementos de TS Session Broker desarrollados para su uso Windows Server 2008.
-   La API también permite a los desarrolladores crear interfaces de usuario para la administración de servidores de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) (anteriormente conocidos como "servidores de terminal") y máquinas virtuales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritorio remoto de Virtualization API](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[Conexión a Escritorio remoto broker Plug-in Reference](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 