---
title: Constantes de WINBIO_ORIENTATION (Winbio \_ Types. h)
description: Las siguientes constantes especifican las posibles orientaciones de cámara que el componente de sensor especifica como obligatorias.
ms.assetid: E44A6F17-5F38-47C7-947B-FB6FB79B1217
topic_type:
- apiref
api_name:
- WINBIO_ORIENTATION_UNSPECIFIED
- WINBIO_ORIENTATION_LANDSCAPE
- WINBIO_ORIENTATION_PORTRAIT
- WINBIO_ORIENTATION_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e5c3a3150819eff6311c03b8cd279fad7dcf398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905649"
---
# <a name="winbio_orientation-constants"></a><span data-ttu-id="27759-103">Constantes de orientación de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="27759-103">WINBIO\_ORIENTATION Constants</span></span>

<span data-ttu-id="27759-104">Las siguientes constantes especifican las posibles orientaciones de cámara que el componente de sensor especifica como obligatorias.</span><span class="sxs-lookup"><span data-stu-id="27759-104">The following constants specify the possible camera orientations that the sensor component specifies as mandatory.</span></span>



| <span data-ttu-id="27759-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="27759-105">Constant/value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="27759-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="27759-106">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span id="WINBIO_ORIENTATION_UNSPECIFIED"></span><span id="winbio_orientation_unspecified"></span><dl> <span data-ttu-id="27759-107"><dt>**WINBIO \_ ORIENTACIÓN no \_ especificada**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="27759-107"><dt>**WINBIO\_ORIENTATION\_UNSPECIFIED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="27759-108">No se ha especificado una orientación obligatoria para la cámara.</span><span class="sxs-lookup"><span data-stu-id="27759-108">A mandatory orientation for the camera is not specified.</span></span><br/> |
| <span id="WINBIO_ORIENTATION_LANDSCAPE"></span><span id="winbio_orientation_landscape"></span><dl> <span data-ttu-id="27759-109"><dt>**WINBIO \_ \_Horizontal de orientación**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="27759-109"><dt>**WINBIO\_ORIENTATION\_LANDSCAPE**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="27759-110">La orientación horizontal es necesaria para la cámara.</span><span class="sxs-lookup"><span data-stu-id="27759-110">The landscape orientation is required for the camera.</span></span><br/>    |
| <span id="WINBIO_ORIENTATION_PORTRAIT"></span><span id="winbio_orientation_portrait"></span><dl> <span data-ttu-id="27759-111"><dt>**WINBIO \_ ORIENTACIÓN \_ vertical**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="27759-111"><dt>**WINBIO\_ORIENTATION\_PORTRAIT**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="27759-112">La orientación vertical es necesaria para la cámara.</span><span class="sxs-lookup"><span data-stu-id="27759-112">The portrait orientation is required for the camera.</span></span><br/>     |
| <span id="WINBIO_ORIENTATION_ANY"></span><span id="winbio_orientation_any"></span><dl> <span data-ttu-id="27759-113"><dt>**WINBIO \_ ORIENTACIÓN \_ cualquiera**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="27759-113"><dt>**WINBIO\_ORIENTATION\_ANY**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="27759-114">Se permite cualquier orientación para la cámara.</span><span class="sxs-lookup"><span data-stu-id="27759-114">Any orientation is permitted for the camera.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="27759-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27759-115">Requirements</span></span>



| <span data-ttu-id="27759-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="27759-116">Requirement</span></span> | <span data-ttu-id="27759-117">Value</span><span class="sxs-lookup"><span data-stu-id="27759-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27759-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27759-118">Minimum supported client</span></span><br/> | <span data-ttu-id="27759-119">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="27759-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="27759-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27759-120">Minimum supported server</span></span><br/> | <span data-ttu-id="27759-121">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="27759-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="27759-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27759-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="27759-123"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="27759-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27759-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="27759-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27759-125">**\_ \_ información del sensor extendido de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="27759-125">**WINBIO\_EXTENDED\_SENSOR\_INFO**</span></span>](winbio-extended-sensor-info.md)
</dt> </dl>

 

 





