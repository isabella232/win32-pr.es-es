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
# <a name="using-call-center-controls"></a><span data-ttu-id="20edf-103">Usar controles de centro de llamadas</span><span class="sxs-lookup"><span data-stu-id="20edf-103">Using Call Center Controls</span></span>

<span data-ttu-id="20edf-104">Los controles del centro de llamadas amplían el modelo de objetos de TAPI 3 para admitir los requisitos de los sistemas de distribución automática de llamadas (ACD).</span><span class="sxs-lookup"><span data-stu-id="20edf-104">Call center controls extend the TAPI 3 object model to support the requirements of Automatic Call Distribution (ACD) systems.</span></span> <span data-ttu-id="20edf-105">Un centro de llamadas es una ubicación con agentes u operadores en los bancos de teléfonos que realizan llamadas telefónicas salientes o de campo entrantes.</span><span class="sxs-lookup"><span data-stu-id="20edf-105">A call center is a location with agents or operators at banks of telephones either making outgoing telephone calls or fielding incoming ones.</span></span> <span data-ttu-id="20edf-106">Por ejemplo, una empresa bancaria o de tarjeta de crédito usará un centro de llamadas para procesar las consultas de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="20edf-106">For example, a bank or credit card company will use a call center to process account inquiries.</span></span>

<span data-ttu-id="20edf-107">Las aplicaciones del centro de llamadas se dividen en tres tipos básicos:</span><span class="sxs-lookup"><span data-stu-id="20edf-107">Call center applications are divided into three basic types:</span></span>

-   <span data-ttu-id="20edf-108">[Proxy ACD](acd-proxy.md): controla las sesiones entrantes o salientes en el servidor, lo que puede ser cualquier cosa desde un conmutador de teléfono propietario a una puerta de enlace de Internet.</span><span class="sxs-lookup"><span data-stu-id="20edf-108">[ACD Proxy](acd-proxy.md): Handles incoming or outgoing sessions at the server, which can be anything from a proprietary telephone switch to an Internet gateway.</span></span>
-   <span data-ttu-id="20edf-109">[Cliente del agente ACD](acd-agent-client.md): servicios un agente individual que recibe o realiza llamadas.</span><span class="sxs-lookup"><span data-stu-id="20edf-109">[ACD Agent Client](acd-agent-client.md): Services an individual agent who is receiving or making calls.</span></span>
-   <span data-ttu-id="20edf-110">Cliente del supervisor de ACD: proporciona una vista general de las operaciones de agente y ACD.</span><span class="sxs-lookup"><span data-stu-id="20edf-110">ACD Supervisor Client: Provides an overall view of agent and ACD operations.</span></span>

> [!Note]  
> <span data-ttu-id="20edf-111">En Windows 2000, la funcionalidad de proxy está disponible con TAPI 2,2 y las funciones de supervisor no se implementan.</span><span class="sxs-lookup"><span data-stu-id="20edf-111">For Windows 2000, proxy functionality is available using TAPI 2.2, and supervisor functions are not implemented.</span></span>

 

<span data-ttu-id="20edf-112">La sección de ejemplos del Windows SDK contiene ejemplos de código ACD en Netds \\ TAPI \\ Tapi2 \\ ACD y Netds \\ TAPI \\ Tapi3 \\ ACD.</span><span class="sxs-lookup"><span data-stu-id="20edf-112">The samples section of the Windows SDK contains ACD code samples under Netds\\Tapi\\Tapi2\\Acd and Netds\\Tapi\\Tapi3\\Acd.</span></span>

 

 



