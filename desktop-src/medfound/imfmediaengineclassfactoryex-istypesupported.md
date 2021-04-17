---
description: Obtiene un valor que indica si el sistema de claves especificado admite el tipo de medio especificado.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'IMFMediaEngineClassFactoryEx:: IsTypeSupported (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697912"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a><span data-ttu-id="962e8-103">IMFMediaEngineClassFactoryEx:: IsTypeSupported (método)</span><span class="sxs-lookup"><span data-stu-id="962e8-103">IMFMediaEngineClassFactoryEx::IsTypeSupported method</span></span>

<span data-ttu-id="962e8-104">Obtiene un valor que indica si el sistema de claves especificado admite el tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="962e8-104">Gets a value that indicates if the specified key system supports the specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="962e8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="962e8-105">Syntax</span></span>


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a><span data-ttu-id="962e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="962e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="962e8-107">*type*</span><span class="sxs-lookup"><span data-stu-id="962e8-107">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="962e8-108">Tipo MIME para el que se va a comprobar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="962e8-108">The MIME type to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="962e8-109">*keySystem*</span><span class="sxs-lookup"><span data-stu-id="962e8-109">*keySystem*</span></span> 
</dt> <dd>

<span data-ttu-id="962e8-110">Sistema de claves para el que se va a comprobar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="962e8-110">The key system to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="962e8-111">*isSupported*</span><span class="sxs-lookup"><span data-stu-id="962e8-111">*isSupported*</span></span> 
</dt> <dd>

<span data-ttu-id="962e8-112">**true** si el tipo es compatible con *keySystem*; en caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="962e8-112">**true** if type is supported by *keySystem*; otherwise, **false.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="962e8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="962e8-113">Return value</span></span>

<span data-ttu-id="962e8-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="962e8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="962e8-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="962e8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="962e8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="962e8-116">Requirements</span></span>



| <span data-ttu-id="962e8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="962e8-117">Requirement</span></span> | <span data-ttu-id="962e8-118">Value</span><span class="sxs-lookup"><span data-stu-id="962e8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="962e8-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="962e8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="962e8-120">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="962e8-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="962e8-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="962e8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="962e8-122">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="962e8-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="962e8-123">IDL</span><span class="sxs-lookup"><span data-stu-id="962e8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="962e8-124"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="962e8-124"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="962e8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="962e8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="962e8-126">**IMFMediaEngineClassFactoryEx**</span><span class="sxs-lookup"><span data-stu-id="962e8-126">**IMFMediaEngineClassFactoryEx**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




