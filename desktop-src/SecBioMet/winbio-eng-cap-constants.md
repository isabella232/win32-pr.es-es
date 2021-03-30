---
title: Constantes de WINBIO_ENG_CAP (Winbio \_ Types. h)
description: Especifique las capacidades del motor genérico.
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d69db9f0e15ca0d50aa5ca134fdc74904dec85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803907"
---
# <a name="winbio_eng_cap-constants"></a><span data-ttu-id="1af59-103">WINBIO \_ constantes de Cap de ENG \_</span><span class="sxs-lookup"><span data-stu-id="1af59-103">WINBIO\_ENG\_CAP Constants</span></span>

<span data-ttu-id="1af59-104">Las siguientes constantes son valores **de \_ funcionalidad de WINBIO** que se pueden usar para especificar las capacidades genéricas del componente del motor que está conectado a una unidad biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="1af59-104">The following constants are **WINBIO\_CAPABILITIES** values that can be used to specify generic capabilities of the engine component that is connected to a specific biometric unit.</span></span> <span data-ttu-id="1af59-105">Estas funcionalidades se especifican en el miembro **GenericEngineCapabilities** de la estructura de [**\_ \_ \_ información del motor extendido WINBIO**](winbio-extended-engine-info.md) .</span><span class="sxs-lookup"><span data-stu-id="1af59-105">You specify these capabilities in **GenericEngineCapabilities** member of the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure.</span></span>



| <span data-ttu-id="1af59-106">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="1af59-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="1af59-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1af59-107">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <span data-ttu-id="1af59-108"><dt>**WINBIO \_ \_ \_ \_ Mejora iterativa de Cap de ENG**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1af59-108"><dt>**WINBIO\_ENG\_CAP\_ITERATIVE\_IMPROVEMENT**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="1af59-109">El componente del motor biométrico puede realizar una mejora iterativa.</span><span class="sxs-lookup"><span data-stu-id="1af59-109">The biometric engine component can perform iterative improvement.</span></span><br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <span data-ttu-id="1af59-110"><dt>**WINBIO \_ \_Detección de \_ simulación \_ de Cap de ENG**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1af59-110"><dt>**WINBIO\_ENG\_CAP\_SPOOF\_DETECTION**</dt> <dt>0x00000002</dt></span></span> </dl>                   | <span data-ttu-id="1af59-111">El componente del motor biométrico puede realizar la detección de suplantaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="1af59-111">The biometric engine component can perform spoof detection.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="1af59-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1af59-112">Requirements</span></span>



| <span data-ttu-id="1af59-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af59-113">Requirement</span></span> | <span data-ttu-id="1af59-114">Value</span><span class="sxs-lookup"><span data-stu-id="1af59-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1af59-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1af59-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1af59-116">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="1af59-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="1af59-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1af59-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1af59-118">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="1af59-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1af59-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1af59-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1af59-120"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1af59-120"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





