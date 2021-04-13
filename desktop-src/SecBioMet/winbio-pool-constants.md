---
title: Constantes de WINBIO_POOL (Winbio \_ Types. h)
description: Especifique el tipo de grupo de unidades biométricas que se va a usar en la sesión.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7af1ec8d5692a390bb91ecb63736bd94efb2e85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535410"
---
# <a name="winbio_pool-constants"></a><span data-ttu-id="8f41a-103">Constantes de grupo de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="8f41a-103">WINBIO\_POOL Constants</span></span>

<span data-ttu-id="8f41a-104">Se pueden usar las siguientes constantes en la función [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar el tipo de grupo de unidades biométricas que se va a usar en la sesión.</span><span class="sxs-lookup"><span data-stu-id="8f41a-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify the type of biometric unit pool to be used in the session.</span></span>



| <span data-ttu-id="8f41a-105">Constante</span><span class="sxs-lookup"><span data-stu-id="8f41a-105">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="8f41a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f41a-106">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="8f41a-107"><dt>**Grupo de WINBIO \_ \_ desconocido**</dt></span><span class="sxs-lookup"><span data-stu-id="8f41a-107"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="8f41a-108">No se conoce el tipo de grupo.</span><span class="sxs-lookup"><span data-stu-id="8f41a-108">The pool type is unknown.</span></span><br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="8f41a-109"><dt>**\_sistema de grupo de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f41a-109"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>             | <span data-ttu-id="8f41a-110">Especifica una colección compartida de unidades biométricas administradas por el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="8f41a-110">Specifies a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="8f41a-111"><dt>**Grupo de WINBIO \_ \_ privado**</dt></span><span class="sxs-lookup"><span data-stu-id="8f41a-111"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl>          | <span data-ttu-id="8f41a-112">Especifica una colección de unidades biométricas administradas por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="8f41a-112">Specifies a collection of biometric units that are managed by the caller.</span></span><br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <span data-ttu-id="8f41a-113"><dt>**Grupo de WINBIO \_ \_ sin asignar**</dt></span><span class="sxs-lookup"><span data-stu-id="8f41a-113"><dt>**WINBIO\_POOL\_UNASSIGNED**</dt></span></span> </dl> | <span data-ttu-id="8f41a-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8f41a-114">Reserved.</span></span><br/>                                                                         |



## <a name="requirements"></a><span data-ttu-id="8f41a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f41a-115">Requirements</span></span>



| <span data-ttu-id="8f41a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f41a-116">Requirement</span></span> | <span data-ttu-id="8f41a-117">Value</span><span class="sxs-lookup"><span data-stu-id="8f41a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f41a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f41a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8f41a-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f41a-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="8f41a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f41a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8f41a-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f41a-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8f41a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f41a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f41a-123"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f41a-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f41a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f41a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f41a-125">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="8f41a-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





