---
title: Estructura var
description: Representa la organización de los datos en un recurso de versión de archivo. Normalmente contiene una lista de los pares de idioma y de identificador de página de códigos que admite la versión de la aplicación o DLL.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Menús de estructura var y otros recursos
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905607"
---
# <a name="var-structure"></a><span data-ttu-id="c705a-105">Estructura var</span><span class="sxs-lookup"><span data-stu-id="c705a-105">Var structure</span></span>

<span data-ttu-id="c705a-106">Representa la organización de los datos en un recurso de versión de archivo.</span><span class="sxs-lookup"><span data-stu-id="c705a-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="c705a-107">Normalmente contiene una lista de los pares de idioma y de identificador de página de códigos que admite la versión de la aplicación o DLL.</span><span class="sxs-lookup"><span data-stu-id="c705a-107">It typically contains a list of language and code page identifier pairs that the version of the application or DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="c705a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c705a-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a><span data-ttu-id="c705a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c705a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c705a-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="c705a-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="c705a-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c705a-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c705a-112">Longitud, en bytes, de la estructura **var** .</span><span class="sxs-lookup"><span data-stu-id="c705a-112">The length, in bytes, of the **Var** structure.</span></span>

</dd> <dt>

<span data-ttu-id="c705a-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="c705a-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="c705a-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c705a-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c705a-115">La longitud, en bytes, del miembro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="c705a-115">The length, in bytes, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="c705a-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="c705a-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="c705a-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c705a-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c705a-118">El tipo de datos del recurso de versión.</span><span class="sxs-lookup"><span data-stu-id="c705a-118">The type of data in the version resource.</span></span> <span data-ttu-id="c705a-119">Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.</span><span class="sxs-lookup"><span data-stu-id="c705a-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="c705a-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="c705a-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="c705a-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="c705a-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="c705a-122">Cadena Unicode L "Translation".</span><span class="sxs-lookup"><span data-stu-id="c705a-122">The Unicode string L"Translation".</span></span>

</dd> <dt>

<span data-ttu-id="c705a-123">**Relleno**</span><span class="sxs-lookup"><span data-stu-id="c705a-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="c705a-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c705a-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c705a-125">Tantas palabras como sea necesario para alinear el miembro de **valor** en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c705a-125">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="c705a-126">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c705a-126">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="c705a-127">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c705a-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c705a-128">Matriz de uno o más valores que son pares de identificador de idioma y página de códigos.</span><span class="sxs-lookup"><span data-stu-id="c705a-128">An array of one or more values that are language and code page identifier pairs.</span></span> <span data-ttu-id="c705a-129">Para obtener más información, vea la sección Comentarios siguiente.</span><span class="sxs-lookup"><span data-stu-id="c705a-129">For additional information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c705a-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c705a-130">Remarks</span></span>

<span data-ttu-id="c705a-131">Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="c705a-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="c705a-132">Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="c705a-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="c705a-133">Si usa la estructura **var** para enumerar los idiomas admitidos por la aplicación o el archivo dll en lugar de usar varios recursos de versión, use el miembro de **valor** para contener una matriz de valores **DWORD** que indiquen las combinaciones de idioma y página de códigos admitidas por este archivo.</span><span class="sxs-lookup"><span data-stu-id="c705a-133">If you use the **Var** structure to list the languages your application or DLL supports instead of using multiple version resources, use the **Value** member to contain an array of **DWORD** values indicating the language and code page combinations supported by this file.</span></span> <span data-ttu-id="c705a-134">La palabra de orden inferior de cada **DWORD** debe contener un identificador de idioma de Microsoft y la palabra de orden superior debe contener el número de página de códigos de IBM.</span><span class="sxs-lookup"><span data-stu-id="c705a-134">The low-order word of each **DWORD** must contain a Microsoft language identifier, and the high-order word must contain the IBM code page number.</span></span> <span data-ttu-id="c705a-135">La palabra de orden superior o de orden inferior puede ser cero, lo que indica que el archivo es independiente del idioma o de la página de códigos.</span><span class="sxs-lookup"><span data-stu-id="c705a-135">Either high-order or low-order word can be zero, indicating that the file is language or code page independent.</span></span> <span data-ttu-id="c705a-136">Si se omite la estructura **var** , el archivo se interpretará como independiente del lenguaje y de la página de códigos.</span><span class="sxs-lookup"><span data-stu-id="c705a-136">If the **Var** structure is omitted, the file will be interpreted as both language and code page independent.</span></span>

## <a name="requirements"></a><span data-ttu-id="c705a-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c705a-137">Requirements</span></span>



| <span data-ttu-id="c705a-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c705a-138">Requirement</span></span> | <span data-ttu-id="c705a-139">Value</span><span class="sxs-lookup"><span data-stu-id="c705a-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c705a-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c705a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c705a-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c705a-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c705a-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c705a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c705a-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c705a-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c705a-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="c705a-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="c705a-145">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c705a-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c705a-146">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="c705a-146">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="c705a-147">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="c705a-147">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="c705a-148">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="c705a-148">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="c705a-149">**VS \_ versionInfo**</span><span class="sxs-lookup"><span data-stu-id="c705a-149">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="c705a-150">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c705a-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c705a-151">Información de versión</span><span class="sxs-lookup"><span data-stu-id="c705a-151">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





