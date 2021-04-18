---
title: Estructura MENUHEADER
description: Contiene información de versión del recurso de menú. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Menús de la estructura MENUHEADER y otros recursos
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656475"
---
# <a name="menuheader-structure"></a><span data-ttu-id="d8ae6-105">Estructura MENUHEADER</span><span class="sxs-lookup"><span data-stu-id="d8ae6-105">MENUHEADER structure</span></span>

<span data-ttu-id="d8ae6-106">Contiene información de versión del recurso de menú.</span><span class="sxs-lookup"><span data-stu-id="d8ae6-106">Contains version information for the menu resource.</span></span> <span data-ttu-id="d8ae6-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="d8ae6-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ae6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8ae6-108">Syntax</span></span>


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a><span data-ttu-id="d8ae6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d8ae6-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8ae6-110">**wVersion**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d8ae6-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8ae6-112">Número de versión de la plantilla de menú.</span><span class="sxs-lookup"><span data-stu-id="d8ae6-112">The version number of the menu template.</span></span> <span data-ttu-id="d8ae6-113">Este miembro debe ser igual a cero para indicar que se trata de [**un \_ menú RT**](/windows/desktop/menurc/resource-types) creado con una plantilla de menú estándar.</span><span class="sxs-lookup"><span data-stu-id="d8ae6-113">This member must be equal to zero to indicate that this is an [**RT\_MENU**](/windows/desktop/menurc/resource-types) created with a standard menu template.</span></span>

</dd> <dt>

<span data-ttu-id="d8ae6-114">**cbHeaderSize**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-114">**cbHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="d8ae6-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8ae6-116">Tamaño del encabezado de la plantilla de menú.</span><span class="sxs-lookup"><span data-stu-id="d8ae6-116">The size of the menu template header.</span></span> <span data-ttu-id="d8ae6-117">Este valor es cero para los menús que se crean con una plantilla de menú estándar.</span><span class="sxs-lookup"><span data-stu-id="d8ae6-117">This value is zero for menus you create with a standard menu template.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8ae6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8ae6-118">Requirements</span></span>



| <span data-ttu-id="d8ae6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8ae6-119">Requirement</span></span> | <span data-ttu-id="d8ae6-120">Value</span><span class="sxs-lookup"><span data-stu-id="d8ae6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d8ae6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8ae6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ae6-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d8ae6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d8ae6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8ae6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ae6-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d8ae6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d8ae6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8ae6-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d8ae6-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d8ae6-127">**\_encabezado de plantilla MENUEX \_**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-127">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="d8ae6-128">**\_elemento de plantilla MENUEX \_**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-128">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

[<span data-ttu-id="d8ae6-129">**MENUITEMTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-129">**MENUITEMTEMPLATE**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[<span data-ttu-id="d8ae6-130">**MENUITEMTEMPLATEHEADER**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-130">**MENUITEMTEMPLATEHEADER**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[<span data-ttu-id="d8ae6-131">**NORMALMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-131">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

[<span data-ttu-id="d8ae6-132">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-132">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="d8ae6-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d8ae6-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d8ae6-134">Recursos</span><span class="sxs-lookup"><span data-stu-id="d8ae6-134">Resources</span></span>](resources.md)
</dt> </dl>

 

