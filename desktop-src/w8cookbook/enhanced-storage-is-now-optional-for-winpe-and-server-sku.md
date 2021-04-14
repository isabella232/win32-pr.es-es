---
title: El almacenamiento mejorado ahora es opcional para WINPE y SKU de servidor
description: El almacenamiento mejorado ahora es opcional para WINPE y SKU de servidor
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104359461"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a><span data-ttu-id="c45d5-103">El almacenamiento mejorado ahora es opcional para WINPE y SKU de servidor</span><span class="sxs-lookup"><span data-stu-id="c45d5-103">Enhanced storage is now optional for WINPE and server SKU</span></span>

## <a name="platforms"></a><span data-ttu-id="c45d5-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="c45d5-104">Platforms</span></span>

<span data-ttu-id="c45d5-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="c45d5-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="c45d5-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c45d5-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="c45d5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c45d5-107">Description</span></span>

<span data-ttu-id="c45d5-108">El almacenamiento mejorado siempre estaba disponible en dispositivos USB de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c45d5-108">Enhanced storage was always available in Windows 7 USB devices.</span></span> <span data-ttu-id="c45d5-109">Con el lanzamiento de Windows 8, está disponible para todos los dispositivos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="c45d5-109">With the release of Windows 8, it is available for all storage devices.</span></span> <span data-ttu-id="c45d5-110">En los dispositivos basados en cliente, está habilitado de forma predeterminada. en los dispositivos de servidor es opcional y se debe aprovisionar a través de Entorno de preinstalación de Windows (WinPE).</span><span class="sxs-lookup"><span data-stu-id="c45d5-110">In client-based devices, it is enabled by default; in server devices it is optional and must be provisioned through Windows Preinstallation Environment (WinPE).</span></span>

## <a name="manifestation"></a><span data-ttu-id="c45d5-111">Manifestación</span><span class="sxs-lookup"><span data-stu-id="c45d5-111">Manifestation</span></span>

<span data-ttu-id="c45d5-112">El dispositivo de servidor producirá un error si el almacenamiento mejorado no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c45d5-112">The server device will fail if enhanced storage is not enabled.</span></span>

<span data-ttu-id="c45d5-113">Los dispositivos de arranque deben aprovisionarse a través de WinPE con esta opción habilitada.</span><span class="sxs-lookup"><span data-stu-id="c45d5-113">Boot devices must be provisioned through WinPE with this enabled.</span></span>

## <a name="solution"></a><span data-ttu-id="c45d5-114">Solución</span><span class="sxs-lookup"><span data-stu-id="c45d5-114">Solution</span></span>

<span data-ttu-id="c45d5-115">Dado que el almacenamiento mejorado es opcional para el servidor en tiempo de ejecución, los desarrolladores deben agregarlo a WinPE para aprovisionar y activar dichas unidades.</span><span class="sxs-lookup"><span data-stu-id="c45d5-115">Because enhanced storage is optional for runtime server, developers must add it to WinPE for provisioning and activation of those drives.</span></span> <span data-ttu-id="c45d5-116">Consulte la guía de implementación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c45d5-116">See the deployment guide for details.</span></span>

<span data-ttu-id="c45d5-117">Los administradores del servidor deben configurar explícitamente su servidor para que use el almacenamiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="c45d5-117">Server administrators must then explicitly configure their server to use enhanced storage.</span></span>

 

 




