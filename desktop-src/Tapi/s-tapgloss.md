---
description: Los siguientes términos son útiles para comprender la tecnología de TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b4256a4a-c19e-4431-b62f-9e9fef4b5827
title: S (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f33f4d2c16110ad6c79a02401c6a63ad0fb8f4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689549"
---
# <a name="s-telephony-api"></a><span data-ttu-id="8b266-103">S (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="8b266-103">S (Telephony API)</span></span>

<span data-ttu-id="8b266-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N o [p](p-tapgloss.md) Q [R](r-tapgloss.md) s [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="8b266-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="8b266-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="8b266-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**service provider**</span></span>
</dt> <dd>

<span data-ttu-id="8b266-106">Biblioteca de vínculos dinámicos que admite las comunicaciones a través de una red telefónica a través de un conjunto de funciones de servicio exportadas.</span><span class="sxs-lookup"><span data-stu-id="8b266-106">A dynamic-link library that supports communications over a telephone network through a set of exported service functions.</span></span> <span data-ttu-id="8b266-107">El proveedor de servicios responde a las solicitudes de telefonía, enviadas por la biblioteca de vínculos dinámicos TAPI, llevando a cabo las tareas de bajo nivel necesarias para comunicarse a través de la red telefónica.</span><span class="sxs-lookup"><span data-stu-id="8b266-107">The service provider responds to telephony requests, sent to it by the TAPI dynamic-link library, by carrying out the low-level tasks necessary to communicate over the telephone network.</span></span> <span data-ttu-id="8b266-108">De esta manera, el proveedor de servicios, junto con TAPI, protege las aplicaciones de los detalles dependientes de la tecnología y del servicio de la comunicación de red telefónica.</span><span class="sxs-lookup"><span data-stu-id="8b266-108">In this way, the service provider, in conjunction with TAPI, shields applications from the service- and technology-dependent details of the telephone network communication.</span></span>

</dd> <dt>

<span data-ttu-id="8b266-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**Subdirección**</span><span class="sxs-lookup"><span data-stu-id="8b266-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**subaddressing**</span></span>
</dt> <dd>

<span data-ttu-id="8b266-110">Funcionalidad proporcionada en líneas ISDN (RDSI) que permite obtener más información que un único número de teléfono que se va a usar al marcar.</span><span class="sxs-lookup"><span data-stu-id="8b266-110">A capability provided on ISDN lines that allows more information than just a single telephone number to be used when dialing.</span></span>

</dd> <dt>

<span data-ttu-id="8b266-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Telefonía complementaria**</span><span class="sxs-lookup"><span data-stu-id="8b266-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Supplementary Telephony**</span></span>
</dt> <dd>

<span data-ttu-id="8b266-112">Nivel de servicio que proporciona características avanzadas de conmutador, como la retención, la transferencia, etc.</span><span class="sxs-lookup"><span data-stu-id="8b266-112">Level of service that provides advanced switch features such as hold, transfer, and so on.</span></span> <span data-ttu-id="8b266-113">Todos los servicios complementarios son opcionales; es decir, no es necesario que el proveedor de servicios las admita.</span><span class="sxs-lookup"><span data-stu-id="8b266-113">All supplementary services are optional; that is, the service provider is not required to support them.</span></span> <span data-ttu-id="8b266-114">Consulte [*telefonía asistida*](a-tapgloss.md), [*telefonía básica*](b-tapgloss.md)y [*telefonía extendida*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span><span class="sxs-lookup"><span data-stu-id="8b266-114">See [*Assisted Telephony*](a-tapgloss.md), [*Basic Telephony*](b-tapgloss.md), [*Extended Telephony*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span></span>

</dd> <dt>

<span data-ttu-id="8b266-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Cambiado 56**</span><span class="sxs-lookup"><span data-stu-id="8b266-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Switched 56**</span></span>
</dt> <dd>

<span data-ttu-id="8b266-116">Un servicio de datos conmutado que permite al usuario marcar a otra persona y transmitir a través de una llamada de teléfono a 56 kbps digitales sincrónicos digitales.</span><span class="sxs-lookup"><span data-stu-id="8b266-116">A switched data service that lets the user dial someone else and transmit at full duplex, digital synchronous 56 Kbps for the price of a phone call.</span></span>

</dd> <dt>

<span data-ttu-id="8b266-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**sincrónica**</span><span class="sxs-lookup"><span data-stu-id="8b266-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**synchronous**</span></span>
</dt> <dd>

<span data-ttu-id="8b266-118">Método de transmisión de datos en el que hay tiempo constante entre bits, caracteres o eventos sucesivos.</span><span class="sxs-lookup"><span data-stu-id="8b266-118">Data transmission method in which there is constant time between successive bits, characters, or events.</span></span> <span data-ttu-id="8b266-119">El tiempo se consigue mediante el uso compartido de un solo reloj.</span><span class="sxs-lookup"><span data-stu-id="8b266-119">The timing is achieved by the sharing of a single clock.</span></span> <span data-ttu-id="8b266-120">Cada extremo de la transmisión se sincroniza con el uso de relojes e información enviada junto con los datos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="8b266-120">Each end of the transmission synchronizes itself with the use of clocks and information sent along with the transmitted data.</span></span> <span data-ttu-id="8b266-121">Los caracteres se espacian por tiempo, no por bits de inicio y detención.</span><span class="sxs-lookup"><span data-stu-id="8b266-121">Characters are spaced by time, not by start and stop bits.</span></span> <span data-ttu-id="8b266-122">Vea [*asincrónica*](a-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="8b266-122">See [*asynchronous*](a-tapgloss.md).</span></span>

</dd> </dl>

 

 



