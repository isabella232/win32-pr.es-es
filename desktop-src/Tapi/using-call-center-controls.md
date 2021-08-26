---
description: Los controles de centro de llamadas amplían el modelo de objetos TAPI 3 para admitir los requisitos de los sistemas de distribución automática de llamadas (ACD).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Uso de controles de centro de llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f166658cce86faa0003b762ec697286a434a06b36b18ae92a861d1f6757fa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991545"
---
# <a name="using-call-center-controls"></a>Uso de controles de centro de llamadas

Los controles de centro de llamadas amplían el modelo de objetos TAPI 3 para admitir los requisitos de los sistemas de distribución automática de llamadas (ACD). Un centro de llamadas es una ubicación con agentes u operadores en los bancos de teléfonos, ya sea realizando llamadas telefónicas salientes o realizando llamadas entrantes de campo. Por ejemplo, un banco o una empresa de tarjetas de crédito usará un centro de llamadas para procesar las consultas de cuentas.

Las aplicaciones del centro de llamadas se dividen en tres tipos básicos:

-   [Proxy de ACD:](acd-proxy.md)controla las sesiones entrantes o salientes en el servidor, que pueden ser cualquier cosa, desde un conmutador telefónico propietario a una puerta de enlace de Internet.
-   [Cliente del agente de ACD:](acd-agent-client.md)proporciona servicios a un agente individual que recibe o realiza llamadas.
-   Cliente de supervisor de ACD: proporciona una vista general de las operaciones de agente y ACD.

> [!Note]  
> Para Windows 2000, la funcionalidad de proxy está disponible mediante TAPI 2.2 y las funciones de supervisor no se implementan.

 

La sección de ejemplos del SDK de Windows contiene ejemplos de código de ACD en Netds \\ \\ Tapi Tapi2 Acd y \\ Netds \\ Tapi \\ Tapi3 \\ Acd.

 

 



