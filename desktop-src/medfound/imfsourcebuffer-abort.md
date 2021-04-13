---
description: Anula el procesamiento del segmento multimedia actual.
ms.assetid: 31253d0d-c53f-47bd-823a-fc564cb63b78
title: 'IMFSourceBuffer:: ABORT (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Abort
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 3a8b5115032fb918af66094bb87c7118eb503da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543598"
---
# <a name="imfsourcebufferabort-method"></a><span data-ttu-id="a2d6f-103">IMFSourceBuffer:: ABORT (método)</span><span class="sxs-lookup"><span data-stu-id="a2d6f-103">IMFSourceBuffer::Abort method</span></span>

<span data-ttu-id="a2d6f-104">Anula el procesamiento del segmento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="a2d6f-104">Aborts the processing of the current media segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d6f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2d6f-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="a2d6f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2d6f-106">Parameters</span></span>

<span data-ttu-id="a2d6f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2d6f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2d6f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2d6f-108">Return value</span></span>

<span data-ttu-id="a2d6f-109">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a2d6f-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a2d6f-110">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a2d6f-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2d6f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2d6f-111">Requirements</span></span>



| <span data-ttu-id="a2d6f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2d6f-112">Requirement</span></span> | <span data-ttu-id="a2d6f-113">Value</span><span class="sxs-lookup"><span data-stu-id="a2d6f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d6f-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2d6f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a2d6f-115">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="a2d6f-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a2d6f-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2d6f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a2d6f-117">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2d6f-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a2d6f-118">IDL</span><span class="sxs-lookup"><span data-stu-id="a2d6f-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2d6f-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2d6f-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2d6f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2d6f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d6f-121">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="a2d6f-121">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




