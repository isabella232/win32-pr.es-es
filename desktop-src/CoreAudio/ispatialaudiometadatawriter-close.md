---
description: Completa cualquier operación necesaria en el búfer de metadatos y libera el objeto ISpatialAudioMetadataItems especificado.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'ISpatialAudioMetadataWriter:: Close (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153343"
---
# <a name="ispatialaudiometadatawriterclose-method"></a><span data-ttu-id="11a1d-103">ISpatialAudioMetadataWriter:: Close (método)</span><span class="sxs-lookup"><span data-stu-id="11a1d-103">ISpatialAudioMetadataWriter::Close method</span></span>

<span data-ttu-id="11a1d-104">Completa cualquier operación necesaria en el búfer de metadatos y libera el objeto [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) especificado.</span><span class="sxs-lookup"><span data-stu-id="11a1d-104">Completes any needed operations on the metadata buffer and releases the specified [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a1d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11a1d-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="11a1d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11a1d-106">Parameters</span></span>

<span data-ttu-id="11a1d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="11a1d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11a1d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11a1d-108">Return value</span></span>

<span data-ttu-id="11a1d-109">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="11a1d-109">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="11a1d-110">Si se produce un error, los códigos de retorno posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="11a1d-110">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="11a1d-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="11a1d-111">Return code</span></span>                                                                                                                     | <span data-ttu-id="11a1d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="11a1d-112">Description</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11a1d-113"><dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ no hay ningún \_ elemento \_ abierto**</dt></span><span class="sxs-lookup"><span data-stu-id="11a1d-113"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_OPEN**</dt></span></span> </dl>            | <span data-ttu-id="11a1d-114">El [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) proporcionado no se ha abierto con una llamada a [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span><span class="sxs-lookup"><span data-stu-id="11a1d-114">The supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) has not been opened with a call to [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span></span><br/> |
| <dl> <span data-ttu-id="11a1d-115"><dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ no hay \_ elementos \_ escritos**</dt></span><span class="sxs-lookup"><span data-stu-id="11a1d-115"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_WRITTEN**</dt></span></span> </dl>         | <span data-ttu-id="11a1d-116">No se ha escrito ningún elemento de metadatos en el [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)proporcionado.</span><span class="sxs-lookup"><span data-stu-id="11a1d-116">No metadata items have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                              |
| <dl> <span data-ttu-id="11a1d-117"><dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ Item \_ deben \_ tener \_ comandos**</dt></span><span class="sxs-lookup"><span data-stu-id="11a1d-117"><dt>**SPTLAUD\_MD\_CLNT\_E\_ITEM\_MUST\_HAVE\_COMMANDS**</dt></span></span> </dl> | <span data-ttu-id="11a1d-118">No se han escrito comandos de metadatos en el [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)proporcionado.</span><span class="sxs-lookup"><span data-stu-id="11a1d-118">No metadata commands have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                           |



 

## <a name="see-also"></a><span data-ttu-id="11a1d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="11a1d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a1d-120">**ISpatialAudioMetadataWriter**</span><span class="sxs-lookup"><span data-stu-id="11a1d-120">**ISpatialAudioMetadataWriter**</span></span>](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




