---
title: Glosario de acceso a dispositivos
description: A continuación se indican los términos que se usan en la documentación de la API de acceso a dispositivos.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420213"
---
# <a name="device-access-glossary"></a><span data-ttu-id="b9372-103">Glosario de acceso a dispositivos</span><span class="sxs-lookup"><span data-stu-id="b9372-103">Device Access Glossary</span></span>

<span data-ttu-id="b9372-104">A continuación se indican los términos que se usan en la documentación de la API de acceso a dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b9372-104">The following are terms used throughout the documentation for the Device Access API.</span></span>

<dl> <dt>

<span data-ttu-id="b9372-105">**AppContainer**</span><span class="sxs-lookup"><span data-stu-id="b9372-105">**AppContainer**</span></span>
</dt> <dd>

<span data-ttu-id="b9372-106">Entorno de ejecución muy restringido en el que se ejecuta un proceso con un subconjunto reducido de privilegios del usuario.</span><span class="sxs-lookup"><span data-stu-id="b9372-106">A highly restricted execution environment in which a process runs with a reduced subset of the user's privileges.</span></span> <span data-ttu-id="b9372-107">Un proceso que se ejecuta dentro de un AppContainer se denomina proceso AppContainer.</span><span class="sxs-lookup"><span data-stu-id="b9372-107">A process that's running within an AppContainer is called an AppContainer process.</span></span> <span data-ttu-id="b9372-108">Un proceso de AppContainer está aislado de otros procesos de AppContainer y del perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="b9372-108">An AppContainer process is isolated from other AppContainer processes and from the user's profile.</span></span> <span data-ttu-id="b9372-109">Tiene acceso limitado a un subconjunto muy pequeño de recursos del sistema, como archivos, dispositivos, claves del registro, puntos de conexión de la llamada a procedimiento de la comunicación entre procesos (IPC)/Remote y recursos de red.</span><span class="sxs-lookup"><span data-stu-id="b9372-109">It has limited access to a very small subset of system resources like files, devices, registry keys, interprocess communication (IPC)/remote procedure call (RPC) endpoints, and network resources.</span></span>

</dd> <dt>

<span data-ttu-id="b9372-110">**Binding**</span><span class="sxs-lookup"><span data-stu-id="b9372-110">**Binding**</span></span>
</dt> <dd>

<span data-ttu-id="b9372-111">Asociar un objeto de acceso de dispositivo a una interfaz de dispositivo determinada.</span><span class="sxs-lookup"><span data-stu-id="b9372-111">Associating a device access object with a particular device interface.</span></span> <span data-ttu-id="b9372-112">Si el enlace se realiza correctamente, las aplicaciones de la tienda Windows pueden usar el objeto de acceso de dispositivo como agente para comunicarse con el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9372-112">If binding is successful, Windows Store apps can use the device access object as a broker to communicate with the device driver.</span></span>

</dd> <dt>

<span data-ttu-id="b9372-113">**Agente**</span><span class="sxs-lookup"><span data-stu-id="b9372-113">**Broker**</span></span>
</dt> <dd>

<span data-ttu-id="b9372-114">Componente que proporciona acceso a un recurso que no se concede de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b9372-114">A component that provides access to a resource that isn't granted by default.</span></span>

</dd> <dt>

<span data-ttu-id="b9372-115">**Aplicación con privilegios**</span><span class="sxs-lookup"><span data-stu-id="b9372-115">**Privileged App**</span></span>
</dt> <dd>

<span data-ttu-id="b9372-116">Una aplicación que se identifica en los metadatos de un dispositivo determinado como asociado a ese dispositivo, de modo que pueda comunicarse con la interfaz restringida del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9372-116">An app that's identified in a particular device's metadata as associated with that device, so that it can communicate with the device driver's restricted interface.</span></span> <span data-ttu-id="b9372-117">Un ejemplo de este tipo de aplicación podría ser una aplicación de reproducción de música de su propiedad que tiene permiso exclusivo para la sincronización con un reproductor de música portátil, cuando las aplicaciones de la competencia no pueden.</span><span class="sxs-lookup"><span data-stu-id="b9372-117">An example of such an app might be a proprietary music playback app that has exclusive permission to sync with a portable music player, when apps from competitors can't.</span></span> <span data-ttu-id="b9372-118">Para obtener más información sobre cómo establecer los metadatos de un dispositivo o cómo restringir un controlador a las aplicaciones con privilegios, consulte [aplicaciones de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span><span class="sxs-lookup"><span data-stu-id="b9372-118">For more information about how to set a device's metadata or how to restrict a driver to privileged apps, see [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span></span>

</dd> </dl>
