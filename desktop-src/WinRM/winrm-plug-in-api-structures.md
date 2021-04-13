---
title: Estructuras de la API del complemento de WinRM
description: Estructuras de la API del complemento de WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357423"
---
# <a name="winrm-plug-in-api-structures"></a><span data-ttu-id="a678e-103">Estructuras de la API del complemento de WinRM</span><span class="sxs-lookup"><span data-stu-id="a678e-103">WinRM Plug-in API Structures</span></span>

<span data-ttu-id="a678e-104">En la tabla siguiente se proporciona información general sobre las estructuras de la interfaz de programación de aplicaciones (API) de complementos de Administración remota de Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="a678e-104">The following table provides an overview of the structures in the Windows Remote Management (WinRM) plug-in application programming interface (API).</span></span>



| <span data-ttu-id="a678e-105">Estructura</span><span class="sxs-lookup"><span data-stu-id="a678e-105">Structure</span></span>                                                        | <span data-ttu-id="a678e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a678e-106">Description</span></span>                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a678e-107">**cuota de WSMAN \_ AUTHZ \_**</span><span class="sxs-lookup"><span data-stu-id="a678e-107">**WSMAN\_AUTHZ\_QUOTA**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | <span data-ttu-id="a678e-108">Define la información de cuota por usuario.</span><span class="sxs-lookup"><span data-stu-id="a678e-108">Defines quota information on a per-user basis.</span></span>                                           |
| [<span data-ttu-id="a678e-109">**\_detalles del certificado WSMAN \_**</span><span class="sxs-lookup"><span data-stu-id="a678e-109">**WSMAN\_CERTIFICATE\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | <span data-ttu-id="a678e-110">Representa los campos en el certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="a678e-110">Represents the fields within the client certificate.</span></span>                                     |
| [<span data-ttu-id="a678e-111">**\_conjunto de \_ argumentos del comando WSMAN \_**</span><span class="sxs-lookup"><span data-stu-id="a678e-111">**WSMAN\_COMMAND\_ARG\_SET**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | <span data-ttu-id="a678e-112">Representa el conjunto de argumentos que se pasan a la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a678e-112">Represents the set of arguments that are passed in to the command line.</span></span>                  |
| [<span data-ttu-id="a678e-113">**\_filtro WSMAN**</span><span class="sxs-lookup"><span data-stu-id="a678e-113">**WSMAN\_FILTER**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | <span data-ttu-id="a678e-114">Define el filtrado utilizado para una operación.</span><span class="sxs-lookup"><span data-stu-id="a678e-114">Defines the filtering used for an operation.</span></span>                                             |
| [<span data-ttu-id="a678e-115">**\_fragmento WSMAN**</span><span class="sxs-lookup"><span data-stu-id="a678e-115">**WSMAN\_FRAGMENT**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | <span data-ttu-id="a678e-116">Define la información de fragmento para una operación.</span><span class="sxs-lookup"><span data-stu-id="a678e-116">Defines the fragment information for an operation.</span></span>                                       |
| [<span data-ttu-id="a678e-117">**información de la \_ operación WSMAN \_**</span><span class="sxs-lookup"><span data-stu-id="a678e-117">**WSMAN\_OPERATION\_INFO**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | <span data-ttu-id="a678e-118">Representa un punto de conexión de recurso específico para el que el complemento debe realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a678e-118">Represents a specific resource end-point for which the plug-in must perform the request.</span></span> |
| [<span data-ttu-id="a678e-119">**\_solicitud de complemento WSMAN \_**</span><span class="sxs-lookup"><span data-stu-id="a678e-119">**WSMAN\_PLUGIN\_REQUEST**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | <span data-ttu-id="a678e-120">Contiene información sobre la solicitud y se pasa a cada operación de complemento.</span><span class="sxs-lookup"><span data-stu-id="a678e-120">Contains information about the request and is passed into every plug-in operation.</span></span>       |
| [<span data-ttu-id="a678e-121">**detalles del remitente de WSMAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a678e-121">**WSMAN\_SENDER\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | <span data-ttu-id="a678e-122">Especifica los detalles del cliente para cada solicitud de entrada.</span><span class="sxs-lookup"><span data-stu-id="a678e-122">Specifies client details for every inbound request.</span></span>                                      |



 

 

 




