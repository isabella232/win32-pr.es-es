---
title: IDWriteFont2 IsColorFont, método
description: Permite determinar si es posible que una ruta de representación de color sea necesaria.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Método IsColorFont de escritura directa
- Método IsColorFont de escritura directa, interfaz IDWriteFont2
- Interfaz IDWriteFont2 Direct Write, método IsColorFont
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422445"
---
# <a name="idwritefont2iscolorfont-method"></a><span data-ttu-id="460f8-106">IDWriteFont2:: IsColorFont (método)</span><span class="sxs-lookup"><span data-stu-id="460f8-106">IDWriteFont2::IsColorFont method</span></span>

<span data-ttu-id="460f8-107">Permite determinar si es posible que una ruta de representación de color sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="460f8-107">Enables determining if a color rendering path is potentially necessary.</span></span>

## <a name="syntax"></a><span data-ttu-id="460f8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="460f8-108">Syntax</span></span>


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a><span data-ttu-id="460f8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="460f8-109">Parameters</span></span>

<span data-ttu-id="460f8-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="460f8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="460f8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="460f8-111">Return value</span></span>

<span data-ttu-id="460f8-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="460f8-112">Type: **BOOL**</span></span>

<span data-ttu-id="460f8-113">Devuelve **true** si la fuente tiene información de color (tablas COLR y CPAL); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="460f8-113">Returns **TRUE** if the font has color information (COLR and CPAL tables); otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="460f8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="460f8-114">Requirements</span></span>



| <span data-ttu-id="460f8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="460f8-115">Requirement</span></span> | <span data-ttu-id="460f8-116">Value</span><span class="sxs-lookup"><span data-stu-id="460f8-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="460f8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="460f8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="460f8-118">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="460f8-118">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="460f8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="460f8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="460f8-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="460f8-120">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="460f8-121">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="460f8-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="460f8-122">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="460f8-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="460f8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="460f8-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="460f8-124"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="460f8-124"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="460f8-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="460f8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="460f8-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="460f8-126"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="460f8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="460f8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="460f8-128">**IDWriteFont2**</span><span class="sxs-lookup"><span data-stu-id="460f8-128">**IDWriteFont2**</span></span>](idwritefont2.md)
</dt> </dl>

 

 





