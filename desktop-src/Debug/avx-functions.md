---
description: Funciones de Intel AVX.
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: AVX (funciones)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0b56c83b6beb674bc284b139bb656441956705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274829"
---
# <a name="avx-functions"></a><span data-ttu-id="e0454-103">AVX (funciones)</span><span class="sxs-lookup"><span data-stu-id="e0454-103">AVX Functions</span></span>

<span data-ttu-id="e0454-104">A continuación se muestran las funciones de Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="e0454-104">The following are the Intel AVX functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e0454-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e0454-105">In this section</span></span>



| <span data-ttu-id="e0454-106">Tema</span><span class="sxs-lookup"><span data-stu-id="e0454-106">Topic</span></span>                                                                   | <span data-ttu-id="e0454-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0454-107">Description</span></span>                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0454-108">**CopyContext**</span><span class="sxs-lookup"><span data-stu-id="e0454-108">**CopyContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | <span data-ttu-id="e0454-109">Copia una estructura de contexto de origen (incluido cualquier XState) en una estructura de contexto de destino inicializada.</span><span class="sxs-lookup"><span data-stu-id="e0454-109">Copies a source context structure (including any XState) onto an initialized destination context structure.</span></span><br/>         |
| [<span data-ttu-id="e0454-110">**GetEnabledXStateFeatures**</span><span class="sxs-lookup"><span data-stu-id="e0454-110">**GetEnabledXStateFeatures**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | <span data-ttu-id="e0454-111">Obtiene una máscara de características de XState habilitadas en procesadores x86 o x64.</span><span class="sxs-lookup"><span data-stu-id="e0454-111">Gets a mask of enabled XState features on x86 or x64 processors.</span></span><br/>                                                    |
| [<span data-ttu-id="e0454-112">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="e0454-112">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | <span data-ttu-id="e0454-113">Devuelve la máscara de las características de XState establecidas dentro de una estructura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) .</span><span class="sxs-lookup"><span data-stu-id="e0454-113">Returns the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) structure.</span></span><br/>                        |
| [<span data-ttu-id="e0454-114">**InitializeContext**</span><span class="sxs-lookup"><span data-stu-id="e0454-114">**InitializeContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | <span data-ttu-id="e0454-115">Inicializa una estructura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) dentro de un búfer con el tamaño y la alineación necesarios.</span><span class="sxs-lookup"><span data-stu-id="e0454-115">Initializes a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure inside a buffer with the necessary size and alignment.</span></span><br/>       |
| [<span data-ttu-id="e0454-116">**LocateXStateFeature**</span><span class="sxs-lookup"><span data-stu-id="e0454-116">**LocateXStateFeature**</span></span>](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | <span data-ttu-id="e0454-117">Recupera un puntero al estado del procesador para una característica de XState dentro de una estructura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .</span><span class="sxs-lookup"><span data-stu-id="e0454-117">Retrieves a pointer to the processor state for an XState feature within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/> |
| [<span data-ttu-id="e0454-118">**SetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="e0454-118">**SetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | <span data-ttu-id="e0454-119">Establece la máscara de las características de XState establecidas en una estructura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .</span><span class="sxs-lookup"><span data-stu-id="e0454-119">Sets the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/>                             |



 

 

 




