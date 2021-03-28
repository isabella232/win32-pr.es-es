---
description: Contiene información que utiliza el administrador de archivos para agregar un menú personalizado proporcionado por un archivo DLL de extensión del administrador de archivos. La estructura también proporciona un valor Delta que el archivo DLL de extensión puede utilizar para manipular el menú personalizado una vez que el administrador de archivos ha cargado el menú.
title: FMS_LOAD estructura (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: 1745c4e34ac124e9990602350db6479ce287be8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984203"
---
# <a name="fms_load-structure"></a><span data-ttu-id="e9937-104">Estructura de carga de FMS \_</span><span class="sxs-lookup"><span data-stu-id="e9937-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="e9937-105">Contiene información que utiliza el administrador de archivos para agregar un menú personalizado proporcionado por un archivo DLL de extensión del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="e9937-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="e9937-106">La estructura también proporciona un valor Delta que el archivo DLL de extensión puede utilizar para manipular el menú personalizado una vez que el administrador de archivos ha cargado el menú.</span><span class="sxs-lookup"><span data-stu-id="e9937-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9937-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9937-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="e9937-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9937-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9937-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="e9937-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="e9937-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9937-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9937-111">Longitud, en bytes, de la estructura.</span><span class="sxs-lookup"><span data-stu-id="e9937-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="e9937-112">**szMenuName**</span><span class="sxs-lookup"><span data-stu-id="e9937-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="e9937-113">Tipo: **\[ texto del menú TCHAR \_ \_ longitud \]**</span><span class="sxs-lookup"><span data-stu-id="e9937-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="e9937-114">Un nombre terminado en null para un elemento de menú que aparece en la barra de menús del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="e9937-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="e9937-115">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="e9937-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="e9937-116">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="e9937-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="e9937-117">Identificador del menú emergente que se ha agregado a la barra de menús del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="e9937-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="e9937-118">**wMenuDelta**</span><span class="sxs-lookup"><span data-stu-id="e9937-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="e9937-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e9937-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="e9937-120">Valor Delta del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="e9937-120">The menu item delta value.</span></span> <span data-ttu-id="e9937-121">Para evitar conflictos con sus propios elementos de menú, el administrador de archivos renumera los identificadores de elemento de menú en el menú emergente identificado por el miembro **hMenu** agregando este valor Delta a cada identificador.</span><span class="sxs-lookup"><span data-stu-id="e9937-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="e9937-122">Un archivo DLL de extensión que debe modificar un elemento de menú debe identificar el elemento agregando el valor delta al identificador del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="e9937-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="e9937-123">El valor de este miembro puede variar de una sesión a una sesión.</span><span class="sxs-lookup"><span data-stu-id="e9937-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9937-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9937-124">Requirements</span></span>



| <span data-ttu-id="e9937-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9937-125">Requirement</span></span> | <span data-ttu-id="e9937-126">Value</span><span class="sxs-lookup"><span data-stu-id="e9937-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9937-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9937-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e9937-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e9937-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e9937-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9937-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e9937-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9937-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e9937-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9937-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9937-132"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9937-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9937-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9937-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9937-134">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="e9937-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




