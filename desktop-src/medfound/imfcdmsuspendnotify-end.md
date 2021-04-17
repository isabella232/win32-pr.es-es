---
description: La suspensión real está a punto de producirse y no se realizarán más llamadas en el módulo de descifrado de contenido (CDM).
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: 'IMFCdmSuspendNotify:: end (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.End
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71843b53fa85fded646fe71f2caa463a71c9415f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715883"
---
# <a name="imfcdmsuspendnotifyend-method"></a><span data-ttu-id="1e1b3-103">IMFCdmSuspendNotify:: end (método)</span><span class="sxs-lookup"><span data-stu-id="1e1b3-103">IMFCdmSuspendNotify::End method</span></span>

<span data-ttu-id="1e1b3-104">La suspensión real está a punto de producirse y no se realizarán más llamadas en el módulo de descifrado de contenido (CDM).</span><span class="sxs-lookup"><span data-stu-id="1e1b3-104">The actual suspend is about to occur and no more calls will be made into the Content Decryption Module (CDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e1b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e1b3-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="1e1b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e1b3-106">Parameters</span></span>

<span data-ttu-id="1e1b3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1e1b3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e1b3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e1b3-108">Return value</span></span>

<span data-ttu-id="1e1b3-109">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1e1b3-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e1b3-110">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e1b3-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e1b3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e1b3-111">Requirements</span></span>



| <span data-ttu-id="1e1b3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e1b3-112">Requirement</span></span> | <span data-ttu-id="1e1b3-113">Value</span><span class="sxs-lookup"><span data-stu-id="1e1b3-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e1b3-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e1b3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1e1b3-115">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="1e1b3-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1e1b3-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e1b3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1e1b3-117">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e1b3-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1e1b3-118">IDL</span><span class="sxs-lookup"><span data-stu-id="1e1b3-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e1b3-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e1b3-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e1b3-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e1b3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e1b3-121">**IMFCdmSuspendNotify**</span><span class="sxs-lookup"><span data-stu-id="1e1b3-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




