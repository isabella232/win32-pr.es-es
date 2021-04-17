---
description: Siga las instrucciones que se indican a continuación al crear una revisión para una Windows Installer actualización pequeña.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Crear una revisión de actualización pequeña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669750"
---
# <a name="creating-a-small-update-patch"></a><span data-ttu-id="349aa-103">Crear una revisión de actualización pequeña</span><span class="sxs-lookup"><span data-stu-id="349aa-103">Creating a Small Update Patch</span></span>

<span data-ttu-id="349aa-104">Al crear una revisión para [las actualizaciones pequeñas](small-updates.md), los autores deben cumplir las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="349aa-104">When creating a patch for [small updates](small-updates.md), authors should adhere to the following guidelines:</span></span>

-   <span data-ttu-id="349aa-105">Las revisiones de actualización pequeñas deben diseñarse para una única instalación de destino.</span><span class="sxs-lookup"><span data-stu-id="349aa-105">Small update patches must be designed for a single, target installation.</span></span>
-   <span data-ttu-id="349aa-106">Las revisiones de actualización pequeñas deben usar la versión más antigua como la instalación de destino.</span><span class="sxs-lookup"><span data-stu-id="349aa-106">Small update patches should use the earliest version as the target installation.</span></span>
-   <span data-ttu-id="349aa-107">Una revisión de actualización pequeña debe reemplazar y hacer que las revisiones de actualización pequeñas anteriores queden obsoletas.</span><span class="sxs-lookup"><span data-stu-id="349aa-107">A small update patch should replace and make obsolete any earlier small update patches.</span></span>

<span data-ttu-id="349aa-108">El siguiente escenario muestra Cuándo es mejor una pequeña revisión de actualización.</span><span class="sxs-lookup"><span data-stu-id="349aa-108">The following scenario illustrates when a small update patch is best.</span></span>

<span data-ttu-id="349aa-109">Su empresa incluye la versión 1,0 de Myproduct.msi.</span><span class="sxs-lookup"><span data-stu-id="349aa-109">Your company ships version 1.0 of Myproduct.msi.</span></span> <span data-ttu-id="349aa-110">Poco después, envía una pequeña revisión de [actualización](small-updates.md) para Myproduct.msi denominada QFE1.</span><span class="sxs-lookup"><span data-stu-id="349aa-110">Shortly thereafter, you ship a [small update](small-updates.md) patch for Myproduct.msi called QFE1.</span></span> <span data-ttu-id="349aa-111">Esto no cambia la propiedad [**ProductCode**](productcode.md) o la propiedad [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="349aa-111">This does not change the [**ProductCode**](productcode.md) property or the [**ProductVersion**](productversion.md) property.</span></span>

<span data-ttu-id="349aa-112">Más adelante, creará una segunda revisión de [actualización pequeña](small-updates.md) para Myproduct.msi denominada QFE2.</span><span class="sxs-lookup"><span data-stu-id="349aa-112">Later, you author a second [small update](small-updates.md) patch for Myproduct.msi called QFE2.</span></span> <span data-ttu-id="349aa-113">Esta segunda revisión debe tener como destino Myproduct.msi versión 1,0.</span><span class="sxs-lookup"><span data-stu-id="349aa-113">This second patch must target Myproduct.msi version 1.0.</span></span> <span data-ttu-id="349aa-114">Esta segunda revisión no debe tener como destino Myproduct.msi versión 1,0 y Myproduct.msi versión 1,0 + QFE1.</span><span class="sxs-lookup"><span data-stu-id="349aa-114">This second patch must not target both Myproduct.msi version 1.0 and Myproduct.msi version 1.0 + QFE1.</span></span> <span data-ttu-id="349aa-115">Cuando se aplica QFE2, debe quitar QFE1.</span><span class="sxs-lookup"><span data-stu-id="349aa-115">When QFE2 is applied it should remove QFE1.</span></span>

 

 



