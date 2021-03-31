---
title: Método Initialize ISoftKbd (Softkbdc. h)
description: El método ISoftKbd Initialize inicializa todos los campos necesarios para un teclado en pantalla y genera distribuciones estándar de teclado en pantalla.
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Método Initialize servicios de texto Framework
- Método Initialize Text Services Framework, ISoftKbd (interfaz)
- ISoftKbd interface Text Services Framework, Initialize (método)
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801304"
---
# <a name="isoftkbdinitialize-method"></a><span data-ttu-id="f450d-106">ISoftKbd:: Initialize (método)</span><span class="sxs-lookup"><span data-stu-id="f450d-106">ISoftKbd::Initialize method</span></span>

<span data-ttu-id="f450d-107">El método **ISoftKbd:: Initialize** inicializa todos los campos necesarios para un teclado en pantalla y genera distribuciones estándar de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="f450d-107">The **ISoftKbd::Initialize** method initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="f450d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f450d-108">Syntax</span></span>


```C++
HRESULT Initialize();
```



## <a name="parameters"></a><span data-ttu-id="f450d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f450d-109">Parameters</span></span>

<span data-ttu-id="f450d-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f450d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f450d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f450d-111">Return value</span></span>

<span data-ttu-id="f450d-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f450d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f450d-113">Value</span><span class="sxs-lookup"><span data-stu-id="f450d-113">Value</span></span>                                                                                | <span data-ttu-id="f450d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f450d-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f450d-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f450d-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f450d-116">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f450d-116">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f450d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f450d-117">Requirements</span></span>



| <span data-ttu-id="f450d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f450d-118">Requirement</span></span> | <span data-ttu-id="f450d-119">Value</span><span class="sxs-lookup"><span data-stu-id="f450d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f450d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f450d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f450d-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f450d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f450d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f450d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f450d-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f450d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f450d-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f450d-124">Redistributable</span></span><br/>          | <span data-ttu-id="f450d-125">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f450d-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f450d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f450d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f450d-127"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f450d-127"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f450d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="f450d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f450d-129"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f450d-129"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="f450d-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f450d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f450d-131"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f450d-131"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f450d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f450d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f450d-133">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="f450d-133">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





