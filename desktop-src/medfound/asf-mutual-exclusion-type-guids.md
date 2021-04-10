---
description: Los siguientes GUID definen los tipos para el objeto de exclusión mutua de las secuencias de formato ASF (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUID de tipo de exclusión mutua de ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275151"
---
# <a name="asf-mutual-exclusion-type-guids"></a><span data-ttu-id="f8b26-103">GUID de tipo de exclusión mutua de ASF</span><span class="sxs-lookup"><span data-stu-id="f8b26-103">ASF Mutual Exclusion Type GUIDs</span></span>

<span data-ttu-id="f8b26-104">Los siguientes GUID definen los tipos para el objeto de exclusión mutua de las secuencias de formato ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="f8b26-104">The following GUIDs define the types for the mutual exclusion object for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="f8b26-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f8b26-105">Constant</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="f8b26-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8b26-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <span data-ttu-id="f8b26-107"><dt>**\_Lenguaje MFASFMutexType**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b26-107"><dt>**MFASFMutexType\_Language**</dt></span></span> </dl>                 | <span data-ttu-id="f8b26-108">Los flujos se excluyen mutuamente por lenguaje.</span><span class="sxs-lookup"><span data-stu-id="f8b26-108">The streams are mutually exclusive by language.</span></span> <span data-ttu-id="f8b26-109">Este tipo de exclusión mutua es similar a las pistas de audio en un DVD.</span><span class="sxs-lookup"><span data-stu-id="f8b26-109">This type of mutual exclusion is similar to the audio tracks on a DVD.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <span data-ttu-id="f8b26-110"><dt>**\_Velocidad de bits MFASFMutexType**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b26-110"><dt>**MFASFMutexType\_Bitrate**</dt></span></span> </dl>                     | <span data-ttu-id="f8b26-111">Las secuencias se excluyen mutuamente a través de la velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="f8b26-111">The streams are mutually exclusive by bit rate.</span></span> <span data-ttu-id="f8b26-112">Este tipo de exclusión mutua también se denomina exclusión de velocidad de bits múltiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="f8b26-112">This type of mutual exclusion is also called multiple bit rate (MBR) exclusion.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <span data-ttu-id="f8b26-113"><dt>**Presentación de MFASFMutexType \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b26-113"><dt>**MFASFMutexType\_Presentation**</dt></span></span> </dl> | <span data-ttu-id="f8b26-114">Los flujos se excluyen mutuamente mediante presentación.</span><span class="sxs-lookup"><span data-stu-id="f8b26-114">The streams are mutually exclusive by presentation.</span></span> <span data-ttu-id="f8b26-115">Este tipo se puede usar para muchos escenarios, pero solo se debe usar cuando el contenido es el mismo pero tiene un formato diferente.</span><span class="sxs-lookup"><span data-stu-id="f8b26-115">This type can be used for many scenarios, but it should only be used when the content is the same but takes a different form.</span></span> <span data-ttu-id="f8b26-116">Por ejemplo, dos flujos que contienen el mismo vídeo, uno formateado para rellenar la pantalla y el otro que mantiene la relación de aspecto de pantalla panorámica original, se deben hacer mutuamente excluyentes mediante este tipo.</span><span class="sxs-lookup"><span data-stu-id="f8b26-116">For example, two streams containing the same video, one formatted to fill the screen and the other maintaining the original widescreen aspect ratio, should be made mutually exclusive by using this type.</span></span> <span data-ttu-id="f8b26-117">Otro ejemplo son las secuencias que contienen vídeo de la misma escena capturados de distintos ángulos.</span><span class="sxs-lookup"><span data-stu-id="f8b26-117">Another example is streams containing video of the same scene shot from different angles.</span></span><br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <span data-ttu-id="f8b26-118"><dt>**MFASFMutexType \_ desconocido**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b26-118"><dt>**MFASFMutexType\_Unknown**</dt></span></span> </dl>                     | <span data-ttu-id="f8b26-119">Las secuencias se excluyen mutuamente en función de criterios personalizados.</span><span class="sxs-lookup"><span data-stu-id="f8b26-119">The streams are mutually exclusive based on custom criteria.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="f8b26-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8b26-120">Requirements</span></span>



| <span data-ttu-id="f8b26-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8b26-121">Requirement</span></span> | <span data-ttu-id="f8b26-122">Value</span><span class="sxs-lookup"><span data-stu-id="f8b26-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b26-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8b26-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b26-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f8b26-124">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f8b26-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8b26-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b26-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8b26-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f8b26-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8b26-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8b26-128"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8b26-128"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b26-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8b26-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b26-130">**IMFASFMutualExclusion:: GetType**</span><span class="sxs-lookup"><span data-stu-id="f8b26-130">**IMFASFMutualExclusion::GetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[<span data-ttu-id="f8b26-131">**IMFASFMutualExclusion::SetType**</span><span class="sxs-lookup"><span data-stu-id="f8b26-131">**IMFASFMutualExclusion::SetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[<span data-ttu-id="f8b26-132">Constantes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f8b26-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




