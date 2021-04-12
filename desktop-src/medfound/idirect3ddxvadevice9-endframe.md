---
description: Finaliza el procesamiento para crear una imagen descodificada.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'IDirect3DDXVADevice9:: EndFrame (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155189"
---
# <a name="idirect3ddxvadevice9endframe-method"></a><span data-ttu-id="e2ecc-103">IDirect3DDXVADevice9:: EndFrame (método)</span><span class="sxs-lookup"><span data-stu-id="e2ecc-103">IDirect3DDXVADevice9::EndFrame method</span></span>

<span data-ttu-id="e2ecc-104">Finaliza el procesamiento para crear una imagen descodificada.</span><span class="sxs-lookup"><span data-stu-id="e2ecc-104">Ends the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ecc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2ecc-105">Syntax</span></span>


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a><span data-ttu-id="e2ecc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2ecc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2ecc-107">*SizeMiscData*</span><span class="sxs-lookup"><span data-stu-id="e2ecc-107">*SizeMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="e2ecc-108">Tamaño del búfer especificado por *pMiscData*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e2ecc-108">The size of the buffer specified by *pMiscData*, in bytes.</span></span> <span data-ttu-id="e2ecc-109">El valor debe ser 2.</span><span class="sxs-lookup"><span data-stu-id="e2ecc-109">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="e2ecc-110">*pMiscData*</span><span class="sxs-lookup"><span data-stu-id="e2ecc-110">*pMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="e2ecc-111">Puntero a un búfer que contiene datos para el acelerador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e2ecc-111">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="e2ecc-112">Este búfer debe contener el mismo índice de marco que se pasó al método [**IDirect3DDXVADevice9:: BeginFrame**](idirect3ddxvadevice9-beginframe.md) en el parámetro *pInputData* .</span><span class="sxs-lookup"><span data-stu-id="e2ecc-112">This buffer must contain the same frame index that was passed to the [**IDirect3DDXVADevice9::BeginFrame**](idirect3ddxvadevice9-beginframe.md) method in the *pInputData* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2ecc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2ecc-113">Return value</span></span>

<span data-ttu-id="e2ecc-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e2ecc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e2ecc-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e2ecc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ecc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2ecc-116">Requirements</span></span>



| <span data-ttu-id="e2ecc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2ecc-117">Requirement</span></span> | <span data-ttu-id="e2ecc-118">Value</span><span class="sxs-lookup"><span data-stu-id="e2ecc-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e2ecc-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2ecc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2ecc-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e2ecc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2ecc-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2ecc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2ecc-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2ecc-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e2ecc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2ecc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2ecc-124"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ecc-124"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2ecc-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2ecc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ecc-126">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="e2ecc-126">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




