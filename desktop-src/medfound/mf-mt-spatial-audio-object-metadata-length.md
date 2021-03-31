---
description: Valor que especifica el tamaño, en bytes, del tipo de objeto de metadatos de audio espacial que el descodificador generará.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2cd0b3cab788dbc724ab896d2cbfeb0d42f633f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277077"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a><span data-ttu-id="e7b8d-103">\_Atributo de \_ \_ longitud de \_ metadatos de objetos de audio espacial \_ MF MT \_</span><span class="sxs-lookup"><span data-stu-id="e7b8d-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_LENGTH attribute</span></span>

<span data-ttu-id="e7b8d-104">Valor que especifica el tamaño, en bytes, del tipo de objeto de metadatos de audio espacial que el descodificador generará.</span><span class="sxs-lookup"><span data-stu-id="e7b8d-104">A value specifying the size, in bytes, of the spatial audio metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="e7b8d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e7b8d-105">Data type</span></span>

<span data-ttu-id="e7b8d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e7b8d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b8d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7b8d-107">Remarks</span></span>

<span data-ttu-id="e7b8d-108">El BLOB de metadatos con el formato especificado se escribe mediante la interfaz [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) y se lee mediante la interfaz [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) .</span><span class="sxs-lookup"><span data-stu-id="e7b8d-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="e7b8d-109">El BLOB de metadatos es opaco para la canalización Media Foundation y los componentes.</span><span class="sxs-lookup"><span data-stu-id="e7b8d-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="e7b8d-110">El atributo se aplica al tipo de medio de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="e7b8d-110">The attribute is applied to the spatial audio media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b8d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7b8d-111">Requirements</span></span>



| <span data-ttu-id="e7b8d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b8d-112">Requirement</span></span> | <span data-ttu-id="e7b8d-113">Value</span><span class="sxs-lookup"><span data-stu-id="e7b8d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b8d-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7b8d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b8d-115">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7b8d-115">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e7b8d-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7b8d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b8d-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e7b8d-117">None supported</span></span><br/>                                                          |
| <span data-ttu-id="e7b8d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7b8d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7b8d-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b8d-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
