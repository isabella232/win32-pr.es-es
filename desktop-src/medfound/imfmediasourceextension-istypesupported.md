---
description: Obtiene un valor que indica si el origen de medios admite el tipo MIME especificado.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'IMFMediaSourceExtension:: IsTypeSupported (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697958"
---
# <a name="imfmediasourceextensionistypesupported-method"></a><span data-ttu-id="55f56-103">IMFMediaSourceExtension:: IsTypeSupported (método)</span><span class="sxs-lookup"><span data-stu-id="55f56-103">IMFMediaSourceExtension::IsTypeSupported method</span></span>

<span data-ttu-id="55f56-104">Obtiene un valor que indica si el origen de medios admite el tipo MIME especificado.</span><span class="sxs-lookup"><span data-stu-id="55f56-104">Gets a value that indicates if the specified MIME type is supported by the media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f56-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55f56-105">Syntax</span></span>


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a><span data-ttu-id="55f56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55f56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55f56-107">*tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="55f56-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55f56-108">Tipo de medio para el que se va a comprobar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="55f56-108">The media type to check support for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55f56-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55f56-109">Return value</span></span>

<span data-ttu-id="55f56-110">**true** si se admite el tipo de medio; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="55f56-110">**true** if the media type is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f56-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55f56-111">Requirements</span></span>



| <span data-ttu-id="55f56-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="55f56-112">Requirement</span></span> | <span data-ttu-id="55f56-113">Value</span><span class="sxs-lookup"><span data-stu-id="55f56-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="55f56-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55f56-114">Minimum supported client</span></span><br/> | <span data-ttu-id="55f56-115">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="55f56-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55f56-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55f56-116">Minimum supported server</span></span><br/> | <span data-ttu-id="55f56-117">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="55f56-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="55f56-118">IDL</span><span class="sxs-lookup"><span data-stu-id="55f56-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55f56-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55f56-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="55f56-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f56-121">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="55f56-121">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




