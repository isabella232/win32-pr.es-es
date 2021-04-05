---
title: MPRESOURCE_INFO estructura (MpClient. h)
description: Estructura de información de recursos.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPRESOURCE_INFO características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996660"
---
# <a name="mpresource_info-structure"></a><span data-ttu-id="69aa8-105">Estructura de información de MPRESOURCE \_</span><span class="sxs-lookup"><span data-stu-id="69aa8-105">MPRESOURCE\_INFO structure</span></span>

<span data-ttu-id="69aa8-106">Estructura de información de recursos.</span><span class="sxs-lookup"><span data-stu-id="69aa8-106">Resource information structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="69aa8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69aa8-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a><span data-ttu-id="69aa8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="69aa8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="69aa8-109">**Regímenes**</span><span class="sxs-lookup"><span data-stu-id="69aa8-109">**Scheme**</span></span>
</dt> <dd>

<span data-ttu-id="69aa8-110">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="69aa8-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="69aa8-111">Identificador del esquema de recursos como "File" o "dir".</span><span class="sxs-lookup"><span data-stu-id="69aa8-111">Resource scheme identifier such as "file" or "dir".</span></span>

</dd> <dt>

<span data-ttu-id="69aa8-112">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="69aa8-112">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="69aa8-113">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="69aa8-113">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="69aa8-114">Ruta de acceso absoluta del recurso, basándose en el **esquema**.</span><span class="sxs-lookup"><span data-stu-id="69aa8-114">Absolute path of resource, based on **Scheme**.</span></span>

</dd> <dt>

<span data-ttu-id="69aa8-115">**Clase**</span><span class="sxs-lookup"><span data-stu-id="69aa8-115">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="69aa8-116">Type: **\_ clase MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="69aa8-116">Type: **MPRESOURCE\_CLASS**</span></span>

</dd> <dd>

<span data-ttu-id="69aa8-117">Este campo se establece cuando el recurso se identifica como parte de la amenaza.</span><span class="sxs-lookup"><span data-stu-id="69aa8-117">This field is set when the resource is identified as part of the threat.</span></span> <span data-ttu-id="69aa8-118">Especifica la clase de recurso, principalmente concreta frente a latente.</span><span class="sxs-lookup"><span data-stu-id="69aa8-118">It specifies the resource class, mainly concrete vs. latent.</span></span> <span data-ttu-id="69aa8-119">Puede ser una combinación de estos valores posibles:</span><span class="sxs-lookup"><span data-stu-id="69aa8-119">It can be a combination of these possible values:</span></span>



| <span data-ttu-id="69aa8-120">Value</span><span class="sxs-lookup"><span data-stu-id="69aa8-120">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="69aa8-121">Significado</span><span class="sxs-lookup"><span data-stu-id="69aa8-121">Meaning</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <span data-ttu-id="69aa8-122"><dt>**Módulo de administración \_ Clase de recursos \_ \_ desconocida**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="69aa8-122"><dt>**MP\_RESOURCE\_CLASS\_UNKNOWN**</dt> <dt>0x0000</dt></span></span> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <span data-ttu-id="69aa8-123"><dt>**Módulo de administración \_ Clase de recurso 0x0001 \_ \_ concreta**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="69aa8-123"><dt>**MP\_RESOURCE\_CLASS\_CONCRETE**</dt> <dt>0x0001</dt></span></span> </dl>           | <span data-ttu-id="69aa8-124">Es mutuamente excluyente con la **clase de recursos del módulo de administración \_ \_ \_ latente**.</span><span class="sxs-lookup"><span data-stu-id="69aa8-124">Mutually exclusive with **MP\_RESOURCE\_CLASS\_LATENT**.</span></span><br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <span data-ttu-id="69aa8-125"><dt>**Módulo de administración \_ Clase de recurso \_ \_ lated**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="69aa8-125"><dt>**MP\_RESOURCE\_CLASS\_LATENT**</dt> <dt>0x0002</dt></span></span> </dl>                 | <span data-ttu-id="69aa8-126">Es mutuamente excluyente con la **clase de recursos del módulo de administración \_ \_ \_ concreta**.</span><span class="sxs-lookup"><span data-stu-id="69aa8-126">Mutually exclusive with **MP\_RESOURCE\_CLASS\_CONCRETE**.</span></span><br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <span data-ttu-id="69aa8-127"><dt>**Módulo de administración \_ \_Archivo de \_ ejemplo \_ de clase de recursos**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="69aa8-127"><dt>**MP\_RESOURCE\_CLASS\_SAMPLE\_FILE**</dt> <dt>0x0004</dt></span></span> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <span data-ttu-id="69aa8-128"><dt>**Módulo de administración \_ 0x0100 \_ \_ compartido de clase de recurso**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="69aa8-128"><dt>**MP\_RESOURCE\_CLASS\_SHARED**</dt> <dt>0x0100</dt></span></span> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69aa8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69aa8-129">Requirements</span></span>



| <span data-ttu-id="69aa8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="69aa8-130">Requirement</span></span> | <span data-ttu-id="69aa8-131">Value</span><span class="sxs-lookup"><span data-stu-id="69aa8-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69aa8-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69aa8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="69aa8-133">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="69aa8-133">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="69aa8-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69aa8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="69aa8-135">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="69aa8-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69aa8-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69aa8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="69aa8-137"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="69aa8-137"><dt>MpClient.h</dt></span></span> </dl> |



 

 





