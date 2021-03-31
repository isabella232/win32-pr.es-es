---
title: El sistema operativo controla ahora las unidades de disco ópticos de energía
description: El sistema operativo controla ahora las unidades de disco ópticos de energía
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794200"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a><span data-ttu-id="8bbff-103">El sistema operativo controla ahora las unidades de disco ópticos de energía</span><span class="sxs-lookup"><span data-stu-id="8bbff-103">Operating system now controls power to optical disk drives</span></span>

## <a name="platforms"></a><span data-ttu-id="8bbff-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="8bbff-104">Platforms</span></span>

<span data-ttu-id="8bbff-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="8bbff-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="8bbff-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8bbff-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="8bbff-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bbff-107">Description</span></span>

<span data-ttu-id="8bbff-108">En versiones anteriores de Windows, la capacidad de la unidad óptica no se administraba cuando la unidad óptica no estaba en uso.</span><span class="sxs-lookup"><span data-stu-id="8bbff-108">In previous versions of Windows, power to the optical drive was not managed when the optical drive was not in use.</span></span> <span data-ttu-id="8bbff-109">Ahora, si no hay ningún medio en la unidad de disco óptico (IMPAr), el sistema operativo apaga la alimentación de la unidad óptica.</span><span class="sxs-lookup"><span data-stu-id="8bbff-109">Now, if there is no media present in the optical disk drive (ODD), the operating system turns off the power to the optical drive.</span></span> <span data-ttu-id="8bbff-110">Esta característica se denomina sin fuerza de energía (ZPODD).</span><span class="sxs-lookup"><span data-stu-id="8bbff-110">This feature is called zero power ODD (ZPODD).</span></span> <span data-ttu-id="8bbff-111">La característica solo es aplicable a las unidades ópticas que usan un conector SATA Slimline (Serial Advanced Technology Attachment).</span><span class="sxs-lookup"><span data-stu-id="8bbff-111">The feature is applicable only to optical drives that use a Slimline SATA (Serial Advanced Technology Attachment) connector.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8bbff-112">Manifestación</span><span class="sxs-lookup"><span data-stu-id="8bbff-112">Manifestation</span></span>

<span data-ttu-id="8bbff-113">No hemos encontrado ningún impacto negativo en este nuevo comportamiento; sin embargo, debe ser consciente de ello, ya que puede dar lugar a un comportamiento inesperado del software de escritura de medios.</span><span class="sxs-lookup"><span data-stu-id="8bbff-113">We have not found any negative impacts from this new behavior; however, you should be aware of it as it may result in unexpected behavior of media-writing software.</span></span>

## <a name="mitigation"></a><span data-ttu-id="8bbff-114">Mitigación</span><span class="sxs-lookup"><span data-stu-id="8bbff-114">Mitigation</span></span>

<span data-ttu-id="8bbff-115">Para revertir al estado AlwaysOn, desactive esta funcionalidad en el registro.</span><span class="sxs-lookup"><span data-stu-id="8bbff-115">To revert to always-on status, turn off this functionality in the Registry.</span></span> <span data-ttu-id="8bbff-116">La ruta de acceso absoluta al valor del registro es:</span><span class="sxs-lookup"><span data-stu-id="8bbff-116">The absolute path to the registry value is:</span></span>

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

<span data-ttu-id="8bbff-117">Su tipo es DWORD (32 bits) y si su valor es 0, ZPODD está deshabilitado; Si se trata de cualquier otro valor, ZPODD está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8bbff-117">Its type is DWORD (32 bit), and if its value is 0, then ZPODD is disabled; if it’s any other value, then ZPODD is enabled.</span></span>

## <a name="tests"></a><span data-ttu-id="8bbff-118">Pruebas</span><span class="sxs-lookup"><span data-stu-id="8bbff-118">Tests</span></span>

<span data-ttu-id="8bbff-119">Pruebe el software de escritura multimedia para detectar las anomalías que se produzcan debido a esta nueva característica.</span><span class="sxs-lookup"><span data-stu-id="8bbff-119">Test your media-writing software for any anomalies that occur due to this new feature.</span></span> <span data-ttu-id="8bbff-120">[Informe a Microsoft](mailto:OptIssue@microsoft.com) de los problemas que encuentre con esta nueva característica.</span><span class="sxs-lookup"><span data-stu-id="8bbff-120">Please [inform Microsoft](mailto:OptIssue@microsoft.com) of any issues you find with this new feature.</span></span>

 

 




