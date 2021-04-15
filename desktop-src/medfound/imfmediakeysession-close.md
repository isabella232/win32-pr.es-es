---
description: Cierra la sesión de la clave multimedia y se debe llamar antes de que se libere la sesión de clave.
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: 'IMFMediaKeySession:: Close (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 16e6efbe27c411c38dca92d12e05fe9395c4946b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689626"
---
# <a name="imfmediakeysessionclose-method"></a><span data-ttu-id="1e569-103">IMFMediaKeySession:: Close (método)</span><span class="sxs-lookup"><span data-stu-id="1e569-103">IMFMediaKeySession::Close method</span></span>

<span data-ttu-id="1e569-104">Cierra la sesión de la clave multimedia y se debe llamar antes de que se libere la sesión de clave.</span><span class="sxs-lookup"><span data-stu-id="1e569-104">Closes the media key session and must be called before the key session is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e569-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e569-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="1e569-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e569-106">Parameters</span></span>

<span data-ttu-id="1e569-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1e569-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e569-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e569-108">Return value</span></span>

<span data-ttu-id="1e569-109">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1e569-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e569-110">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e569-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e569-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e569-111">Requirements</span></span>



| <span data-ttu-id="1e569-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e569-112">Requirement</span></span> | <span data-ttu-id="1e569-113">Value</span><span class="sxs-lookup"><span data-stu-id="1e569-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e569-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e569-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1e569-115">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="1e569-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1e569-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e569-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1e569-117">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e569-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1e569-118">IDL</span><span class="sxs-lookup"><span data-stu-id="1e569-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e569-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e569-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e569-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e569-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e569-121">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="1e569-121">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




