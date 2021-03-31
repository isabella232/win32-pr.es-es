---
description: Define los diferentes Estados de error de la extensión de origen de medios.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: Enumeración MF_MSE_ERROR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155564"
---
# <a name="mf_mse_error-enumeration"></a><span data-ttu-id="bc5db-103">\_Enumeración de errores de MF MSE \_</span><span class="sxs-lookup"><span data-stu-id="bc5db-103">MF\_MSE\_ERROR enumeration</span></span>

<span data-ttu-id="bc5db-104">Define los diferentes Estados de error de la extensión de origen de medios.</span><span class="sxs-lookup"><span data-stu-id="bc5db-104">Defines the different error states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc5db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc5db-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a><span data-ttu-id="bc5db-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bc5db-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bc5db-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF \_ MSE \_ ERROR \_ NoError**</span><span class="sxs-lookup"><span data-stu-id="bc5db-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF\_MSE\_ERROR\_NOERROR**</span></span>
</dt> <dd>

<span data-ttu-id="bc5db-108">No especifica ningún error.</span><span class="sxs-lookup"><span data-stu-id="bc5db-108">Specifies no error.</span></span>

</dd> <dt>

<span data-ttu-id="bc5db-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**red de error de MF \_ MSE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bc5db-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF\_MSE\_ERROR\_NETWORK**</span></span>
</dt> <dd>

<span data-ttu-id="bc5db-110">Especifica un error con la red.</span><span class="sxs-lookup"><span data-stu-id="bc5db-110">Specifies an error with the network.</span></span>

</dd> <dt>

<span data-ttu-id="bc5db-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**\_ \_ error al \_ descodificar MF MSE**</span><span class="sxs-lookup"><span data-stu-id="bc5db-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**MF\_MSE\_ERROR\_DECODE**</span></span>
</dt> <dd>

<span data-ttu-id="bc5db-112">Especifica un error con la descodificación.</span><span class="sxs-lookup"><span data-stu-id="bc5db-112">Specifies an error with decoding.</span></span>

</dd> <dt>

<span data-ttu-id="bc5db-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**error \_ desconocido de el MSE de MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bc5db-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF\_MSE\_ERROR\_UNKNOWN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="bc5db-114">Especifica un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="bc5db-114">Specifies an unknown error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc5db-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc5db-115">Requirements</span></span>



| <span data-ttu-id="bc5db-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc5db-116">Requirement</span></span> | <span data-ttu-id="bc5db-117">Value</span><span class="sxs-lookup"><span data-stu-id="bc5db-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc5db-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc5db-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bc5db-119">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="bc5db-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bc5db-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc5db-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bc5db-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc5db-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bc5db-122">IDL</span><span class="sxs-lookup"><span data-stu-id="bc5db-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc5db-123"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc5db-123"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc5db-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc5db-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc5db-125">Enumeraciones de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bc5db-125">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




