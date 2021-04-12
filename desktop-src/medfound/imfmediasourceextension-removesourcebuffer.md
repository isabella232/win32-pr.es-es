---
description: Quita el búfer de origen especificado de la colección de búferes de origen administrados por el objeto IMFMediaSourceExtension.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: 'IMFMediaSourceExtension:: RemoveSourceBuffer (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2a093401058895f31b29843778a18a040e722c33
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361902"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a><span data-ttu-id="cebf2-103">IMFMediaSourceExtension:: RemoveSourceBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="cebf2-103">IMFMediaSourceExtension::RemoveSourceBuffer method</span></span>

<span data-ttu-id="cebf2-104">Quita el búfer de origen especificado de la colección de búferes de origen administrados por el objeto [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) .</span><span class="sxs-lookup"><span data-stu-id="cebf2-104">Removes the specified source buffer from the collection of source buffers managed by the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cebf2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cebf2-105">Syntax</span></span>


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="cebf2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cebf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cebf2-107">*pSourceBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cebf2-107">*pSourceBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cebf2-108">Búfer que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="cebf2-108">The buffer to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cebf2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cebf2-109">Return value</span></span>

<span data-ttu-id="cebf2-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="cebf2-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cebf2-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cebf2-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cebf2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cebf2-112">Requirements</span></span>



| <span data-ttu-id="cebf2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cebf2-113">Requirement</span></span> | <span data-ttu-id="cebf2-114">Value</span><span class="sxs-lookup"><span data-stu-id="cebf2-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cebf2-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cebf2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cebf2-116">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="cebf2-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cebf2-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cebf2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cebf2-118">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cebf2-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cebf2-119">IDL</span><span class="sxs-lookup"><span data-stu-id="cebf2-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cebf2-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cebf2-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cebf2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="cebf2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cebf2-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="cebf2-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




