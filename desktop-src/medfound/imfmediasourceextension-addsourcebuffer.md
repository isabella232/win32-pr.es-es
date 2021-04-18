---
description: Agrega un IMFSourceBuffer a la colección de búferes asociados a IMFMediaSourceExtension.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: 'IMFMediaSourceExtension:: AddSourceBuffer (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: a62a62d8cf11afaa0190ac442f84b00cfe23517b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707551"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a><span data-ttu-id="2c971-103">IMFMediaSourceExtension:: AddSourceBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="2c971-103">IMFMediaSourceExtension::AddSourceBuffer method</span></span>

<span data-ttu-id="2c971-104">Agrega un [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) a la colección de búferes asociados a [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span><span class="sxs-lookup"><span data-stu-id="2c971-104">Adds a [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) to the collection of buffers associated with the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c971-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c971-105">Syntax</span></span>


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="2c971-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c971-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c971-107">*tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2c971-107">*type* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="2c971-108">*pNotify* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c971-108">*pNotify* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="2c971-109">*ppSourceBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2c971-109">*ppSourceBuffer* \[out\]</span></span>
<span data-ttu-id="2c971-110"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2c971-110"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="2c971-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c971-111">Return value</span></span>

<span data-ttu-id="2c971-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2c971-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2c971-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2c971-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c971-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c971-114">Requirements</span></span>



| <span data-ttu-id="2c971-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c971-115">Requirement</span></span> | <span data-ttu-id="2c971-116">Value</span><span class="sxs-lookup"><span data-stu-id="2c971-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c971-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c971-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2c971-118">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="2c971-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2c971-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c971-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2c971-120">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c971-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2c971-121">IDL</span><span class="sxs-lookup"><span data-stu-id="2c971-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c971-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c971-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c971-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c971-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c971-124">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="2c971-124">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




