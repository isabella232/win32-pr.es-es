---
description: Efecto sobre volumen
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Efecto sobre volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687862"
---
# <a name="volume-envelope-effect"></a><span data-ttu-id="d92ae-103">Efecto sobre volumen</span><span class="sxs-lookup"><span data-stu-id="d92ae-103">Volume Envelope Effect</span></span>

> [!Note]  
> <span data-ttu-id="d92ae-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d92ae-104">\[Deprecated.</span></span> <span data-ttu-id="d92ae-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d92ae-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d92ae-106">El efecto sobre volumen establece el volumen en una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="d92ae-106">The Volume Envelope effect sets the volume on an audio stream.</span></span>

<span data-ttu-id="d92ae-107">IDENTIFICADOR de clase (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="d92ae-107">Class ID (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span></span>

<span data-ttu-id="d92ae-108">Nombre de la variable CLSID: CLSID \_ AudMixer</span><span class="sxs-lookup"><span data-stu-id="d92ae-108">CLSID Variable Name: CLSID\_AudMixer</span></span>

<span data-ttu-id="d92ae-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d92ae-109">Properties</span></span>



| <span data-ttu-id="d92ae-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d92ae-110">Property</span></span> | <span data-ttu-id="d92ae-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d92ae-111">Type</span></span>   | <span data-ttu-id="d92ae-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="d92ae-112">Default</span></span> | <span data-ttu-id="d92ae-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d92ae-113">Description</span></span>                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d92ae-114">Vol</span><span class="sxs-lookup"><span data-stu-id="d92ae-114">Vol</span></span>      | <span data-ttu-id="d92ae-115">double</span><span class="sxs-lookup"><span data-stu-id="d92ae-115">double</span></span> | <span data-ttu-id="d92ae-116">1,0</span><span class="sxs-lookup"><span data-stu-id="d92ae-116">1.0</span></span>     | <span data-ttu-id="d92ae-117">Volumen, como porcentaje del volumen creado.</span><span class="sxs-lookup"><span data-stu-id="d92ae-117">Volume, as a percentage of the authored volume.</span></span> <span data-ttu-id="d92ae-118">Puede producir fundidos de audio modificando este valor de propiedad a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="d92ae-118">You can produce audio fades by varying this property value over time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d92ae-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d92ae-119">Remarks</span></span>

<span data-ttu-id="d92ae-120">Cada objeto de una escala de tiempo puede tener como máximo un efecto de sobre de volumen.</span><span class="sxs-lookup"><span data-stu-id="d92ae-120">Each object in a timeline can have at most one volume envelope effect.</span></span> <span data-ttu-id="d92ae-121">En una composición o un grupo, el sobre del volumen se aplica primero, antes que cualquier otro efecto de audio, independientemente de su prioridad.</span><span class="sxs-lookup"><span data-stu-id="d92ae-121">In a composition or a group, the volume envelope is applied first, before any other audio effects, regardless of its priority.</span></span> <span data-ttu-id="d92ae-122">En un origen o una pista, el efecto de volumen se aplica en función de su prioridad.</span><span class="sxs-lookup"><span data-stu-id="d92ae-122">In a source or a track, the volume effect is applied according to its priority.</span></span>

 

 



