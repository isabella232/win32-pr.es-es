---
title: Trabajar con unidades de datos de protocolo
description: El Protocolo simple de administración de redes (SNMP) envía solicitudes de operación y respuestas como mensajes SNMP.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Trabajar con unidades de datos de protocolo SNMP
- Unidades de datos de protocolo SNMP, trabajar con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076041"
---
# <a name="working-with-protocol-data-units"></a><span data-ttu-id="6f76d-105">Trabajar con unidades de datos de protocolo</span><span class="sxs-lookup"><span data-stu-id="6f76d-105">Working with Protocol Data Units</span></span>

<span data-ttu-id="6f76d-106">El Protocolo simple de administración de redes (SNMP) envía solicitudes de operación y respuestas como mensajes SNMP.</span><span class="sxs-lookup"><span data-stu-id="6f76d-106">The Simple Network Management Protocol (SNMP) sends operation requests and responses as SNMP messages.</span></span> <span data-ttu-id="6f76d-107">Un mensaje SNMP es una unidad de datos de protocolo SNMP (PDU) más elementos de encabezado de mensaje adicionales definidos por la RFC correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6f76d-107">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="6f76d-108">Una PDU incluye una lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="6f76d-108">A PDU includes a variable binding list.</span></span>

<span data-ttu-id="6f76d-109">La estructura de una PDU está restringida a la implementación de Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="6f76d-109">The structure of a PDU is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="6f76d-110">Una aplicación WinSNMP puede tener acceso a una PDU con un identificador del **tipo \_ PDU HSNMP**.</span><span class="sxs-lookup"><span data-stu-id="6f76d-110">A WinSNMP application can access a PDU with a handle of the type **HSNMP\_PDU**.</span></span> <span data-ttu-id="6f76d-111">La aplicación WinSNMP debe crear una PDU antes de llamar a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) o a la función [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .</span><span class="sxs-lookup"><span data-stu-id="6f76d-111">The WinSNMP application must create a PDU before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function.</span></span>

<span data-ttu-id="6f76d-112">La aplicación puede extraer y actualizar los elementos de datos de una PDU y liberar los recursos asignados para las PDU.</span><span class="sxs-lookup"><span data-stu-id="6f76d-112">The application can extract and update the data elements of a PDU, and release resources allocated for PDUs.</span></span> <span data-ttu-id="6f76d-113">Para realizar estas operaciones, la aplicación usa las [funciones de PDU](winsnmp-functions.md)WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="6f76d-113">To perform these operations, the application uses the WinSNMP [PDU functions](winsnmp-functions.md).</span></span> <span data-ttu-id="6f76d-114">En la tabla siguiente se enumeran los temas en los que se explica cómo trabajar con PDU en el entorno de programación WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="6f76d-114">The following table lists topics that discuss working with PDUs in the WinSNMP programming environment.</span></span>



| <span data-ttu-id="6f76d-115">Tema</span><span class="sxs-lookup"><span data-stu-id="6f76d-115">Topic</span></span>                                                                        | <span data-ttu-id="6f76d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f76d-116">Description</span></span>                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="6f76d-117">Creación de una PDU</span><span class="sxs-lookup"><span data-stu-id="6f76d-117">Creating a PDU</span></span>](creating-a-pdu.md)                                         | <span data-ttu-id="6f76d-118">Describe cómo crear una PDU.</span><span class="sxs-lookup"><span data-stu-id="6f76d-118">Describes how to create a PDU.</span></span>                                     |
| [<span data-ttu-id="6f76d-119">Actualización de una PDU</span><span class="sxs-lookup"><span data-stu-id="6f76d-119">Updating a PDU</span></span>](updating-a-pdu.md)                                         | <span data-ttu-id="6f76d-120">Describe cómo recuperar y actualizar los campos de PDU.</span><span class="sxs-lookup"><span data-stu-id="6f76d-120">Describes how to retrieve and update PDU fields.</span></span>                   |
| [<span data-ttu-id="6f76d-121">Duplicación de una PDU</span><span class="sxs-lookup"><span data-stu-id="6f76d-121">Duplicating a PDU</span></span>](duplicating-a-pdu.md)                                   | <span data-ttu-id="6f76d-122">Describe cómo duplicar una PDU.</span><span class="sxs-lookup"><span data-stu-id="6f76d-122">Describes how to duplicate a PDU.</span></span>                                  |
| [<span data-ttu-id="6f76d-123">Validación de una PDU</span><span class="sxs-lookup"><span data-stu-id="6f76d-123">Validating a PDU</span></span>](validating-a-pdu.md)                                     | <span data-ttu-id="6f76d-124">Describe la validación de una PDU.</span><span class="sxs-lookup"><span data-stu-id="6f76d-124">Describes the validation of a PDU.</span></span>                                 |
| [<span data-ttu-id="6f76d-125">Respuesta coincidente y solicitud de PDU</span><span class="sxs-lookup"><span data-stu-id="6f76d-125">Matching Response and Request PDUs</span></span>](matching-response-and-request-pdus.md) | <span data-ttu-id="6f76d-126">Describe el proceso de coincidencia de una PDU de respuesta con una PDU de solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f76d-126">Describes the process of matching a response PDU to a request PDU.</span></span> |



 

<span data-ttu-id="6f76d-127">Para obtener más información, vea [trabajar con listas de enlaces de variables](working-with-variable-binding-lists.md) y objetos de identificador de [recursos](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6f76d-127">For more information, see [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Resource Handle Objects](resource-handle-objects.md).</span></span>

 

 




