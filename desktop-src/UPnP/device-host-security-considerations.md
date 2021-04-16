---
title: Consideraciones de seguridad del host de dispositivo
description: El uso del host del dispositivo crea problemas de seguridad.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5a51b90bff33949a33cd9fa1046deb1916ab30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487863"
---
# <a name="device-host-security-considerations"></a><span data-ttu-id="575d9-103">Consideraciones de seguridad del host de dispositivo</span><span class="sxs-lookup"><span data-stu-id="575d9-103">Device Host Security Considerations</span></span>

<span data-ttu-id="575d9-104">El uso del host de dispositivo crea problemas de seguridad debido a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="575d9-104">Using the device host creates security issues because of the following:</span></span>

-   <span data-ttu-id="575d9-105">Los dispositivos alojados en un equipo que ejecuta Windows XP envían anuncios en todas las redes.</span><span class="sxs-lookup"><span data-stu-id="575d9-105">Devices hosted on a computer running Windows XP sends announcements on all networks.</span></span>
-   <span data-ttu-id="575d9-106">Los dispositivos hospedados en un equipo que ejecuta Windows XP permiten el control de dispositivos desde todas las redes.</span><span class="sxs-lookup"><span data-stu-id="575d9-106">Devices hosted on a computer running Windows XP allow control of devices from all networks.</span></span>

<span data-ttu-id="575d9-107">Esto aumenta el riesgo para los consumidores domésticos, ya que los dispositivos como un reproductor de media o una iluminación puente o sistema HVAC hospedados en un equipo que ejecuta Windows XP son visibles y se pueden controlar desde puntos de control fuera de la Página principal.</span><span class="sxs-lookup"><span data-stu-id="575d9-107">This increases the risk to home consumers, because devices such as a media player or a bridged lighting or HVAC system hosted on a computer running Windows XP are visible and can be controlled from control points outside the home.</span></span>

<span data-ttu-id="575d9-108">Al crear un dispositivo hospedado, debe tener en cuenta algunos problemas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="575d9-108">When you are creating a hosted device, you need to take into consideration some security issues.</span></span>

-   <span data-ttu-id="575d9-109">Para reducir el ámbito de detección y ataque de dispositivos basados en UPnP, el TTL de todos los mensajes SSDP es 1.</span><span class="sxs-lookup"><span data-stu-id="575d9-109">To reduce the scope of discovery and attack of UPnP-based devices, the TTL of all SSDP messages is 1.</span></span> <span data-ttu-id="575d9-110">Esto significa que un dispositivo registrado solo lo detectan los puntos de control de la misma red.</span><span class="sxs-lookup"><span data-stu-id="575d9-110">This means that a registered device is only discovered by control points on the same network.</span></span> <span data-ttu-id="575d9-111">Puede configurar un TTL superior en el registro.</span><span class="sxs-lookup"><span data-stu-id="575d9-111">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="575d9-112">El registro de un dispositivo que no se está ejecutando requiere el registro previo del archivo Device. dll con COM, lo que requiere privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="575d9-112">Registering a non-running device requires pre-registering the device .dll with COM, which requires administrator privilege.</span></span>
-   <span data-ttu-id="575d9-113">El registro de un dispositivo en ejecución requiere privilegios de administrador, servicio local o sistema local.</span><span class="sxs-lookup"><span data-stu-id="575d9-113">Registering a running device requires Administrator, Local Service, or Local System privilege.</span></span>
-   <span data-ttu-id="575d9-114">Cuando se inicia el host del dispositivo, se ejecuta como [LocalService](/windows/desktop/Services/localservice-account).</span><span class="sxs-lookup"><span data-stu-id="575d9-114">When the device host is started, it is run as [LocalService](/windows/desktop/Services/localservice-account).</span></span> <span data-ttu-id="575d9-115">Esto proporciona al dispositivo la capacidad de generar auditorías y leer la clave del registro **HKEY \_ local \_ Machine** .</span><span class="sxs-lookup"><span data-stu-id="575d9-115">This gives the device the ability to generate audits and read the **HKEY\_LOCAL\_MACHINE** registry key.</span></span> <span data-ttu-id="575d9-116">El dispositivo tiene acceso a **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="575d9-116">The device does have access to **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="575d9-117">La cuenta LocalService puede usar los recursos a los que se ha concedido a LocalService, así como los que conceden acceso a AuthenticatedUser.</span><span class="sxs-lookup"><span data-stu-id="575d9-117">The LocalService account can use resources to which LocalService has been granted access, as well as those that grant access to AuthenticatedUser.</span></span> <span data-ttu-id="575d9-118">El dispositivo tiene acceso de sistema de archivos restringido.</span><span class="sxs-lookup"><span data-stu-id="575d9-118">The device has restricted file system access.</span></span>
-   <span data-ttu-id="575d9-119">Las ACL del sistema de archivos deben actualizarse para permitir el acceso de [LocalService](/windows/desktop/Services/localservice-account) al directorio de recursos.</span><span class="sxs-lookup"><span data-stu-id="575d9-119">The file system ACLs must be updated to allow [LocalService](/windows/desktop/Services/localservice-account) access to the resource directory.</span></span>
-   <span data-ttu-id="575d9-120">Si el dispositivo debe tener más acceso de seguridad, puede crear su propio proceso para el dispositivo y registrarlo mediante [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).</span><span class="sxs-lookup"><span data-stu-id="575d9-120">If your device must have more security access, you can create your own process for the device and register it by using [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).</span></span>

 

 