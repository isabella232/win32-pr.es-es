---
title: Estructura de MENUEX_TEMPLATE_HEADER
description: Define el encabezado de una plantilla de menú extendida. Esta definición de estructura solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER menús de estructura y otros recursos
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714557"
---
# <a name="menuex_template_header-structure"></a><span data-ttu-id="33e27-105">Estructura del encabezado de \_ plantilla MENUEX \_</span><span class="sxs-lookup"><span data-stu-id="33e27-105">MENUEX\_TEMPLATE\_HEADER structure</span></span>

<span data-ttu-id="33e27-106">Define el encabezado de una plantilla de menú extendida.</span><span class="sxs-lookup"><span data-stu-id="33e27-106">Defines the header for an extended menu template.</span></span> <span data-ttu-id="33e27-107">Esta definición de estructura solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="33e27-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e27-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33e27-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a><span data-ttu-id="33e27-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="33e27-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="33e27-110">**wVersion**</span><span class="sxs-lookup"><span data-stu-id="33e27-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="33e27-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="33e27-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="33e27-112">El número de versión de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="33e27-112">The template version number.</span></span> <span data-ttu-id="33e27-113">Este miembro debe ser 1 para las plantillas de menú extendidas.</span><span class="sxs-lookup"><span data-stu-id="33e27-113">This member must be 1 for extended menu templates.</span></span>

</dd> <dt>

<span data-ttu-id="33e27-114">**wOffset**</span><span class="sxs-lookup"><span data-stu-id="33e27-114">**wOffset**</span></span>
</dt> <dd>

<span data-ttu-id="33e27-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="33e27-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="33e27-116">Desplazamiento a la primera estructura [**de \_ \_ elementos de plantilla MENUEX**](menuex-template-item.md) , con respecto al final de este miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="33e27-116">The offset to the first [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structure, relative to the end of this structure member.</span></span> <span data-ttu-id="33e27-117">Si la primera definición de elemento sigue inmediatamente al miembro **dwHelpId** , este miembro debe ser 4.</span><span class="sxs-lookup"><span data-stu-id="33e27-117">If the first item definition immediately follows the **dwHelpId** member, this member should be 4.</span></span>

</dd> <dt>

<span data-ttu-id="33e27-118">**dwHelpId**</span><span class="sxs-lookup"><span data-stu-id="33e27-118">**dwHelpId**</span></span>
</dt> <dd>

<span data-ttu-id="33e27-119">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="33e27-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="33e27-120">El identificador de la ayuda de la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="33e27-120">The help identifier of menu bar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33e27-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33e27-121">Remarks</span></span>

<span data-ttu-id="33e27-122">Una plantilla de menú extendida está formada por una estructura de **\_ \_ encabezado de plantilla de MENUEX** , seguida de una o varias estructuras de [**\_ \_ elemento de plantilla MENUEX**](menuex-template-item.md) contiguas.</span><span class="sxs-lookup"><span data-stu-id="33e27-122">An extended menu template consists of a **MENUEX\_TEMPLATE\_HEADER** structure followed by one or more contiguous [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structures.</span></span> <span data-ttu-id="33e27-123">Las estructuras de **\_ \_ elementos de plantilla MENUEX** , que son de longitud variable, se alinean en los límites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="33e27-123">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="33e27-124">Para crear un menú a partir de una plantilla de menú extendida en memoria, use la función [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="33e27-124">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="33e27-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33e27-125">Requirements</span></span>



| <span data-ttu-id="33e27-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="33e27-126">Requirement</span></span> | <span data-ttu-id="33e27-127">Value</span><span class="sxs-lookup"><span data-stu-id="33e27-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="33e27-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33e27-128">Minimum supported client</span></span><br/> | <span data-ttu-id="33e27-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="33e27-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="33e27-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33e27-130">Minimum supported server</span></span><br/> | <span data-ttu-id="33e27-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="33e27-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="33e27-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="33e27-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="33e27-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="33e27-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="33e27-134">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="33e27-134">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="33e27-135">**\_elemento de plantilla MENUEX \_**</span><span class="sxs-lookup"><span data-stu-id="33e27-135">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

<span data-ttu-id="33e27-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="33e27-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="33e27-137">Menús</span><span class="sxs-lookup"><span data-stu-id="33e27-137">Menus</span></span>](menus.md)
</dt> </dl>

 

 





