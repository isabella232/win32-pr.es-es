---
description: Indica que se ha alcanzado el final de la secuencia de medios.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: 'IMFMediaSourceExtension:: SetEndOfStream (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717373"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a><span data-ttu-id="ea041-103">IMFMediaSourceExtension:: SetEndOfStream (método)</span><span class="sxs-lookup"><span data-stu-id="ea041-103">IMFMediaSourceExtension::SetEndOfStream method</span></span>

<span data-ttu-id="ea041-104">Indica que se ha alcanzado el final de la secuencia de medios.</span><span class="sxs-lookup"><span data-stu-id="ea041-104">Indicate that the end of the media stream has been reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea041-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea041-105">Syntax</span></span>


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a><span data-ttu-id="ea041-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea041-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea041-107">*error* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ea041-107">*error* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea041-108">Se usa para pasar información de error.</span><span class="sxs-lookup"><span data-stu-id="ea041-108">Used to pass error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea041-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea041-109">Return value</span></span>

<span data-ttu-id="ea041-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ea041-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ea041-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ea041-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea041-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea041-112">Requirements</span></span>



| <span data-ttu-id="ea041-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea041-113">Requirement</span></span> | <span data-ttu-id="ea041-114">Value</span><span class="sxs-lookup"><span data-stu-id="ea041-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea041-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea041-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ea041-116">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="ea041-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ea041-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea041-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ea041-118">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea041-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ea041-119">IDL</span><span class="sxs-lookup"><span data-stu-id="ea041-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea041-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea041-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea041-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea041-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea041-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="ea041-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[<span data-ttu-id="ea041-123">**\_error de MSE de MF \_**</span><span class="sxs-lookup"><span data-stu-id="ea041-123">**MF\_MSE\_ERROR**</span></span>](mf-mse-error.md)
</dt> </dl>

 

 




