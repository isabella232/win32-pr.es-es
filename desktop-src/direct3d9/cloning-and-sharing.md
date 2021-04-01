---
description: Clonación y uso compartido (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonación y uso compartido (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907481"
---
# <a name="cloning-and-sharing-direct3d-9"></a><span data-ttu-id="a5400-103">Clonación y uso compartido (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a5400-103">Cloning and Sharing (Direct3D 9)</span></span>

## <a name="cloning-parameters"></a><span data-ttu-id="a5400-104">Parámetros de clonación</span><span class="sxs-lookup"><span data-stu-id="a5400-104">Cloning Parameters</span></span>

<span data-ttu-id="a5400-105">La clonación tiene las siguientes restricciones.</span><span class="sxs-lookup"><span data-stu-id="a5400-105">Cloning has the following restrictions.</span></span>

-   <span data-ttu-id="a5400-106">Los clones heredan el grupo del efecto original.</span><span class="sxs-lookup"><span data-stu-id="a5400-106">Clones inherit the original effect's pool.</span></span> <span data-ttu-id="a5400-107">Vea la sección parámetros de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="a5400-107">See the Sharing Parameters section.</span></span>
-   <span data-ttu-id="a5400-108">Los clones heredan las técnicas, las pasadas, los parámetros y las anotaciones del efecto original (incluidas todas las anotaciones agregadas con [**ID3DXEffect**](id3dxeffect.md)).</span><span class="sxs-lookup"><span data-stu-id="a5400-108">Clones inherit the original effect's techniques, passes, parameters, and annotations (including all annotations added with [**ID3DXEffect**](id3dxeffect.md)).</span></span>
-   <span data-ttu-id="a5400-109">Los clones heredan las anotaciones agregadas dinámicamente del efecto original.</span><span class="sxs-lookup"><span data-stu-id="a5400-109">Clones inherit the original effect's dynamically added annotations.</span></span>
-   <span data-ttu-id="a5400-110">La clonación en un nuevo dispositivo producirá un error si el grupo del efecto original no era **nulo** y el efecto original contenía un parámetro dependiente del dispositivo compartido (como una textura o un sombreador).</span><span class="sxs-lookup"><span data-stu-id="a5400-110">Cloning onto a new device will fail if the original effect's pool was not **NULL** and the original effect contained a shared device-dependent parameter (such as a texture or shader).</span></span>

## <a name="sharing-parameters"></a><span data-ttu-id="a5400-111">Parámetros de uso compartido</span><span class="sxs-lookup"><span data-stu-id="a5400-111">Sharing Parameters</span></span>

<span data-ttu-id="a5400-112">Un grupo es un búfer que comparte parámetros de efectos entre distintos efectos.</span><span class="sxs-lookup"><span data-stu-id="a5400-112">A pool is a buffer that shares effect parameters between different effects.</span></span> <span data-ttu-id="a5400-113">Para agregar parámetros a un grupo, especifique un uso compartido cuando se cree el efecto.</span><span class="sxs-lookup"><span data-stu-id="a5400-113">To add parameters to a pool, specify a shared usage when the effect is created.</span></span>

<span data-ttu-id="a5400-114">Un grupo tiene las restricciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="a5400-114">A pool has the following restrictions.</span></span>

-   <span data-ttu-id="a5400-115">Un parámetro se agrega al grupo la primera vez que se agrega al grupo un efecto que contiene el parámetro (compartido).</span><span class="sxs-lookup"><span data-stu-id="a5400-115">A parameter is added to the pool the first time an effect containing that (shared) parameter is added to the pool.</span></span>
-   <span data-ttu-id="a5400-116">Un grupo obtiene los valores iniciales del primer parámetro compartido; los parámetros compartidos posteriormente obtienen sus valores del grupo.</span><span class="sxs-lookup"><span data-stu-id="a5400-116">A pool gets initial values from the first shared parameter; parameters shared subsequently get their values from the pool.</span></span>
-   <span data-ttu-id="a5400-117">Un parámetro se elimina del grupo cuando se liberan todas las referencias de efecto al parámetro compartido.</span><span class="sxs-lookup"><span data-stu-id="a5400-117">A parameter is deleted from the pool when all effect references to the shared parameter are released.</span></span>
-   <span data-ttu-id="a5400-118">Todos los efectos del grupo que contengan el mismo parámetro dependiente del dispositivo (compartido) deben tener el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5400-118">All effects in the pool that contain the same (shared) device-dependent parameter must have the same device.</span></span>

<span data-ttu-id="a5400-119">**Null** se puede usar para especificar ningún grupo, en cuyo caso no se comparte ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="a5400-119">**NULL** can be used to specify no pool, in which case no parameters are shared.</span></span> <span data-ttu-id="a5400-120">Esto es casi equivalente a especificar un grupo único solo para este efecto.</span><span class="sxs-lookup"><span data-stu-id="a5400-120">This is almost equivalent to specifying a unique pool just for this effect.</span></span> <span data-ttu-id="a5400-121">La única diferencia es que, cuando se clona el efecto, el clon no compartirá sus parámetros compartidos con el original.</span><span class="sxs-lookup"><span data-stu-id="a5400-121">The single difference is that when the effect is cloned, the clone will not share its shared parameters with the original.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5400-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5400-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5400-123">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="a5400-123">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



