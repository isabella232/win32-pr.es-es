---
title: El puerto 3 está en desuso para los controladores NDIS 6,30
description: El puerto 3 está en desuso para los controladores NDIS 6,30
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104488410"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a><span data-ttu-id="03f53-103">El puerto 3 está en desuso para los controladores NDIS 6,30</span><span class="sxs-lookup"><span data-stu-id="03f53-103">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="03f53-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="03f53-104">Platforms</span></span>

<span data-ttu-id="03f53-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="03f53-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="03f53-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03f53-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="03f53-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="03f53-107">Description</span></span>

<span data-ttu-id="03f53-108">Windows 8 quita la compatibilidad de la plataforma para los controladores de WLAN del minipuerto NDIS para crear o iniciar el puerto de extensibilidad de IHV (también conocido como tercer puerto).</span><span class="sxs-lookup"><span data-stu-id="03f53-108">Windows 8 removes platform support for NDIS miniport WLAN drivers to create or start up the IHV extensibility port (also known as 3rd port).</span></span> <span data-ttu-id="03f53-109">Esta característica se presentó en Windows 7 como medida provisional mientras que Wi-Fi Alliance (WFA) desarrolló la Wi-Fi especificación directa.</span><span class="sxs-lookup"><span data-stu-id="03f53-109">This feature was introduced in Windows 7 as a stopgap measure while the Wi-Fi Alliance (WFA) developed the Wi-Fi Direct specification.</span></span> <span data-ttu-id="03f53-110">La especificación ya ha finalizado, los productos que usan Wi-Fi Direct se están certificando y Windows 8 presenta una pila de Wi-Fi directo nativa.</span><span class="sxs-lookup"><span data-stu-id="03f53-110">The specification is now finished, products using Wi-Fi Direct are being certified, and Windows 8 introduces a native Wi-Fi Direct stack.</span></span>

## <a name="manifestation"></a><span data-ttu-id="03f53-111">Manifestación</span><span class="sxs-lookup"><span data-stu-id="03f53-111">Manifestation</span></span>

<span data-ttu-id="03f53-112">Nada, ya que el tercer puerto es una funcionalidad de plataforma en la que se inician los controladores de minipuerto de WLAN si necesitan esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="03f53-112">Nothing, as third port is a platform capability that WLAN miniport drivers start up if they need this functionality.</span></span>

## <a name="solution"></a><span data-ttu-id="03f53-113">Solución</span><span class="sxs-lookup"><span data-stu-id="03f53-113">Solution</span></span>

<span data-ttu-id="03f53-114">Estamos manteniendo la característica de puerto de extensibilidad disponible para los controladores existentes que no informan de NDIS 6,30 para mantener la compatibilidad de los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="03f53-114">We are keeping the extensibility port feature available for existing drivers that do not report NDIS 6.30 to maintain device compatibility.</span></span> <span data-ttu-id="03f53-115">Sin embargo, los nuevos controladores de WLAN que informan de NDIS 6,30 no podrán iniciar este puerto; en su lugar, los desarrolladores de estos controladores deben usar Wi-Fi directo.</span><span class="sxs-lookup"><span data-stu-id="03f53-115">However, new WLAN drivers that report NDIS 6.30 will not be able to start this port; instead, developers of these drivers should use Wi-Fi Direct.</span></span>

 

 




