---
description: Cuando se habilitan Terminal Services, GINA debe llamar a las funciones de compatibilidad con Winlogon para completar la instalación de cada usuario, consultar las credenciales de una sesión de cliente Terminal Services y desconectarse de una sesión de red Terminal Services. Nota las dll de GINA se omiten en Windows Vista.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Terminal Services funciones GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907865"
---
# <a name="terminal-services-gina-functions"></a><span data-ttu-id="615a4-103">Terminal Services funciones GINA</span><span class="sxs-lookup"><span data-stu-id="615a4-103">Terminal Services GINA Functions</span></span>

<span data-ttu-id="615a4-104">Cuando se habilitan Terminal Services, [*Gina*](../secgloss/g-gly.md) debe llamar a las funciones de compatibilidad con [*Winlogon*](../secgloss/w-gly.md) para completar la instalación de cada usuario, consultar las [*credenciales*](../secgloss/c-gly.md) de una sesión de cliente Terminal Services y desconectarse de una sesión de red Terminal Services.</span><span class="sxs-lookup"><span data-stu-id="615a4-104">When Terminal Services are enabled, the [*GINA*](../secgloss/g-gly.md) must call [*Winlogon*](../secgloss/w-gly.md) support functions to complete the setup for each user, to query the [*credentials*](../secgloss/c-gly.md) of a Terminal Services client session, and to disconnect from a Terminal Services network session.</span></span>

> [!Note]  
> <span data-ttu-id="615a4-105">Los archivos dll de GINA se omiten en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="615a4-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="615a4-106">Estas funciones de compatibilidad incluyen lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="615a4-106">These support functions include the following.</span></span>



| <span data-ttu-id="615a4-107">Función</span><span class="sxs-lookup"><span data-stu-id="615a4-107">Function</span></span>                                                                     | <span data-ttu-id="615a4-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="615a4-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="615a4-109">**WlxWin31Migrate**</span><span class="sxs-lookup"><span data-stu-id="615a4-109">**WlxWin31Migrate**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | <span data-ttu-id="615a4-110">Completa la instalación del usuario.</span><span class="sxs-lookup"><span data-stu-id="615a4-110">Completes the setup of the user.</span></span>                                                                    |
| [<span data-ttu-id="615a4-111">**WlxQueryClientCredentials**</span><span class="sxs-lookup"><span data-stu-id="615a4-111">**WlxQueryClientCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | <span data-ttu-id="615a4-112">Se llama para consultar las credenciales de clientes remotos que no usan una licencia de conector de Internet.</span><span class="sxs-lookup"><span data-stu-id="615a4-112">Called to query the credentials of remote clients that are not using an Internet connector license.</span></span> |
| [<span data-ttu-id="615a4-113">**WlxQueryInetConnectorCredentials**</span><span class="sxs-lookup"><span data-stu-id="615a4-113">**WlxQueryInetConnectorCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | <span data-ttu-id="615a4-114">Se llama para consultar las credenciales de clientes remotos que usan una licencia de conector de Internet.</span><span class="sxs-lookup"><span data-stu-id="615a4-114">Called to query the credentials of remote clients that are using an Internet connector license.</span></span>     |
| [<span data-ttu-id="615a4-115">**WlxQueryTerminalServicesData**</span><span class="sxs-lookup"><span data-stu-id="615a4-115">**WlxQueryTerminalServicesData**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | <span data-ttu-id="615a4-116">Se llama para recuperar Terminal Services información de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="615a4-116">Called to retrieve Terminal Services user configuration information.</span></span>                                |
| [<span data-ttu-id="615a4-117">**WlxDisconnect**</span><span class="sxs-lookup"><span data-stu-id="615a4-117">**WlxDisconnect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | <span data-ttu-id="615a4-118">Se llama para desconectarse de una sesión de red Terminal Services.</span><span class="sxs-lookup"><span data-stu-id="615a4-118">Called to disconnect from a Terminal Services network session.</span></span>                                      |



 

<span data-ttu-id="615a4-119">Para tener acceso a estas funciones de compatibilidad con Winlogon, el archivo DLL de GINA debe usar la estructura [**WLX \_ Dispatch \_ versión \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) .</span><span class="sxs-lookup"><span data-stu-id="615a4-119">In order to access these Winlogon support functions, the GINA DLL must use the [**WLX\_DISPATCH\_VERSION\_1\_3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) structure.</span></span> <span data-ttu-id="615a4-120">En la función [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) de Gina, ambos parámetros deben ser al menos WLX \_ versión \_ 1 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="615a4-120">In the GINA's [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) function, both parameters must be at least WLX\_VERSION\_1\_3.</span></span>

 

 
