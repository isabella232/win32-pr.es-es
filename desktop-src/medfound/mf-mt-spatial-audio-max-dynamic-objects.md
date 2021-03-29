---
description: Especifica el número máximo de objetos de audio dinámicos que se pueden representar mediante el punto de conexión de audio simulataneously.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648418"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a><span data-ttu-id="214c6-103">\_Atributo de \_ \_ \_ \_ objetos dinámicos Max MT Spatial audio \_</span><span class="sxs-lookup"><span data-stu-id="214c6-103">MF\_MT\_SPATIAL\_AUDIO\_MAX\_DYNAMIC\_OBJECTS attribute</span></span>

<span data-ttu-id="214c6-104">Especifica el número máximo de objetos de audio dinámicos que se pueden representar mediante el punto de conexión de audio simulataneously.</span><span class="sxs-lookup"><span data-stu-id="214c6-104">Specifies the maximum number of dynamic audio objects that can be rendered by the audio endpoint simulataneously.</span></span>

## <a name="data-type"></a><span data-ttu-id="214c6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="214c6-105">Data type</span></span>

<span data-ttu-id="214c6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="214c6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="214c6-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="214c6-107">Remarks</span></span>

<span data-ttu-id="214c6-108">Un [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) puede contener menos muestras que el número especificado por este atributo.</span><span class="sxs-lookup"><span data-stu-id="214c6-108">An [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) may contain fewer samples than the number specified by this attribute.</span></span> <span data-ttu-id="214c6-109">Si un ejemplo contiene más objetos de audio de los especificados por este atributo, el comportamiento es indefinido.</span><span class="sxs-lookup"><span data-stu-id="214c6-109">If a sample contains more audio objects than specified by this attribute, the behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="214c6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="214c6-110">Requirements</span></span>



| <span data-ttu-id="214c6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="214c6-111">Requirement</span></span> | <span data-ttu-id="214c6-112">Value</span><span class="sxs-lookup"><span data-stu-id="214c6-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="214c6-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="214c6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="214c6-114">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="214c6-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="214c6-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="214c6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="214c6-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="214c6-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="214c6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="214c6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="214c6-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="214c6-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




