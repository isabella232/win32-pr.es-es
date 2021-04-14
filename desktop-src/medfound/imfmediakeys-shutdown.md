---
description: 'Más información sobre: IMFMediaKeys:: Shutdown (método)'
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
title: 'IMFMediaKeys:: Shutdown (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.Shutdown
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9fcee861b53aaf0c9fda2c6265f50fcee60f674c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361912"
---
# <a name="imfmediakeysshutdown-method"></a><span data-ttu-id="a9394-103">IMFMediaKeys:: Shutdown (método)</span><span class="sxs-lookup"><span data-stu-id="a9394-103">IMFMediaKeys::Shutdown method</span></span>

## <a name="syntax"></a><span data-ttu-id="a9394-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9394-104">Syntax</span></span>


```C++
HRESULT Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="a9394-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9394-105">Parameters</span></span>

<span data-ttu-id="a9394-106">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a9394-106">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9394-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9394-107">Return value</span></span>

<span data-ttu-id="a9394-108">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a9394-108">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9394-109">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a9394-109">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9394-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9394-110">Remarks</span></span>

<span data-ttu-id="a9394-111">La aplicación debe llamar al **cierre** antes de la versión final.</span><span class="sxs-lookup"><span data-stu-id="a9394-111">**Shutdown** should be called by the application before final release.</span></span> <span data-ttu-id="a9394-112">En este momento se libera la referencia del módulo de descifrado de contenido (CDM) y cualquier otro recurso.</span><span class="sxs-lookup"><span data-stu-id="a9394-112">The Content Decryption Module (CDM) reference and any other resources is released at this point.</span></span> <span data-ttu-id="a9394-113">Sin embargo, las sesiones relacionadas no se liberan ni se cierran.</span><span class="sxs-lookup"><span data-stu-id="a9394-113">However, related sessions are not freed or closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9394-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9394-114">Requirements</span></span>



| <span data-ttu-id="a9394-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9394-115">Requirement</span></span> | <span data-ttu-id="a9394-116">Value</span><span class="sxs-lookup"><span data-stu-id="a9394-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9394-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9394-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a9394-118">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="a9394-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a9394-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9394-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a9394-120">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9394-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a9394-121">IDL</span><span class="sxs-lookup"><span data-stu-id="a9394-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9394-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9394-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9394-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9394-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9394-124">**IMFMediaKeys**</span><span class="sxs-lookup"><span data-stu-id="a9394-124">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




