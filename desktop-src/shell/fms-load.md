---
description: Contiene información que el Administrador de archivos usa para agregar un menú personalizado proporcionado por un archivo DLL de extensión del Administrador de archivos. La estructura también proporciona un valor delta que el archivo DLL de extensión puede usar para manipular el menú personalizado después de que el Administrador de archivos haya cargado el menú.
title: FMS_LOAD estructura (Wfext.h)
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
ms.openlocfilehash: efd1777704c775db84c7dabf54b9e06c81535fb4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842196"
---
# <a name="fms_load-structure"></a><span data-ttu-id="363ff-104">Estructura \_ DE FMS LOAD</span><span class="sxs-lookup"><span data-stu-id="363ff-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="363ff-105">Contiene información que el Administrador de archivos usa para agregar un menú personalizado proporcionado por un archivo DLL de extensión del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="363ff-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="363ff-106">La estructura también proporciona un valor delta que el archivo DLL de extensión puede usar para manipular el menú personalizado después de que el Administrador de archivos haya cargado el menú.</span><span class="sxs-lookup"><span data-stu-id="363ff-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="363ff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="363ff-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="363ff-108">Members</span><span class="sxs-lookup"><span data-stu-id="363ff-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="363ff-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="363ff-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="363ff-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="363ff-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="363ff-111">Longitud, en bytes, de la estructura .</span><span class="sxs-lookup"><span data-stu-id="363ff-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="363ff-112">**szMenuName**</span><span class="sxs-lookup"><span data-stu-id="363ff-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="363ff-113">Tipo: **\[ \_ LEN \_ \] DE TEXTO DEL MENÚ TCHAR**</span><span class="sxs-lookup"><span data-stu-id="363ff-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="363ff-114">Nombre terminado en NULL para un elemento de menú que aparece en la barra de menús del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="363ff-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="363ff-115">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="363ff-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="363ff-116">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="363ff-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="363ff-117">Identificador del menú emergente agregado a la barra de menús del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="363ff-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="363ff-118">**wMenuDelta**</span><span class="sxs-lookup"><span data-stu-id="363ff-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="363ff-119">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="363ff-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="363ff-120">Valor delta del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="363ff-120">The menu item delta value.</span></span> <span data-ttu-id="363ff-121">Para evitar conflictos con sus propios elementos de menú, el Administrador de archivos vuelve a numerar los identificadores de elementos de menú en el menú emergente identificado por el **miembro hMenu** agregando este valor delta a cada identificador.</span><span class="sxs-lookup"><span data-stu-id="363ff-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="363ff-122">Un archivo DLL de extensión que debe modificar un elemento de menú debe identificar el elemento agregando el valor delta al identificador del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="363ff-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="363ff-123">El valor de este miembro puede variar de una sesión a otra.</span><span class="sxs-lookup"><span data-stu-id="363ff-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="363ff-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="363ff-124">Requirements</span></span>



| <span data-ttu-id="363ff-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="363ff-125">Requirement</span></span> | <span data-ttu-id="363ff-126">Value</span><span class="sxs-lookup"><span data-stu-id="363ff-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="363ff-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="363ff-127">Minimum supported client</span></span><br/> | <span data-ttu-id="363ff-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="363ff-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="363ff-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="363ff-129">Minimum supported server</span></span><br/> | <span data-ttu-id="363ff-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="363ff-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="363ff-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="363ff-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="363ff-132"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="363ff-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="363ff-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="363ff-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363ff-134">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="363ff-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




