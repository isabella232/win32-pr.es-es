---
description: La instalación de un nuevo proveedor de servicios es muy específica del dispositivo y del sistema operativo, por lo que los detalles están fuera del ámbito de este SDK.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Instalación e inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688416"
---
# <a name="installation-and-initialization"></a><span data-ttu-id="5d069-103">Instalación e inicialización</span><span class="sxs-lookup"><span data-stu-id="5d069-103">Installation and Initialization</span></span>

<span data-ttu-id="5d069-104">La instalación de un nuevo proveedor de servicios es muy específica del dispositivo y del sistema operativo, por lo que los detalles están fuera del ámbito de este SDK.</span><span class="sxs-lookup"><span data-stu-id="5d069-104">Installation of a new service provider is highly device- and operating-system-specific, so the details are outside the scope of this SDK.</span></span> <span data-ttu-id="5d069-105">En general, el objetivo de la instalación es la configuración del proveedor de servicios para el entorno de comunicaciones actual.</span><span class="sxs-lookup"><span data-stu-id="5d069-105">Generally speaking, the goal of installation is configuration of the service provider for the current communications environment.</span></span> <span data-ttu-id="5d069-106">Normalmente, esto implica las entradas del registro y la configuración de las dependencias del servicio.</span><span class="sxs-lookup"><span data-stu-id="5d069-106">This usually involves registry entries and the setting of service dependencies.</span></span>

<span data-ttu-id="5d069-107">La inicialización de un proveedor de servicios de telefonía comienza con la negociación de la versión.</span><span class="sxs-lookup"><span data-stu-id="5d069-107">Initialization of a telephony service provider starts with version negotiation.</span></span> <span data-ttu-id="5d069-108">Vea [control de versiones de TSPI](tspi-versioning.md) para obtener una explicación de la negociación de la versión y la versión actual.</span><span class="sxs-lookup"><span data-stu-id="5d069-108">See [TSPI Versioning](tspi-versioning.md) for a discussion of version negotiation and current version.</span></span>

<span data-ttu-id="5d069-109">A continuación, TAPI llama a [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), que pasa al proveedor un puntero a una función de devolución de llamada que se usa para informar sobre el progreso de las funciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="5d069-109">TAPI then calls [**TSPI\_providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), which passes the provider a pointer to a callback function used to report on asynchronous functions progress.</span></span> <span data-ttu-id="5d069-110">El TSP devuelve un recuento de dispositivos de línea y teléfono asociados al identificador de dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="5d069-110">The TSP returns a count of line and phone devices associated with the current device identifier.</span></span>

<span data-ttu-id="5d069-111">Normalmente, el siguiente paso será el inventario de recursos, realizado por TAPI al invocar [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) y [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span><span class="sxs-lookup"><span data-stu-id="5d069-111">Typically, the next step will be resource inventory, conducted by TAPI invoking [**TSPI\_lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) and [**TSPI\_lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span></span> <span data-ttu-id="5d069-112">Se espera que el proveedor de servicios rellene los elementos de las estructuras de datos implicados que pertenecen a las capacidades de sesión y dispositivo que admite.</span><span class="sxs-lookup"><span data-stu-id="5d069-112">The service provider is expected to fill in those elements of the data structures involved that pertain to device and session capabilities it supports.</span></span>

<span data-ttu-id="5d069-113">TAPI recopila información de las distintas aplicaciones relativas a los requisitos de notificación de eventos e indica a TSP que use [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) para indicar qué tipos de medios se deben detectar para una línea y [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) para indicar qué eventos de línea y dirección se deben notificar.</span><span class="sxs-lookup"><span data-stu-id="5d069-113">TAPI collects information from the various applications concerning event notification requirements, and instructs the TSP using [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) to indicate which media types to detect for a line and [**TSPI\_lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) to indicate which line and address events should be reported.</span></span>

 

 
