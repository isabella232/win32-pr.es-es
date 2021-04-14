---
title: Infracción de subprocesamiento de D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Se tuvo acceso a una interfaz de subprocesos de alquiler simultáneamente desde varios subprocesos.
keywords:
- D1105 infracción de subprocesos Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105661450"
---
# <a name="d1105-threading-violation"></a><span data-ttu-id="db5d3-104">D1105: infracción de subprocesos</span><span class="sxs-lookup"><span data-stu-id="db5d3-104">D1105: Threading Violation</span></span>

<span data-ttu-id="db5d3-105">Se tuvo acceso simultáneamente a una interfaz de interfaz de subprocesos \[  \] de alquiler desde varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="db5d3-105">A rental threaded interface \[*interface*\] was simultaneously accessed from multiple threads.</span></span>

## <a name="placeholders"></a><span data-ttu-id="db5d3-106">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="db5d3-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="db5d3-107"><span id="interface"></span><span id="INTERFACE"></span>*interfaz*</span><span class="sxs-lookup"><span data-stu-id="db5d3-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="db5d3-108">Dirección de la interfaz a la que se ha tenido acceso a través de varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="db5d3-108">The address of the interface that was accessed by multiple threads.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="db5d3-109">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="db5d3-109">Possible Causes</span></span>

<span data-ttu-id="db5d3-110">Usar una instancia de objeto del mismo generador de un solo subproceso de dos subprocesos diferentes.</span><span class="sxs-lookup"><span data-stu-id="db5d3-110">Using an object instance from the same single-threaded factory from two different threads.</span></span>

 

 




