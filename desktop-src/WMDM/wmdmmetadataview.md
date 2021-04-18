---
title: Estructura WMDMMetadataView
description: La estructura WMDMMetadataView define la vista de metadatos. El contenido se organiza en función de esta definición.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Estructura WMDMMetadataView Administrador de dispositivos Windows Media
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698557"
---
# <a name="wmdmmetadataview-structure"></a><span data-ttu-id="9479d-105">Estructura WMDMMetadataView</span><span class="sxs-lookup"><span data-stu-id="9479d-105">WMDMMetadataView structure</span></span>

<span data-ttu-id="9479d-106">La estructura **WMDMMetadataView** define la vista de metadatos.</span><span class="sxs-lookup"><span data-stu-id="9479d-106">The **WMDMMetadataView** structure defines the metadata view.</span></span> <span data-ttu-id="9479d-107">El contenido se organiza en función de esta definición.</span><span class="sxs-lookup"><span data-stu-id="9479d-107">Content is organized based on this definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9479d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9479d-108">Syntax</span></span>


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a><span data-ttu-id="9479d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9479d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="9479d-110">**pwszViewName**</span><span class="sxs-lookup"><span data-stu-id="9479d-110">**pwszViewName**</span></span>
</dt> <dd>

<span data-ttu-id="9479d-111">Puntero a una cadena de caracteres anchos terminada en null que contiene el nombre de la vista.</span><span class="sxs-lookup"><span data-stu-id="9479d-111">Pointer to a wide-character null-terminated string containing the name of the view.</span></span> <span data-ttu-id="9479d-112">Se utiliza como el nombre del nodo raíz en el que se presenta esta vista.</span><span class="sxs-lookup"><span data-stu-id="9479d-112">This is used as the name of the root node under which this view is presented.</span></span>

</dd> <dt>

<span data-ttu-id="9479d-113">**nDepth**</span><span class="sxs-lookup"><span data-stu-id="9479d-113">**nDepth**</span></span>
</dt> <dd>

<span data-ttu-id="9479d-114">Entero que contiene la profundidad de la vista, que indica el número de etiquetas de metadatos anidadas que se utilizan para la vista.</span><span class="sxs-lookup"><span data-stu-id="9479d-114">Integer containing the depth of the view, which indicates how many nested metadata tags are used for the view.</span></span>

</dd> <dt>

<span data-ttu-id="9479d-115">**ppwszTags**</span><span class="sxs-lookup"><span data-stu-id="9479d-115">**ppwszTags**</span></span>
</dt> <dd>

<span data-ttu-id="9479d-116">Matriz de cadenas de etiquetas de metadatos para las etiquetas anidadas.</span><span class="sxs-lookup"><span data-stu-id="9479d-116">Array of metadata tag strings for the nested tags.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9479d-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9479d-117">Examples</span></span>

<span data-ttu-id="9479d-118">En el código siguiente se crea una vista de metadatos:</span><span class="sxs-lookup"><span data-stu-id="9479d-118">The following code creates a metadata view:</span></span>


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



<span data-ttu-id="9479d-119">El código anterior organiza el contenido de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="9479d-119">The preceding code organizes content as follows:</span></span>

<dl> <span data-ttu-id="9479d-120">Mi vista</span><span class="sxs-lookup"><span data-stu-id="9479d-120">My View</span></span><dl> <span data-ttu-id="9479d-121">Genre1</span><span class="sxs-lookup"><span data-stu-id="9479d-121">Genre1</span></span><dl> <span data-ttu-id="9479d-122">Artist1</span><span class="sxs-lookup"><span data-stu-id="9479d-122">Artist1</span></span><dl> <span data-ttu-id="9479d-123">Album1</span><span class="sxs-lookup"><span data-stu-id="9479d-123">Album1</span></span><dl> <span data-ttu-id="9479d-124">Song1</span><span class="sxs-lookup"><span data-stu-id="9479d-124">Song1</span></span>  
<span data-ttu-id="9479d-125">Song2</span><span class="sxs-lookup"><span data-stu-id="9479d-125">Song2</span></span>  
<span data-ttu-id="9479d-126">...</span><span class="sxs-lookup"><span data-stu-id="9479d-126">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="9479d-127">Album1</span><span class="sxs-lookup"><span data-stu-id="9479d-127">Album1</span></span><dl> <span data-ttu-id="9479d-128">Song1</span><span class="sxs-lookup"><span data-stu-id="9479d-128">Song1</span></span>  
<span data-ttu-id="9479d-129">Song2</span><span class="sxs-lookup"><span data-stu-id="9479d-129">Song2</span></span>  
<span data-ttu-id="9479d-130">...</span><span class="sxs-lookup"><span data-stu-id="9479d-130">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> <span data-ttu-id="9479d-131">Artist1</span><span class="sxs-lookup"><span data-stu-id="9479d-131">Artist1</span></span><dl> <span data-ttu-id="9479d-132">Album1</span><span class="sxs-lookup"><span data-stu-id="9479d-132">Album1</span></span><dl> <span data-ttu-id="9479d-133">Song1</span><span class="sxs-lookup"><span data-stu-id="9479d-133">Song1</span></span>  
<span data-ttu-id="9479d-134">Song2</span><span class="sxs-lookup"><span data-stu-id="9479d-134">Song2</span></span>  
<span data-ttu-id="9479d-135">...</span><span class="sxs-lookup"><span data-stu-id="9479d-135">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="9479d-136">Album1</span><span class="sxs-lookup"><span data-stu-id="9479d-136">Album1</span></span><dl> <span data-ttu-id="9479d-137">Song1</span><span class="sxs-lookup"><span data-stu-id="9479d-137">Song1</span></span>  
<span data-ttu-id="9479d-138">Song2</span><span class="sxs-lookup"><span data-stu-id="9479d-138">Song2</span></span>  
<span data-ttu-id="9479d-139">...</span><span class="sxs-lookup"><span data-stu-id="9479d-139">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9479d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9479d-140">Requirements</span></span>



| <span data-ttu-id="9479d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9479d-141">Requirement</span></span> | <span data-ttu-id="9479d-142">Value</span><span class="sxs-lookup"><span data-stu-id="9479d-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9479d-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9479d-143">Header</span></span><br/> | <dl> <span data-ttu-id="9479d-144"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9479d-144"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9479d-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="9479d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9479d-146">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="9479d-146">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





