---
title: Formatos de captura
description: El formato de las PDU de captura es diferente del de otras PDU. El formato de las capturas de SNMPv1 y las capturas de SNMPv2C también es diferente.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075377"
---
# <a name="trap-formats"></a><span data-ttu-id="6f9a3-104">Formatos de captura</span><span class="sxs-lookup"><span data-stu-id="6f9a3-104">Trap Formats</span></span>

<span data-ttu-id="6f9a3-105">El formato de las PDU de captura es diferente del de otras PDU.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-105">The format of trap PDUs is different than that of other PDUs.</span></span> <span data-ttu-id="6f9a3-106">El formato de las capturas de SNMPv1 y las capturas de SNMPv2C también es diferente.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-106">The format of SNMPv1 traps and SNMPv2C traps is also different.</span></span>

<span data-ttu-id="6f9a3-107">En el marco de SNMPv2C, el formato de reventado de PDU es una lista de enlaces variables de *n* entradas de enlace variable organizadas de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6f9a3-107">Under the SNMPv2C framework, the PDU trap format is a variable binding list of *n* variable binding entries organized in the following manner:</span></span>

-   <span data-ttu-id="6f9a3-108">La primera entrada de enlace de variable contiene una marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-108">The first variable binding entry contains a time-stamp.</span></span>
-   <span data-ttu-id="6f9a3-109">La segunda entrada de enlace de variables es un identificador de objeto que identifica la captura.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-109">The second variable binding entry is an object identifier that identifies the trap.</span></span>
-   <span data-ttu-id="6f9a3-110">Las demás entradas de enlace de variables, si están presentes, contienen información adicional *asociada a la* captura.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-110">The third through *n* variable binding entries, if present, contain additional information associated with the trap.</span></span>

<span data-ttu-id="6f9a3-111">En la plataforma SNMPv1, el formato de la captura PDU es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-111">Under the SNMPv1 framework, the PDU trap format is as follows.</span></span>

| <span data-ttu-id="6f9a3-112">Campo</span><span class="sxs-lookup"><span data-stu-id="6f9a3-112">Field</span></span>                      | <span data-ttu-id="6f9a3-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f9a3-113">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6f9a3-114">empresa</span><span class="sxs-lookup"><span data-stu-id="6f9a3-114">enterprise</span></span>                 | <span data-ttu-id="6f9a3-115">Identifica el tipo de dispositivo que generó la captura.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-115">Identifies the type of device that generated the trap.</span></span>           |
| <span data-ttu-id="6f9a3-116">Agent-addr</span><span class="sxs-lookup"><span data-stu-id="6f9a3-116">agent-addr</span></span>                 | <span data-ttu-id="6f9a3-117">Identifica la dirección IP del dispositivo que generó la captura.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-117">Identifies the IP address of the device that generated the trap.</span></span> |
| <span data-ttu-id="6f9a3-118">captura de tipos genéricos y de captura específica</span><span class="sxs-lookup"><span data-stu-id="6f9a3-118">generic-trap/specific-trap</span></span> | <span data-ttu-id="6f9a3-119">Identifica un tipo de captura predefinido.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-119">Identifies a predefined trap type.</span></span>                               |
| <span data-ttu-id="6f9a3-120">marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="6f9a3-120">time-stamp</span></span>                 | <span data-ttu-id="6f9a3-121">Identifica Cuándo se generó la captura.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-121">Identifies when the trap was generated.</span></span>                          |
| <span data-ttu-id="6f9a3-122">enlaces de variables</span><span class="sxs-lookup"><span data-stu-id="6f9a3-122">variable-bindings</span></span>          | <span data-ttu-id="6f9a3-123">Contiene información adicional asociada a la captura.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-123">Contains additional information associated with the trap.</span></span>        |



 

<span data-ttu-id="6f9a3-124">La función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) siempre devuelve un mensaje en el formato SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-124">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function always returns a message in the SNMPv2C format.</span></span> <span data-ttu-id="6f9a3-125">Si el mensaje contiene el tipo de **operación \_ \_ captura de PDU de SNMP**, la aplicación puede leer las entradas de enlace de variables del mensaje y recuperar la información asociada a la captura.</span><span class="sxs-lookup"><span data-stu-id="6f9a3-125">If the message contains the operation type **SNMP\_PDU\_TRAP**, the application can read the variable binding entries of the message and retrieve the information associated with the trap.</span></span>

 

 




