---
title: Estructura StringFileInfo
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene información de versión que se puede mostrar para un idioma y una página de códigos determinados.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Menús de la estructura StringFileInfo y otros recursos
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996065"
---
# <a name="stringfileinfo-structure"></a><span data-ttu-id="6a318-105">Estructura StringFileInfo</span><span class="sxs-lookup"><span data-stu-id="6a318-105">StringFileInfo structure</span></span>

<span data-ttu-id="6a318-106">Representa la organización de los datos en un recurso de versión de archivo.</span><span class="sxs-lookup"><span data-stu-id="6a318-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="6a318-107">Contiene información de versión que se puede mostrar para un idioma y una página de códigos determinados.</span><span class="sxs-lookup"><span data-stu-id="6a318-107">It contains version information that can be displayed for a particular language and code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a318-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a318-108">Syntax</span></span>


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a><span data-ttu-id="6a318-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a318-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6a318-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="6a318-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="6a318-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="6a318-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6a318-112">La longitud, en bytes, del bloque **StringFileInfo** completo, incluidas todas las estructuras indicadas por el miembro **secundario** .</span><span class="sxs-lookup"><span data-stu-id="6a318-112">The length, in bytes, of the entire **StringFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="6a318-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="6a318-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="6a318-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="6a318-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6a318-115">Este miembro siempre es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="6a318-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6a318-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="6a318-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="6a318-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="6a318-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6a318-118">El tipo de datos del recurso de versión.</span><span class="sxs-lookup"><span data-stu-id="6a318-118">The type of data in the version resource.</span></span> <span data-ttu-id="6a318-119">Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.</span><span class="sxs-lookup"><span data-stu-id="6a318-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="6a318-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="6a318-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="6a318-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="6a318-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="6a318-122">Cadena Unicode L "StringFileInfo".</span><span class="sxs-lookup"><span data-stu-id="6a318-122">The Unicode string L"StringFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="6a318-123">**Relleno**</span><span class="sxs-lookup"><span data-stu-id="6a318-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="6a318-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="6a318-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6a318-125">Tantas palabras como sea necesario para alinear el miembro **secundario** en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6a318-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="6a318-126">**Children**</span><span class="sxs-lookup"><span data-stu-id="6a318-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="6a318-127">Tipo: **[ **StringTable**](stringtable.md)**</span><span class="sxs-lookup"><span data-stu-id="6a318-127">Type: **[**StringTable**](stringtable.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6a318-128">Una matriz de una o más estructuras de [**StringTable**](stringtable.md) .</span><span class="sxs-lookup"><span data-stu-id="6a318-128">An array of one or more [**StringTable**](stringtable.md) structures.</span></span> <span data-ttu-id="6a318-129">Cada miembro **szKey** de la estructura **stringtable** indica el idioma y la página de códigos adecuados para mostrar el texto en esa estructura de **stringtable** .</span><span class="sxs-lookup"><span data-stu-id="6a318-129">Each **StringTable** structure's **szKey** member indicates the appropriate language and code page for displaying the text in that **StringTable** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a318-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a318-130">Remarks</span></span>

<span data-ttu-id="6a318-131">Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="6a318-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="6a318-132">Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="6a318-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="6a318-133">El miembro **secundario** de la estructura de [**vs \_ versionInfo**](vs-versioninfo.md) puede contener cero o más estructuras **StringFileInfo** .</span><span class="sxs-lookup"><span data-stu-id="6a318-133">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or more **StringFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a318-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a318-134">Requirements</span></span>



| <span data-ttu-id="6a318-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a318-135">Requirement</span></span> | <span data-ttu-id="6a318-136">Value</span><span class="sxs-lookup"><span data-stu-id="6a318-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6a318-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a318-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6a318-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6a318-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6a318-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a318-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6a318-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6a318-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6a318-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a318-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a318-142">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6a318-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6a318-143">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="6a318-143">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="6a318-144">**String@**</span><span class="sxs-lookup"><span data-stu-id="6a318-144">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="6a318-145">**VS \_ versionInfo**</span><span class="sxs-lookup"><span data-stu-id="6a318-145">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="6a318-146">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6a318-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6a318-147">Información de versión</span><span class="sxs-lookup"><span data-stu-id="6a318-147">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





