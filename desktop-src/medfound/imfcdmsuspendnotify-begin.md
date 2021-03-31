---
description: Indica que se está iniciando el proceso de suspensión y los recursos se deben convertir en un estado coherente.
ms.assetid: 5cf3d249-3d8b-4596-9d8b-e7b95a270eff
title: 'IMFCdmSuspendNotify:: Begin (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.Begin
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 84453a6c846e88a9d6e6c32c5253d97d36e89c7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808396"
---
# <a name="imfcdmsuspendnotifybegin-method"></a><span data-ttu-id="5663b-103">IMFCdmSuspendNotify:: Begin (método)</span><span class="sxs-lookup"><span data-stu-id="5663b-103">IMFCdmSuspendNotify::Begin method</span></span>

<span data-ttu-id="5663b-104">Indica que se está iniciando el proceso de suspensión y los recursos se deben convertir en un estado coherente.</span><span class="sxs-lookup"><span data-stu-id="5663b-104">Indicates that the suspend process is starting and resources should be brought into a consistent state.</span></span>

## <a name="syntax"></a><span data-ttu-id="5663b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5663b-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="5663b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5663b-106">Parameters</span></span>

<span data-ttu-id="5663b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5663b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5663b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5663b-108">Return value</span></span>

<span data-ttu-id="5663b-109">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5663b-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5663b-110">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5663b-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5663b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5663b-111">Requirements</span></span>



| <span data-ttu-id="5663b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5663b-112">Requirement</span></span> | <span data-ttu-id="5663b-113">Value</span><span class="sxs-lookup"><span data-stu-id="5663b-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5663b-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5663b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5663b-115">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="5663b-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5663b-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5663b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5663b-117">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5663b-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5663b-118">IDL</span><span class="sxs-lookup"><span data-stu-id="5663b-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5663b-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5663b-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5663b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5663b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5663b-121">**IMFCdmSuspendNotify**</span><span class="sxs-lookup"><span data-stu-id="5663b-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




