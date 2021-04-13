---
title: MPVERSION_INFO estructura (MpClient. h)
description: Información de versión de los componentes del administrador de protección contra malware de.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPVERSION_INFO características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359807"
---
# <a name="mpversion_info-structure"></a><span data-ttu-id="25c49-105">Estructura de información de MPVERSION \_</span><span class="sxs-lookup"><span data-stu-id="25c49-105">MPVERSION\_INFO structure</span></span>

<span data-ttu-id="25c49-106">Información de versión de los componentes del administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="25c49-106">Version information for the malware protection manager's components.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c49-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25c49-107">Syntax</span></span>


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a><span data-ttu-id="25c49-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="25c49-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="25c49-109">**Producto**</span><span class="sxs-lookup"><span data-stu-id="25c49-109">**Product**</span></span>
</dt> <dd>

<span data-ttu-id="25c49-110">Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="25c49-110">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25c49-111">Versión del producto.</span><span class="sxs-lookup"><span data-stu-id="25c49-111">Product version.</span></span>

</dd> <dt>

<span data-ttu-id="25c49-112">**Servicio**</span><span class="sxs-lookup"><span data-stu-id="25c49-112">**Service**</span></span>
</dt> <dd>

<span data-ttu-id="25c49-113">Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="25c49-113">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25c49-114">Versión del componente de servicio.</span><span class="sxs-lookup"><span data-stu-id="25c49-114">Service component version.</span></span>

</dd> <dt>

<span data-ttu-id="25c49-115">**FileSystemFilter**</span><span class="sxs-lookup"><span data-stu-id="25c49-115">**FileSystemFilter**</span></span>
</dt> <dd>

<span data-ttu-id="25c49-116">Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="25c49-116">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25c49-117">Versión del componente de filtro del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="25c49-117">File system filter component version.</span></span>

</dd> <dt>

<span data-ttu-id="25c49-118">**Engine**</span><span class="sxs-lookup"><span data-stu-id="25c49-118">**Engine**</span></span>
</dt> <dd>

<span data-ttu-id="25c49-119">Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="25c49-119">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25c49-120">Versión del componente del motor.</span><span class="sxs-lookup"><span data-stu-id="25c49-120">Engine component version.</span></span>

</dd> <dt>

<span data-ttu-id="25c49-121">**Assignature**</span><span class="sxs-lookup"><span data-stu-id="25c49-121">**ASSignature**</span></span>
</dt> <dd>

<span data-ttu-id="25c49-122">Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="25c49-122">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25c49-123">Versión del componente de firma de AntiSpyware.</span><span class="sxs-lookup"><span data-stu-id="25c49-123">Antispyware signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="25c49-124">**AVSignature**</span><span class="sxs-lookup"><span data-stu-id="25c49-124">**AVSignature**</span></span>
</dt> <dd>

<span data-ttu-id="25c49-125">Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="25c49-125">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25c49-126">Versión del componente de firma antivirus.</span><span class="sxs-lookup"><span data-stu-id="25c49-126">Antivirus signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="25c49-127">**NISEngine**</span><span class="sxs-lookup"><span data-stu-id="25c49-127">**NISEngine**</span></span>
</dt> <dd>

<span data-ttu-id="25c49-128">Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="25c49-128">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25c49-129">Versión del motor NIS.</span><span class="sxs-lookup"><span data-stu-id="25c49-129">NIS engine version.</span></span>

</dd> <dt>

<span data-ttu-id="25c49-130">**NISSignature**</span><span class="sxs-lookup"><span data-stu-id="25c49-130">**NISSignature**</span></span>
</dt> <dd>

<span data-ttu-id="25c49-131">Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="25c49-131">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25c49-132">Versión del componente de firma de firma NIS.</span><span class="sxs-lookup"><span data-stu-id="25c49-132">NIS Signature signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="25c49-133">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="25c49-133">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="25c49-134">Tipo: **[**MPCOMPONENT \_ versión**](mpcomponent-version.md) \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="25c49-134">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="25c49-135">Campos reservados.</span><span class="sxs-lookup"><span data-stu-id="25c49-135">Reserved fields.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25c49-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25c49-136">Requirements</span></span>



| <span data-ttu-id="25c49-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="25c49-137">Requirement</span></span> | <span data-ttu-id="25c49-138">Value</span><span class="sxs-lookup"><span data-stu-id="25c49-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25c49-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25c49-139">Minimum supported client</span></span><br/> | <span data-ttu-id="25c49-140">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="25c49-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="25c49-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25c49-141">Minimum supported server</span></span><br/> | <span data-ttu-id="25c49-142">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="25c49-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25c49-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25c49-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="25c49-144"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="25c49-144"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25c49-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="25c49-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c49-146">**versión de MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="25c49-146">**MPCOMPONENT\_VERSION**</span></span>](mpcomponent-version.md)
</dt> </dl>

 

 





