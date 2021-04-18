---
description: Quita los segmentos multimedia definidos por el intervalo de tiempo especificado de IMFSourceBuffer.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: 'IMFSourceBuffer:: Remove (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: d82660d08efe651b321672b6ccd0cb475875beee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715437"
---
# <a name="imfsourcebufferremove-method"></a><span data-ttu-id="159eb-103">IMFSourceBuffer:: Remove (método)</span><span class="sxs-lookup"><span data-stu-id="159eb-103">IMFSourceBuffer::Remove method</span></span>

<span data-ttu-id="159eb-104">Quita los segmentos multimedia definidos por el intervalo de tiempo especificado de [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="159eb-104">Removes the media segments defined by the specified time range from the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="159eb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="159eb-105">Syntax</span></span>


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a><span data-ttu-id="159eb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="159eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="159eb-107">*iniciar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="159eb-107">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="159eb-108">Inicio del intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="159eb-108">The start of the time range.</span></span>

</dd> <dt>

<span data-ttu-id="159eb-109">*fin* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="159eb-109">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="159eb-110">Final del intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="159eb-110">The end of the time range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="159eb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="159eb-111">Return value</span></span>

<span data-ttu-id="159eb-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="159eb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="159eb-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="159eb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="159eb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="159eb-114">Requirements</span></span>



| <span data-ttu-id="159eb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="159eb-115">Requirement</span></span> | <span data-ttu-id="159eb-116">Value</span><span class="sxs-lookup"><span data-stu-id="159eb-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="159eb-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="159eb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="159eb-118">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="159eb-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="159eb-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="159eb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="159eb-120">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="159eb-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="159eb-121">IDL</span><span class="sxs-lookup"><span data-stu-id="159eb-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="159eb-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="159eb-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="159eb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="159eb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159eb-124">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="159eb-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




