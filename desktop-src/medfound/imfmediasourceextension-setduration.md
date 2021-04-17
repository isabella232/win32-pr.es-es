---
description: Establece la duración del origen del medio en unidades de 100-nanosegundos.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'IMFMediaSourceExtension:: SetDuration (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697957"
---
# <a name="imfmediasourceextensionsetduration-method"></a><span data-ttu-id="e5d57-103">IMFMediaSourceExtension:: SetDuration (método)</span><span class="sxs-lookup"><span data-stu-id="e5d57-103">IMFMediaSourceExtension::SetDuration method</span></span>

<span data-ttu-id="e5d57-104">Establece la duración del origen del medio en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="e5d57-104">Sets the duration of the media source in 100-nanosecond units.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d57-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5d57-105">Syntax</span></span>


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a><span data-ttu-id="e5d57-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5d57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d57-107">*duración* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e5d57-107">*duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d57-108">La duración del origen del medio en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="e5d57-108">The duration of the media source in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5d57-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5d57-109">Return value</span></span>

<span data-ttu-id="e5d57-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e5d57-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e5d57-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e5d57-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d57-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5d57-112">Requirements</span></span>



| <span data-ttu-id="e5d57-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5d57-113">Requirement</span></span> | <span data-ttu-id="e5d57-114">Value</span><span class="sxs-lookup"><span data-stu-id="e5d57-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d57-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5d57-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d57-116">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="e5d57-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e5d57-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5d57-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d57-118">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e5d57-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e5d57-119">IDL</span><span class="sxs-lookup"><span data-stu-id="e5d57-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5d57-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5d57-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5d57-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5d57-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d57-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="e5d57-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




