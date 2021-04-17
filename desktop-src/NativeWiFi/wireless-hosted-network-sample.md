---
description: Muestra el uso de las funciones de red hospedada inalámbrica.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Ejemplo de red hospedada inalámbrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677415"
---
# <a name="wireless-hosted-network-sample"></a><span data-ttu-id="bad92-103">Ejemplo de red hospedada inalámbrica</span><span class="sxs-lookup"><span data-stu-id="bad92-103">Wireless Hosted Network Sample</span></span>

<span data-ttu-id="bad92-104">En el kit de desarrollo de software (SDK) de Microsoft Windows se incluye un ejemplo de red hospedada inalámbrica que muestra el uso de las funciones de red hospedada inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="bad92-104">A wireless Hosted Network sample that demonstrates the use of wireless Hosted Network functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bad92-105">La versión más reciente del Windows SDK está disponible en el [centro de descarga](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span><span class="sxs-lookup"><span data-stu-id="bad92-105">The latest version of the Windows SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span>

<span data-ttu-id="bad92-106">De forma predeterminada, el código fuente de ejemplo de red hospedada inalámbrica se instala en el directorio siguiente:</span><span class="sxs-lookup"><span data-stu-id="bad92-106">By default, the wireless Hosted Network sample source code is installed in the following directory:</span></span>

<span data-ttu-id="bad92-107">**C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ NetDs \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="bad92-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="bad92-108">El ejemplo de red hospedada inalámbrica se encuentra en la siguiente carpeta:</span><span class="sxs-lookup"><span data-stu-id="bad92-108">The wireless Hosted Network sample is located under the following folder:</span></span>

<span data-ttu-id="bad92-109">**WirelessHostedNetwork**</span><span class="sxs-lookup"><span data-stu-id="bad92-109">**WirelessHostedNetwork**</span></span>

<span data-ttu-id="bad92-110">El ejemplo de red hospedada inalámbrica se puede compilar en el Windows SDK para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bad92-110">The Wireless Hosted Network sample can be compiled on the Windows SDK for Windows 7.</span></span> <span data-ttu-id="bad92-111">El ejemplo de red hospedada inalámbrica se puede ejecutar en Windows 7 y en Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado.</span><span class="sxs-lookup"><span data-stu-id="bad92-111">The Wireless Hosted Network sample can be run on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span>

<span data-ttu-id="bad92-112">En Windows 7 y en Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado, el sistema operativo instala un dispositivo virtual si hay un adaptador inalámbrico compatible con redes hospedadas en la máquina.</span><span class="sxs-lookup"><span data-stu-id="bad92-112">On Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine.</span></span> <span data-ttu-id="bad92-113">Este dispositivo virtual normalmente se muestra en la "carpeta conexiones de red" como "conexión de red inalámbrica 2" con el nombre de dispositivo "adaptador de minipuerto de Microsoft Virtual WiFi" si el equipo tiene un único adaptador de red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="bad92-113">This virtual device normally shows up in the "Network Connections Folder" as "Wireless Network Connection 2" with a Device Name of "Microsoft Virtual WiFi Miniport adapter" if the computer has a single wireless network adapter.</span></span> <span data-ttu-id="bad92-114">Este dispositivo virtual se utiliza exclusivamente para realizar conexiones de punto de acceso de software (SoftAP).</span><span class="sxs-lookup"><span data-stu-id="bad92-114">This virtual device is used exclusively for performing software access point (SoftAP) connections.</span></span> <span data-ttu-id="bad92-115">La duración de este dispositivo virtual está ligada al adaptador inalámbrico físico.</span><span class="sxs-lookup"><span data-stu-id="bad92-115">The lifetime of this virtual device is tied to the physical wireless adapter.</span></span> <span data-ttu-id="bad92-116">Si el adaptador inalámbrico físico está deshabilitado, este dispositivo virtual también se quitará.</span><span class="sxs-lookup"><span data-stu-id="bad92-116">If the physical wireless adapter is disabled, this virtual device will be removed as well.</span></span>

<span data-ttu-id="bad92-117">Las funciones de red hospedada inalámbrica se usan para iniciar y detener la red hospedada inalámbrica, configurar o cambiar la configuración o consultar información.</span><span class="sxs-lookup"><span data-stu-id="bad92-117">The wireless Hosted Network functions are used to start and stop the wireless Hosted Network, configure or change settings, or query for information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bad92-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bad92-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bad92-119">Acerca de la red hospedada inalámbrica</span><span class="sxs-lookup"><span data-stu-id="bad92-119">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="bad92-120">Uso de redes hospedadas y conexión compartida a Internet</span><span class="sxs-lookup"><span data-stu-id="bad92-120">Using Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[<span data-ttu-id="bad92-121">**WlanHostedNetworkForceStart**</span><span class="sxs-lookup"><span data-stu-id="bad92-121">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[<span data-ttu-id="bad92-122">**WlanHostedNetworkInitSettings**</span><span class="sxs-lookup"><span data-stu-id="bad92-122">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[<span data-ttu-id="bad92-123">**WlanHostedNetworkQueryProperty**</span><span class="sxs-lookup"><span data-stu-id="bad92-123">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[<span data-ttu-id="bad92-124">**WlanHostedNetworkQuerySecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="bad92-124">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[<span data-ttu-id="bad92-125">**WlanHostedNetworkQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="bad92-125">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[<span data-ttu-id="bad92-126">**WlanHostedNetworkRefreshSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="bad92-126">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[<span data-ttu-id="bad92-127">**WlanHostedNetworkSetProperty**</span><span class="sxs-lookup"><span data-stu-id="bad92-127">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[<span data-ttu-id="bad92-128">**WlanHostedNetworkSetSecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="bad92-128">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[<span data-ttu-id="bad92-129">**WlanHostedNetworkStartUsing**</span><span class="sxs-lookup"><span data-stu-id="bad92-129">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[<span data-ttu-id="bad92-130">**WlanHostedNetworkStopUsing**</span><span class="sxs-lookup"><span data-stu-id="bad92-130">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[<span data-ttu-id="bad92-131">**WlanRegisterVirtualStationNotification**</span><span class="sxs-lookup"><span data-stu-id="bad92-131">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



