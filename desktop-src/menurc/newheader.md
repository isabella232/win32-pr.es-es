---
title: Estructura NEWHEADER
description: Contiene el número de componentes de icono o de cursor de un grupo de recursos. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menús de la estructura NEWHEADER y otros recursos
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996068"
---
# <a name="newheader-structure"></a><span data-ttu-id="9a229-105">Estructura NEWHEADER</span><span class="sxs-lookup"><span data-stu-id="9a229-105">NEWHEADER structure</span></span>

<span data-ttu-id="9a229-106">Contiene el número de componentes de icono o de cursor de un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9a229-106">Contains the number of icon or cursor components in a resource group.</span></span> <span data-ttu-id="9a229-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="9a229-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a229-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a229-108">Syntax</span></span>


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a><span data-ttu-id="9a229-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9a229-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="9a229-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="9a229-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="9a229-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="9a229-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9a229-112">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9a229-112">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9a229-113">**ResType**</span><span class="sxs-lookup"><span data-stu-id="9a229-113">**ResType**</span></span>
</dt> <dd>

<span data-ttu-id="9a229-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="9a229-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9a229-115">El tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="9a229-115">The resource type.</span></span> <span data-ttu-id="9a229-116">Este miembro debe tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9a229-116">This member must have one of the following values.</span></span>



| <span data-ttu-id="9a229-117">Value</span><span class="sxs-lookup"><span data-stu-id="9a229-117">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="9a229-118">Significado</span><span class="sxs-lookup"><span data-stu-id="9a229-118">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <span data-ttu-id="9a229-119"><dt>**Res \_ CURSOR**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9a229-119"><dt>**RES\_CURSOR**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="9a229-120">Tipo de recurso de cursor.</span><span class="sxs-lookup"><span data-stu-id="9a229-120">Cursor resource type.</span></span><br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <span data-ttu-id="9a229-121"><dt>**Res \_ ICONO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9a229-121"><dt>**RES\_ICON**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="9a229-122">Tipo de recurso de icono.</span><span class="sxs-lookup"><span data-stu-id="9a229-122">Icon resource type.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="9a229-123">**ResCount**</span><span class="sxs-lookup"><span data-stu-id="9a229-123">**ResCount**</span></span>
</dt> <dd>

<span data-ttu-id="9a229-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="9a229-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9a229-125">El número de componentes de icono o de cursor en el grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9a229-125">The number of icon or cursor components in the resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a229-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a229-126">Remarks</span></span>

<span data-ttu-id="9a229-127">Una o varias estructuras [**RESDIR**](resdir.md) siguen inmediatamente a la estructura **NEWHEADER** del archivo. res.</span><span class="sxs-lookup"><span data-stu-id="9a229-127">One or more [**RESDIR**](resdir.md) structures immediately follow the **NEWHEADER** structure in the .res file.</span></span> <span data-ttu-id="9a229-128">El miembro **ResCount** especifica el número de estructuras **RESDIR** .</span><span class="sxs-lookup"><span data-stu-id="9a229-128">The **ResCount** member specifies the number of **RESDIR** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a229-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a229-129">Requirements</span></span>



| <span data-ttu-id="9a229-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a229-130">Requirement</span></span> | <span data-ttu-id="9a229-131">Value</span><span class="sxs-lookup"><span data-stu-id="9a229-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9a229-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a229-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9a229-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9a229-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9a229-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a229-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9a229-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9a229-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9a229-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a229-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a229-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9a229-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9a229-138">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="9a229-138">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="9a229-139">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9a229-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9a229-140">Recursos</span><span class="sxs-lookup"><span data-stu-id="9a229-140">Resources</span></span>](resources.md)
</dt> </dl>

 

 





