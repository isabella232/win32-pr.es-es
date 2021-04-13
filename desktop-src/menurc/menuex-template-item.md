---
title: Estructura de MENUEX_TEMPLATE_ITEM
description: Define un elemento de menú en una plantilla de menú extendida. Esta definición de estructura solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM menús de estructura y otros recursos
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535085"
---
# <a name="menuex_template_item-structure"></a><span data-ttu-id="7b057-105">Estructura del elemento de \_ plantilla MENUEX \_</span><span class="sxs-lookup"><span data-stu-id="7b057-105">MENUEX\_TEMPLATE\_ITEM structure</span></span>

<span data-ttu-id="7b057-106">Define un elemento de menú en una plantilla de menú extendida.</span><span class="sxs-lookup"><span data-stu-id="7b057-106">Defines a menu item in an extended menu template.</span></span> <span data-ttu-id="7b057-107">Esta definición de estructura solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="7b057-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b057-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b057-108">Syntax</span></span>

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a><span data-ttu-id="7b057-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7b057-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b057-110">**dwType**</span><span class="sxs-lookup"><span data-stu-id="7b057-110">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="7b057-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7b057-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7b057-112">El tipo de elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7b057-112">The menu item type.</span></span> <span data-ttu-id="7b057-113">Este miembro puede ser una combinación de los valores de tipo (a partir de MFT) enumerados con la estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="7b057-113">This member can be a combination of the type (beginning with MFT) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b057-114">**dwState**</span><span class="sxs-lookup"><span data-stu-id="7b057-114">**dwState**</span></span>
</dt> <dd>

<span data-ttu-id="7b057-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7b057-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7b057-116">Estado del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7b057-116">The menu item state.</span></span> <span data-ttu-id="7b057-117">Este miembro puede ser una combinación de los valores de estado (empezando por MFS) enumerados con la estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="7b057-117">This member can be a combination of the state (beginning with MFS) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b057-118">**uId**</span><span class="sxs-lookup"><span data-stu-id="7b057-118">**uId**</span></span>
</dt> <dd>

<span data-ttu-id="7b057-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7b057-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="7b057-120">Identificador del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7b057-120">The menu item identifier.</span></span> <span data-ttu-id="7b057-121">Este es un valor definido por la aplicación que identifica el elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7b057-121">This is an application-defined value that identifies the menu item.</span></span> <span data-ttu-id="7b057-122">En un recurso de menú extendido, los elementos que abren los menús desplegables o los submenús, así como los elementos de comando, pueden tener identificadores.</span><span class="sxs-lookup"><span data-stu-id="7b057-122">In an extended menu resource, items that open drop-down menus or submenus as well as command items can have identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="7b057-123">**wFlags**</span><span class="sxs-lookup"><span data-stu-id="7b057-123">**wFlags**</span></span>
</dt> <dd>

<span data-ttu-id="7b057-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="7b057-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="7b057-125">Especifica si el elemento de menú es el último elemento en la barra de menús, en el menú desplegable, en el submenú o en el menú contextual, y si es un elemento que abre un menú desplegable o un submenú.</span><span class="sxs-lookup"><span data-stu-id="7b057-125">Specifies whether the menu item is the last item in the menu bar, drop-down menu, submenu, or shortcut menu and whether it is an item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="7b057-126">Este miembro puede tener cero o más de estos valores.</span><span class="sxs-lookup"><span data-stu-id="7b057-126">This member can be zero or more of these values.</span></span> <span data-ttu-id="7b057-127">En el caso de las aplicaciones de 32 bits, este miembro es una palabra; en el caso de las aplicaciones de 16 bits, es un byte.</span><span class="sxs-lookup"><span data-stu-id="7b057-127">For 32-bit applications, this member is a word; for 16-bit applications, it is a byte.</span></span>

<dt>

<span data-ttu-id="7b057-128">0x80</span><span class="sxs-lookup"><span data-stu-id="7b057-128">0x80</span></span>
</dt> <dd>

<span data-ttu-id="7b057-129">La estructura define el último elemento de menú en la barra de menús, en el menú desplegable, en el submenú o en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="7b057-129">The structure defines the last menu item in the menu bar, drop-down menu, submenu, or shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="7b057-130">0x01</span><span class="sxs-lookup"><span data-stu-id="7b057-130">0x01</span></span>
</dt> <dd>

<span data-ttu-id="7b057-131">La estructura define un elemento que abre un menú desplegable o un submenú.</span><span class="sxs-lookup"><span data-stu-id="7b057-131">The structure defines a item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="7b057-132">Las estructuras posteriores definen los elementos de menú en el menú desplegable o submenú correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7b057-132">Subsequent structures define menu items in the corresponding drop-down menu or submenu.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7b057-133">**szText**</span><span class="sxs-lookup"><span data-stu-id="7b057-133">**szText**</span></span>
</dt> <dd>

<span data-ttu-id="7b057-134">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="7b057-134">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="7b057-135">Texto del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7b057-135">The menu item text.</span></span> <span data-ttu-id="7b057-136">Este miembro es una cadena Unicode terminada en null, alineada en un límite de palabras.</span><span class="sxs-lookup"><span data-stu-id="7b057-136">This member is a null-terminated Unicode string, aligned on a word boundary.</span></span> <span data-ttu-id="7b057-137">El tamaño de la definición del elemento de menú varía en función de la longitud de esta cadena.</span><span class="sxs-lookup"><span data-stu-id="7b057-137">The size of the menu item definition varies depending on the length of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b057-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b057-138">Remarks</span></span>

<span data-ttu-id="7b057-139">Una plantilla de menú extendida está formada por una estructura de [**\_ \_ encabezado de plantilla de MENUEX**](menuex-template-header.md) , seguida de una o varias estructuras de **\_ \_ elemento de plantilla MENUEX** contiguas.</span><span class="sxs-lookup"><span data-stu-id="7b057-139">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one or more contiguous **MENUEX\_TEMPLATE\_ITEM** structures.</span></span> <span data-ttu-id="7b057-140">Las estructuras de **\_ \_ elementos de plantilla MENUEX** , que son de longitud variable, se alinean en los límites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7b057-140">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="7b057-141">Para crear un menú a partir de una plantilla de menú extendida en memoria, use la función [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="7b057-141">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b057-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b057-142">Requirements</span></span>



| <span data-ttu-id="7b057-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b057-143">Requirement</span></span> | <span data-ttu-id="7b057-144">Value</span><span class="sxs-lookup"><span data-stu-id="7b057-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7b057-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b057-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7b057-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7b057-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7b057-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b057-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7b057-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7b057-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7b057-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b057-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="7b057-150">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7b057-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7b057-151">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="7b057-151">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="7b057-152">**\_encabezado de plantilla MENUEX \_**</span><span class="sxs-lookup"><span data-stu-id="7b057-152">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="7b057-153">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="7b057-153">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

<span data-ttu-id="7b057-154">**Vista**</span><span class="sxs-lookup"><span data-stu-id="7b057-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7b057-155">Menús</span><span class="sxs-lookup"><span data-stu-id="7b057-155">Menus</span></span>](menus.md)
</dt> </dl>

 

 





