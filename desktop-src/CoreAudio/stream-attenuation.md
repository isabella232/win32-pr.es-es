---
description: Experiencia predeterminada de los patos
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Experiencia predeterminada de los patos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807549"
---
# <a name="default-ducking-experience"></a><span data-ttu-id="a3a48-103">Experiencia predeterminada de los patos</span><span class="sxs-lookup"><span data-stu-id="a3a48-103">Default Ducking Experience</span></span>

<span data-ttu-id="a3a48-104">Considere un escenario en el que un usuario recibe una llamada telefónica mientras escucha música en el equipo.</span><span class="sxs-lookup"><span data-stu-id="a3a48-104">Consider a scenario where a user receives a phone call while listening to music on the computer.</span></span> <span data-ttu-id="a3a48-105">Durante la llamada de teléfono, el usuario desea reducir el nivel de volumen de la música mientras asiste a la llamada de teléfono y reanudar el volumen original una vez finalizada la llamada telefónica.</span><span class="sxs-lookup"><span data-stu-id="a3a48-105">During the phone call, the user wants to reduce the volume level of the music while attending to the phone call, and resume the original volume after the phone call has ended.</span></span> <span data-ttu-id="a3a48-106">En función de las opciones especificadas por el usuario en el panel de control **sonidos** , el sistema operativo proporciona automáticamente esta *funcionalidad a través* de la función de la pérdida de la *secuencia* o la reducción de la intensidad de una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="a3a48-106">Depending on the options specified by the user in the **Sounds** control panel, the operating system automatically provides this functionality through *ducking* or *stream attenuation*—reduction in the intensity of an audio stream.</span></span>

<span data-ttu-id="a3a48-107">La experiencia de atenuación predeterminada depende de las preferencias del usuario, tal y como se especifica en la opción de **sonido** del panel de control.</span><span class="sxs-lookup"><span data-stu-id="a3a48-107">The default attenuation experience depends on the user's preference, as specified in the control panel's **Sound** option.</span></span> <span data-ttu-id="a3a48-108">En la pestaña **comunicaciones** , el usuario puede elegir un nivel de atenuación (el valor predeterminado es 80%), silenciar todas las secuencias que no son de comunicación o deshabilitar la experiencia de atenuación de flujo predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a3a48-108">On the **Communications** tab, the user can choose an attenuation level (default value is 80%), mute all non-communication streams, or disable the default stream attenuation experience.</span></span> <span data-ttu-id="a3a48-109">El sistema permite que se abran nuevas secuencias no de comunicación (excepto para nuevos sonidos del sistema) durante la sesión de comunicación, pero las nuevas secuencias no se atenúan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a3a48-109">The system allows new non-communication streams (except for new system sounds) to be opened during the communication session but the new streams are not automatically attenuated.</span></span> <span data-ttu-id="a3a48-110">Cuando se cierran todas las secuencias de comunicación, el sistema finaliza la sesión de comunicación y restaura el volumen de las secuencias que se atenuaron durante la sesión de comunicación.</span><span class="sxs-lookup"><span data-stu-id="a3a48-110">When all of the communication streams are closed, the system ends the communication session and restores the volume of the streams that were attenuated during the communication session.</span></span>

<span data-ttu-id="a3a48-111">Para indicar la atenuación de la secuencia visualmente, el sistema cambia la configuración del mezclador de volumen en función de las preferencias del usuario.</span><span class="sxs-lookup"><span data-stu-id="a3a48-111">To indicate stream attenuation visually, the system changes the volume mixer settings depending on the user's preference.</span></span> <span data-ttu-id="a3a48-112">Por ejemplo, si el usuario especifica un nivel de atenuación, el mezclador de volumen baja el control deslizante, muestra el nuevo volumen atenuado y muestra el nivel de volumen original.</span><span class="sxs-lookup"><span data-stu-id="a3a48-112">For example, if the user specifies an attenuation level, the volume mixer lowers the slider, displays the new attenuated volume, and displays the original volume level.</span></span> <span data-ttu-id="a3a48-113">En la imagen siguiente se ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="a3a48-113">The following image illustrates this process.</span></span>

![diagrama del comportamiento de atenuación de secuencias predeterminado proporcionado en Windows 7](images/stream-aatenuation.jpg)

<span data-ttu-id="a3a48-115">Una aplicación puede invalidar la atenuación de flujos e implementar una experiencia personalizada de pato si sabe cuándo se inicia y finaliza la sesión de comunicación.</span><span class="sxs-lookup"><span data-stu-id="a3a48-115">An application can override stream attenuation and implement a custom ducking experience if it knows when the communication session starts and ends.</span></span> <span data-ttu-id="a3a48-116">Para obtener más información, vea [proporcionar un comportamiento personalizado de patos](providing-a-custom-ducking-experience.md).</span><span class="sxs-lookup"><span data-stu-id="a3a48-116">For more information, see [Providing a Custom Ducking Behavior](providing-a-custom-ducking-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3a48-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3a48-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3a48-118">Uso de un dispositivo de comunicación</span><span class="sxs-lookup"><span data-stu-id="a3a48-118">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="a3a48-119">Deshabilitación de la experiencia de patos predeterminada</span><span class="sxs-lookup"><span data-stu-id="a3a48-119">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="a3a48-120">Proporcionar un comportamiento personalizado de patos</span><span class="sxs-lookup"><span data-stu-id="a3a48-120">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="a3a48-121">Consideraciones de implementación para las notificaciones de patos</span><span class="sxs-lookup"><span data-stu-id="a3a48-121">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="a3a48-122">Obtención de eventos de pato</span><span class="sxs-lookup"><span data-stu-id="a3a48-122">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



