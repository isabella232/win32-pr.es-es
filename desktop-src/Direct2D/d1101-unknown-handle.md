---
title: D1101 identificador desconocido
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: Se le ha pasado una interfaz no asignada por este archivo DLL.
keywords:
- D1101 identificador desconocido de Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105661452"
---
# <a name="d1101-unknown-handle"></a><span data-ttu-id="3164e-104">D1101: identificador desconocido</span><span class="sxs-lookup"><span data-stu-id="3164e-104">D1101: Unknown Handle</span></span>

<span data-ttu-id="3164e-105">\[  \] Se le ha pasado una interfaz de interfaz no asignada por este archivo dll.</span><span class="sxs-lookup"><span data-stu-id="3164e-105">An interface \[*interface*\] not allocated by this DLL was passed to it.</span></span>

## <a name="placeholders"></a><span data-ttu-id="3164e-106">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="3164e-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="3164e-107"><span id="interface"></span><span id="INTERFACE"></span>*interfaz*</span><span class="sxs-lookup"><span data-stu-id="3164e-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="3164e-108">Dirección de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="3164e-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="3164e-109">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="3164e-109">Possible Causes</span></span>

<span data-ttu-id="3164e-110">Uso de recursos no válido.</span><span class="sxs-lookup"><span data-stu-id="3164e-110">Invalid resource usage.</span></span> <span data-ttu-id="3164e-111">El recurso creado fuera de Direct2D se usa con un generador de Direct2D o los recursos creados en un generador se usaban con un recurso creado por otro generador.</span><span class="sxs-lookup"><span data-stu-id="3164e-111">The resource created outside of Direct2D is used with a Direct2D factory, or the resources created on one factory was used with a resource created by another factory.</span></span>

 

 




