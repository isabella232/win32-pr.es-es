---
description: Los controles del centro de llamadas amplían el modelo de objetos de TAPI 3 para admitir los requisitos de los sistemas de distribución automática de llamadas (ACD).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Usar controles de centro de llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687124"
---
# <a name="using-call-center-controls"></a>Usar controles de centro de llamadas

Los controles del centro de llamadas amplían el modelo de objetos de TAPI 3 para admitir los requisitos de los sistemas de distribución automática de llamadas (ACD). Un centro de llamadas es una ubicación con agentes u operadores en los bancos de teléfonos que realizan llamadas telefónicas salientes o de campo entrantes. Por ejemplo, una empresa bancaria o de tarjeta de crédito usará un centro de llamadas para procesar las consultas de la cuenta.

Las aplicaciones del centro de llamadas se dividen en tres tipos básicos:

-   [Proxy ACD](acd-proxy.md): controla las sesiones entrantes o salientes en el servidor, lo que puede ser cualquier cosa desde un conmutador de teléfono propietario a una puerta de enlace de Internet.
-   [Cliente del agente ACD](acd-agent-client.md): servicios un agente individual que recibe o realiza llamadas.
-   Cliente del supervisor de ACD: proporciona una vista general de las operaciones de agente y ACD.

> [!Note]  
> En Windows 2000, la funcionalidad de proxy está disponible con TAPI 2,2 y las funciones de supervisor no se implementan.

 

La sección de ejemplos del Windows SDK contiene ejemplos de código ACD en Netds \\ TAPI \\ Tapi2 \\ ACD y Netds \\ TAPI \\ Tapi3 \\ ACD.

 

 



