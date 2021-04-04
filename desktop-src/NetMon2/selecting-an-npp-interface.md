---
description: Los proveedores de paquetes de red (NPPs) exponen las interfaces IDelaydC, IESP, IRTC y IStas.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Seleccionar una interfaz NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908695"
---
# <a name="selecting-an-npp-interface"></a><span data-ttu-id="839fb-103">Seleccionar una interfaz NPP</span><span class="sxs-lookup"><span data-stu-id="839fb-103">Selecting an NPP Interface</span></span>

<span data-ttu-id="839fb-104">Los proveedores de paquetes de red (NPPs) exponen las interfaces [**IDelaydC**](idelaydc.md), [**iesp**](iesp.md), [**IRTC**](irtc.md)y [**istas**](istats.md) .</span><span class="sxs-lookup"><span data-stu-id="839fb-104">Network packet providers (NPPs) expose the [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md), and [**IStats**](istats.md) interfaces.</span></span> <span data-ttu-id="839fb-105">Cada una de estas interfaces proporciona métodos similares para conectar el NPP a la red, capturar el tráfico de red y recopilar información estadística sobre los datos capturados.</span><span class="sxs-lookup"><span data-stu-id="839fb-105">Each of these interfaces provides similar methods for connecting the NPP to the network, capturing network traffic, and collecting statistical information about the captured data.</span></span> <span data-ttu-id="839fb-106">Para elegir la interfaz que se va a usar, consulte la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="839fb-106">To choose which interface to use, refer to the following table.</span></span>

> [!Note]  
> <span data-ttu-id="839fb-107">Cuando conecta un NPP a la red con una de estas interfaces, solo puede usar los métodos proporcionados por esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="839fb-107">When you connect an NPP to the network with one of these interfaces, you can only use the methods provided by that interface.</span></span> <span data-ttu-id="839fb-108">Por ejemplo, si se conecta a la red mediante la interfaz [**IRTC**](irtc.md) y, a continuación, intenta iniciar una captura con [**IDelaydC**](idelaydc.md), se producirá un error en la llamada para iniciar la captura y se devolverá un código de error.</span><span class="sxs-lookup"><span data-stu-id="839fb-108">For example, if you connect to the network using the [**IRTC**](irtc.md) interface and then try to start a capture with [**IDelaydC**](idelaydc.md), your call to start the capture will fail, and an error code will be returned.</span></span>

 



| <span data-ttu-id="839fb-109">Interfaz</span><span class="sxs-lookup"><span data-stu-id="839fb-109">Interface</span></span>                    | <span data-ttu-id="839fb-110">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="839fb-110">When to use</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="839fb-111">**IDelaydC**</span><span class="sxs-lookup"><span data-stu-id="839fb-111">**IDelaydC**</span></span>](idelaydc.md) | <span data-ttu-id="839fb-112">Use para capturar el tráfico de red y almacenarlo en un archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="839fb-112">Use to capture network traffic and store it in a capture file.</span></span> <span data-ttu-id="839fb-113">Esta interfaz la utilizan la interfaz de usuario de Monitor de red y otras aplicaciones NPP, que requieren el almacenamiento de la información de red capturada.</span><span class="sxs-lookup"><span data-stu-id="839fb-113">This interface is used by the Network Monitor UI and other NPP applications, which require storing captured network information.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="839fb-114">**IESP**</span><span class="sxs-lookup"><span data-stu-id="839fb-114">**IESP**</span></span>](iesp.md)         | <span data-ttu-id="839fb-115">Se utiliza para proporcionar estadísticas mejoradas en un formato de archivo ESP especial.</span><span class="sxs-lookup"><span data-stu-id="839fb-115">Used to provide enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="839fb-116">Esta interfaz la usan las aplicaciones NPP que requieren las estadísticas mejoradas proporcionadas por el formato ESP.</span><span class="sxs-lookup"><span data-stu-id="839fb-116">This interface is used by NPP applications that require the enhanced statistics provided by the ESP format.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="839fb-117">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="839fb-117">**IRTC**</span></span>](irtc.md)         | <span data-ttu-id="839fb-118">Se usa para capturar el tráfico de red en tiempo real y desencadenar eventos cuando se producen.</span><span class="sxs-lookup"><span data-stu-id="839fb-118">Use to capture real-time network traffic and to trigger events when they occur.</span></span> <span data-ttu-id="839fb-119">Esta interfaz la usan las aplicaciones NPP que requieren capturas en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="839fb-119">This interface is used by NPP applications that require run-time captures.</span></span> <span data-ttu-id="839fb-120">Tenga en cuenta que esta interfaz no proporciona las estadísticas que proporcionan las otras interfaces NPP, ni le permite insertar fotogramas en el tráfico de red capturado.</span><span class="sxs-lookup"><span data-stu-id="839fb-120">Note that this interface does not provide the statistics that the other NPP interfaces provide, nor does it allow you to insert frames into the captured network traffic.</span></span><br/> |
| [<span data-ttu-id="839fb-121">**IStas**</span><span class="sxs-lookup"><span data-stu-id="839fb-121">**IStats**</span></span>](istats.md)     | <span data-ttu-id="839fb-122">Use para recuperar estadísticas de captura, pero no los fotogramas capturados.</span><span class="sxs-lookup"><span data-stu-id="839fb-122">Use to retrieve capture statistics but not the captured frames.</span></span>                                                                                                                                                                                                                                                                                 |



 

 

 




