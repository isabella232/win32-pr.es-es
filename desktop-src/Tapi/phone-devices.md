---
description: La compatibilidad con dispositivos telefónicos es complementaria en lugar de básica, por lo que no es necesario que los proveedores de servicios admitan dispositivos telefónicos.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Dispositivos telefónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001316"
---
# <a name="phone-devices"></a><span data-ttu-id="171eb-103">Dispositivos telefónicos</span><span class="sxs-lookup"><span data-stu-id="171eb-103">Phone Devices</span></span>

<span data-ttu-id="171eb-104">La compatibilidad con dispositivos telefónicos es complementaria en lugar de básica, por lo que no es necesario que los proveedores de servicios admitan dispositivos telefónicos.</span><span class="sxs-lookup"><span data-stu-id="171eb-104">Phone device support is supplementary rather than basic, so service providers are not required to support phone devices.</span></span>

<span data-ttu-id="171eb-105">Del mismo modo que una clase de dispositivo de línea es una abstracción de un dispositivo de línea física, la clase de dispositivo telefónico representa una abstracción independiente del dispositivo de un juego de teléfono.</span><span class="sxs-lookup"><span data-stu-id="171eb-105">Just as a line device class is an abstraction of a physical line device, the phone device class represents a device-independent abstraction of a telephone set.</span></span> <span data-ttu-id="171eb-106">TAPI trata los dispositivos de línea y teléfono como dispositivos que son independientes entre sí.</span><span class="sxs-lookup"><span data-stu-id="171eb-106">TAPI treats line and phone devices as devices that are independent of each other.</span></span> <span data-ttu-id="171eb-107">En otras palabras, puede usar un teléfono (dispositivo) sin usar una línea asociada, y puede usar una línea (dispositivo) sin usar un teléfono.</span><span class="sxs-lookup"><span data-stu-id="171eb-107">In other words, you can use a phone (device) without using an associated line, and you can use a line (device) without using a phone.</span></span>

<span data-ttu-id="171eb-108">Los proveedores de servicios que implementan totalmente esta independencia pueden ofrecer usos para estos dispositivos no definidos por los protocolos de telefonía tradicionales.</span><span class="sxs-lookup"><span data-stu-id="171eb-108">Service providers that fully implement this independence can offer uses for these devices not defined by traditional telephony protocols.</span></span> <span data-ttu-id="171eb-109">Por ejemplo, una persona puede usar el auricular del teléfono del escritorio como dispositivo de audio de forma de onda para grabar o reproducir voz, quizás sin la información del conmutador de que el teléfono está en uso.</span><span class="sxs-lookup"><span data-stu-id="171eb-109">For example, a person can use the handset of the desktop's phone as a waveform audio device for voice recording or playback, perhaps without the switch's knowledge that the phone is in use.</span></span> <span data-ttu-id="171eb-110">En este tipo de implementación, levantar el auricular del teléfono local no debe enviar automáticamente una señal OffHook al conmutador.</span><span class="sxs-lookup"><span data-stu-id="171eb-110">In such an implementation, lifting the local phone handset need not automatically send an offhook signal to the switch.</span></span>

<span data-ttu-id="171eb-111">Esta independencia también permite que una aplicación suene el teléfono local de forma independiente de las llamadas entrantes.</span><span class="sxs-lookup"><span data-stu-id="171eb-111">This independence also allows an application to ring the local telephone in a manner that is independent of incoming calls.</span></span> <span data-ttu-id="171eb-112">Las capacidades de los proveedores de servicios están limitadas por las capacidades del hardware y el software que se usan para interconectar el conmutador, el teléfono y el equipo.</span><span class="sxs-lookup"><span data-stu-id="171eb-112">The capabilities of service providers are limited by the capabilities of the hardware and software used to interconnect the switch, the phone, and the computer.</span></span>

<span data-ttu-id="171eb-113">TAPI incluye funciones para recuperar funciones del dispositivo que permiten a los clientes determinar si se admite dicho modelo de uso.</span><span class="sxs-lookup"><span data-stu-id="171eb-113">TAPI includes functions to retrieve device capabilities that allow clients to determine whether such a usage model is supported.</span></span>

<span data-ttu-id="171eb-114">En esta sección se describen los dispositivos telefónicos y se explica cómo usar las funciones de teléfono TAPI para tener acceso a estos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="171eb-114">This section describes phone devices and explains how to use the TAPI phone functions to access these devices.</span></span>

-   [<span data-ttu-id="171eb-115">Dispositivo telefónico</span><span class="sxs-lookup"><span data-stu-id="171eb-115">Phone Device</span></span>](phone-device-elements.md)
-   [<span data-ttu-id="171eb-116">Inicialización y apagado</span><span class="sxs-lookup"><span data-stu-id="171eb-116">Initialization and Shutdown</span></span>](initialization-and-shutdown.md)

 

 



