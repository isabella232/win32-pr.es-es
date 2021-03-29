---
description: GUID definido por el descodificador que identifica el formato de metadatos de audio espacial, y notifica a los componentes de nivel inferior del tipo de objeto de metadatos que el descodificador generará.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277078"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a><span data-ttu-id="adb7e-103">\_Atributo de \_ \_ identificador de \_ \_ formato de metadatos del objeto de audio \_ espacial \_ MF MT</span><span class="sxs-lookup"><span data-stu-id="adb7e-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_FORMAT\_ID attribute</span></span>

<span data-ttu-id="adb7e-104">GUID definido por el descodificador que identifica el formato de metadatos de audio espacial, y notifica a los componentes de nivel inferior del tipo de objeto de metadatos que el descodificador generará.</span><span class="sxs-lookup"><span data-stu-id="adb7e-104">A decoder-defined GUID that identifies the spatial audio metadata format, notifying downstream components of the metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="adb7e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="adb7e-105">Data type</span></span>

<span data-ttu-id="adb7e-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="adb7e-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="adb7e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="adb7e-107">Remarks</span></span>

<span data-ttu-id="adb7e-108">El BLOB de metadatos con el formato especificado se escribe mediante la interfaz [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) y se lee mediante la interfaz [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) .</span><span class="sxs-lookup"><span data-stu-id="adb7e-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="adb7e-109">El BLOB de metadatos es opaco para la canalización Media Foundation y los componentes.</span><span class="sxs-lookup"><span data-stu-id="adb7e-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="adb7e-110">El atributo se aplica al tipo de medio de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="adb7e-110">The attribute is applied to the spatial audio media type.</span></span> <span data-ttu-id="adb7e-111">Si un componente de nivel inferior no admite el formato de metadatos especificado por el GUID, el componente debe rechazar el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="adb7e-111">If a downstream component does not support the metadata format specified by the GUID, the component should reject the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="adb7e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adb7e-112">Requirements</span></span>



| <span data-ttu-id="adb7e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="adb7e-113">Requirement</span></span> | <span data-ttu-id="adb7e-114">Value</span><span class="sxs-lookup"><span data-stu-id="adb7e-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="adb7e-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="adb7e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="adb7e-116">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="adb7e-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="adb7e-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="adb7e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="adb7e-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="adb7e-118">None supported</span></span><br/>                                                          |
| <span data-ttu-id="adb7e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="adb7e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="adb7e-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="adb7e-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
