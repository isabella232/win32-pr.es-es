---
title: Constantes de WINBIO_PRESENCE_CHANGE (Winbio \_ Types. h)
description: Describe los tipos de cambios que se pueden producir cuando el Plataforma de biometría de Windows supervisa la presencia de individuos.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078972"
---
# <a name="winbio_presence_change-constants"></a><span data-ttu-id="91379-103">WINBIO \_ constantes de cambio de presencia \_</span><span class="sxs-lookup"><span data-stu-id="91379-103">WINBIO\_PRESENCE\_CHANGE Constants</span></span>

<span data-ttu-id="91379-104">Describe los tipos de cambios que se pueden producir cuando el Plataforma de biometría de Windows supervisa la presencia de individuos.</span><span class="sxs-lookup"><span data-stu-id="91379-104">Describes the types of changes that can occur when the Windows Biometric Framework monitors the presence of individuals.</span></span>



| <span data-ttu-id="91379-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="91379-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="91379-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="91379-106">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <span data-ttu-id="91379-107"><dt>**WINBIO \_ Tipo de cambio de presencia \_ \_ \_ desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="91379-107"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="91379-108">Se desconoce el tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="91379-108">The type of event is unknown.</span></span> <span data-ttu-id="91379-109">Este valor se usa para la estructura sin inicializar.</span><span class="sxs-lookup"><span data-stu-id="91379-109">This value is used for the uninitialized structure.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <span data-ttu-id="91379-110"><dt>**WINBIO \_ Tipo de cambio de presencia \_ \_ \_ actualizar \_ todo**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="91379-110"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UPDATE\_ALL**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="91379-111">Proporciona información sobre todas las caras actuales en el fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="91379-111">Provides information about all of the faces current in the camera frame.</span></span><br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <span data-ttu-id="91379-112"><dt>**WINBIO \_ \_Llegada del \_ tipo \_ de cambio de presencia**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="91379-112"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_ARRIVE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="91379-113">Una nueva esfera entró en el marco de la cámara.</span><span class="sxs-lookup"><span data-stu-id="91379-113">A new face entered the camera frame.</span></span><br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <span data-ttu-id="91379-114"><dt>**WINBIO \_ Tipo de cambio de presencia \_ \_ \_ Recognize**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="91379-114"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_RECOGNIZE**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="91379-115">Una esfera coincidía con un usuario inscrito.</span><span class="sxs-lookup"><span data-stu-id="91379-115">A face was matched to an enrolled user.</span></span><br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <span data-ttu-id="91379-116"><dt>**WINBIO \_ Tipo de cambio de presencia en la \_ \_ \_ parte**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="91379-116"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_DEPART**</dt> <dt>4</dt></span></span> </dl>              | <span data-ttu-id="91379-117">Una de las caras detectadas con anterioridad está fuera del marco de la cámara durante un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="91379-117">A previously detected face has been out of the camera frame for a period of time.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <span data-ttu-id="91379-118"><dt>**WINBIO \_ \_Seguimiento de \_ tipo \_ de cambio de presencia**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="91379-118"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_TRACK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="91379-119">Proporciona información sobre las actualizaciones del cuadro de límite y los valores de rechazo de un subconjunto de las caras que están actualmente en el marco de la cámara.</span><span class="sxs-lookup"><span data-stu-id="91379-119">Provides updates information about the bounding box and reject detail values for a subset of the faces that are currently in the camera frame.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="91379-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91379-120">Requirements</span></span>



| <span data-ttu-id="91379-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="91379-121">Requirement</span></span> | <span data-ttu-id="91379-122">Value</span><span class="sxs-lookup"><span data-stu-id="91379-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91379-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91379-123">Minimum supported client</span></span><br/> | <span data-ttu-id="91379-124">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="91379-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="91379-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91379-125">Minimum supported server</span></span><br/> | <span data-ttu-id="91379-126">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="91379-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="91379-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91379-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="91379-128"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="91379-128"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





