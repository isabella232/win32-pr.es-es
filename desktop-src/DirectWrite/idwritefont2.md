---
title: Interfaz IDWriteFont2
description: Representa una fuente física en una colección de fuentes.
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- Interfaz IDWriteFont2 de escritura directa
- IDWriteFont2 interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a47e56915747b0e118a6f63484b9dd3dcdbd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359766"
---
# <a name="idwritefont2-interface"></a><span data-ttu-id="38779-105">Interfaz IDWriteFont2</span><span class="sxs-lookup"><span data-stu-id="38779-105">IDWriteFont2 interface</span></span>

<span data-ttu-id="38779-106">Representa una fuente física en una colección de fuentes.</span><span class="sxs-lookup"><span data-stu-id="38779-106">Represents a physical font in a font collection.</span></span>

<span data-ttu-id="38779-107">Esta interfaz agrega la capacidad de comprobar si es posible que una ruta de representación de color sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="38779-107">This interface adds the ability to check if a color rendering path is potentially necessary.</span></span>

## <a name="members"></a><span data-ttu-id="38779-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="38779-108">Members</span></span>

<span data-ttu-id="38779-109">La interfaz **IDWriteFont2** hereda de [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span><span class="sxs-lookup"><span data-stu-id="38779-109">The **IDWriteFont2** interface inherits from [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span></span> <span data-ttu-id="38779-110">**IDWriteFont2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="38779-110">**IDWriteFont2** also has these types of members:</span></span>

-   [<span data-ttu-id="38779-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="38779-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="38779-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="38779-112">Methods</span></span>

<span data-ttu-id="38779-113">La interfaz **IDWriteFont2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="38779-113">The **IDWriteFont2** interface has these methods.</span></span>



| <span data-ttu-id="38779-114">Método</span><span class="sxs-lookup"><span data-stu-id="38779-114">Method</span></span>                                          | <span data-ttu-id="38779-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="38779-115">Description</span></span>                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="38779-116">**IsColorFont**</span><span class="sxs-lookup"><span data-stu-id="38779-116">**IsColorFont**</span></span>](idwritefont2-iscolorfont.md) | <span data-ttu-id="38779-117">Permite determinar si es posible que una ruta de representación de color sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="38779-117">Enables determining if a color rendering path is potentially necessary.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="38779-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38779-118">Requirements</span></span>



| <span data-ttu-id="38779-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="38779-119">Requirement</span></span> | <span data-ttu-id="38779-120">Value</span><span class="sxs-lookup"><span data-stu-id="38779-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38779-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38779-121">Minimum supported client</span></span><br/> | <span data-ttu-id="38779-122">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="38779-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="38779-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38779-123">Minimum supported server</span></span><br/> | <span data-ttu-id="38779-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="38779-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="38779-125">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38779-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="38779-126">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="38779-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="38779-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38779-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="38779-128"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38779-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="38779-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="38779-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38779-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38779-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38779-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="38779-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38779-132">**IDWriteFont1**</span><span class="sxs-lookup"><span data-stu-id="38779-132">**IDWriteFont1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

