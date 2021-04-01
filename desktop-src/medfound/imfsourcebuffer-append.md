---
description: Anexa el segmento multimedia especificado a IMFSourceBuffer.
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
title: 'IMFSourceBuffer:: Append (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Append
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 00c9b6a0af2e48482311a8a0e1bc39dc4ce951aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275696"
---
# <a name="imfsourcebufferappend-method"></a><span data-ttu-id="84e75-103">IMFSourceBuffer:: Append (método)</span><span class="sxs-lookup"><span data-stu-id="84e75-103">IMFSourceBuffer::Append method</span></span>

<span data-ttu-id="84e75-104">Anexa el segmento multimedia especificado a [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="84e75-104">Appends the specified media segment to the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="84e75-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84e75-105">Syntax</span></span>


```C++
HRESULT Append(
  [in] const BYTE  *pData,
  [in]       DWORD len
);
```



## <a name="parameters"></a><span data-ttu-id="84e75-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84e75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84e75-107">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84e75-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84e75-108">Datos multimedia que se van a anexar.</span><span class="sxs-lookup"><span data-stu-id="84e75-108">The media data to append.</span></span>

</dd> <dt>

<span data-ttu-id="84e75-109">*longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84e75-109">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84e75-110">La longitud de los datos multimedia almacenados en *pdata*.</span><span class="sxs-lookup"><span data-stu-id="84e75-110">The length of the media data stored in *pData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84e75-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84e75-111">Return value</span></span>

<span data-ttu-id="84e75-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="84e75-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="84e75-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="84e75-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="84e75-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84e75-114">Requirements</span></span>



| <span data-ttu-id="84e75-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="84e75-115">Requirement</span></span> | <span data-ttu-id="84e75-116">Value</span><span class="sxs-lookup"><span data-stu-id="84e75-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="84e75-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84e75-117">Minimum supported client</span></span><br/> | <span data-ttu-id="84e75-118">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="84e75-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="84e75-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84e75-119">Minimum supported server</span></span><br/> | <span data-ttu-id="84e75-120">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="84e75-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="84e75-121">IDL</span><span class="sxs-lookup"><span data-stu-id="84e75-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84e75-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84e75-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84e75-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="84e75-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84e75-124">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="84e75-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




