---
description: Una red se ve como el mecanismo de transporte que transmite los datos de un punto a otro.
ms.assetid: 88374ac9-81c3-48c3-bf1a-5cfd734c257c
title: Red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d25f0c643ed1b54edb0ec45d47abfdc2f29fd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497740"
---
# <a name="network"></a><span data-ttu-id="90425-103">Red</span><span class="sxs-lookup"><span data-stu-id="90425-103">Network</span></span>

<span data-ttu-id="90425-104">Una red se ve como el mecanismo de transporte que transmite los datos de un punto a otro.</span><span class="sxs-lookup"><span data-stu-id="90425-104">A network is viewed as the transport mechanism that conveys data from one point to another.</span></span> <span data-ttu-id="90425-105">Los proveedores de servicios TAPI controlan los protocolos específicos necesarios para realizar operaciones como establecer una sesión de comunicaciones en una red determinada.</span><span class="sxs-lookup"><span data-stu-id="90425-105">TAPI service providers handle the specific protocols required to perform operations such as establishing a communications session on a given network.</span></span> <span data-ttu-id="90425-106">Normalmente, una aplicación de usuario final o servidor solo requiere información de red muy general, como el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="90425-106">An end-user or server application normally requires only very general network information, such as address type.</span></span>

<span data-ttu-id="90425-107">Algunos tipos comunes de redes:</span><span class="sxs-lookup"><span data-stu-id="90425-107">Some common types of networks:</span></span>

-   <span data-ttu-id="90425-108">**POTS (servicio telefónico anterior):** La voz y los datos se transmiten en formato analógico en el *bucle local* y se transmiten digitalmente en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="90425-108">**POTS (Plain Old Telephone Service):** Voice and data are transmitted in analog format while in the *local loop* and are digitally transmitted elsewhere.</span></span> <span data-ttu-id="90425-109">Normalmente, un tipo de medio por llamada, un canal por línea.</span><span class="sxs-lookup"><span data-stu-id="90425-109">Typically, one media type per call, one channel per line.</span></span>
-   <span data-ttu-id="90425-110">**ISDN (red digital de servicios integrados):** Transmitidos digitalmente.</span><span class="sxs-lookup"><span data-stu-id="90425-110">**ISDN (Integrated Services Digital Network):** Transmitted digitally.</span></span> <span data-ttu-id="90425-111">Velocidades de hasta 128 kbps en líneas de la interfaz de velocidad básica (BRI-ISDN) y mucho más alto en las líneas de la interfaz de velocidad principal (PRI-ISDN).</span><span class="sxs-lookup"><span data-stu-id="90425-111">Speeds of up to 128 Kbps on Basic Rate Interface (BRI-ISDN) lines and much higher on Primary Rate Interface (PRI-ISDN) lines.</span></span> <span data-ttu-id="90425-112">Al menos tres canales y hasta hasta 32 canales, para la transmisión simultánea y de voz y de datos.</span><span class="sxs-lookup"><span data-stu-id="90425-112">At least three channels and as many as 32 channels, for simultaneous, independently operated transmission of voice and data.</span></span> <span data-ttu-id="90425-113">Estándar internacional.</span><span class="sxs-lookup"><span data-stu-id="90425-113">International standard.</span></span>
-   <span data-ttu-id="90425-114">**T1/E1:** Transmitidos digitalmente.</span><span class="sxs-lookup"><span data-stu-id="90425-114">**T1/E1:** Transmitted digitally.</span></span> <span data-ttu-id="90425-115">T1 es un vínculo de transmisión con una capacidad de 1,544 Mbps, que se suele usar para conectar redes entre distancias remotas.</span><span class="sxs-lookup"><span data-stu-id="90425-115">T1 is a transmission link with a capacity of 1.544 Mbps, typically used for connecting networks across remote distances.</span></span> <span data-ttu-id="90425-116">En la Unión Europea T1 se denomina E1.</span><span class="sxs-lookup"><span data-stu-id="90425-116">In the European Union T1 is called E1.</span></span>
-   <span data-ttu-id="90425-117">**Cambiado 56:** Señalización a 56 kbps sobre líneas telefónicas de acceso telefónico, pero requiere equipos especiales.</span><span class="sxs-lookup"><span data-stu-id="90425-117">**Switched 56:** Signaling at 56 Kbps over dial-up telephone lines, but requires special equipment.</span></span> <span data-ttu-id="90425-118">Limitado a las llamadas a otras instalaciones especialmente equipadas.</span><span class="sxs-lookup"><span data-stu-id="90425-118">Limited to calls to other specially equipped facilities.</span></span>
-   <span data-ttu-id="90425-119">**Centrex:** Servicios de red centralizados mediante líneas de teléfono regulares y el uso de equipos de la compañía telefónica.</span><span class="sxs-lookup"><span data-stu-id="90425-119">**CENTREX:** Centralized network services through regular telephone lines and using telephone company equipment.</span></span> <span data-ttu-id="90425-120">No se requiere ningún equipo especial.</span><span class="sxs-lookup"><span data-stu-id="90425-120">No special equipment required.</span></span>
-   <span data-ttu-id="90425-121">**PBX digitales (intercambios de bifurcaciones privadas) y sistemas de claves:** Voz y datos transmitidos en sistemas telefónicos privados mediante interfaces de propiedad.</span><span class="sxs-lookup"><span data-stu-id="90425-121">**Digital PBXs (private branch exchanges) and key systems:** Voice and data transmitted on private telephone systems using proprietary interfaces.</span></span>
-   <span data-ttu-id="90425-122">**Redes IP:** Voz y datos transmitidos en redes mediante el protocolo de Internet (IP), como Internet o una intranet corporativa.</span><span class="sxs-lookup"><span data-stu-id="90425-122">**IP Networks:** Voice and data transmitted on networks using the Internet Protocol (IP), such as the Internet itself or a corporate intranet.</span></span>

<span data-ttu-id="90425-123">Ten en cuenta que no es una lista exhaustiva.</span><span class="sxs-lookup"><span data-stu-id="90425-123">Please note that this list is not exhaustive.</span></span> <span data-ttu-id="90425-124">Se puede admitir cualquier mecanismo de transporte de red, dados los proveedores de servicios adecuados.</span><span class="sxs-lookup"><span data-stu-id="90425-124">Any network transport mechanism can be supported, given appropriate service providers.</span></span>

 

 



