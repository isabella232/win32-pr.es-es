---
title: StringTable (estructura)
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene información sobre el formato del idioma y la página de códigos para las cadenas especificadas por el miembro secundario. Una página de códigos es un juego de caracteres ordenado.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Menús de la estructura StringTable y otros recursos
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422054"
---
# <a name="stringtable-structure"></a><span data-ttu-id="4d9a0-106">StringTable (estructura)</span><span class="sxs-lookup"><span data-stu-id="4d9a0-106">StringTable structure</span></span>

<span data-ttu-id="4d9a0-107">Representa la organización de los datos en un recurso de versión de archivo.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-107">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="4d9a0-108">Contiene información sobre el formato del idioma y la página de códigos para las cadenas especificadas por el miembro **secundario** .</span><span class="sxs-lookup"><span data-stu-id="4d9a0-108">It contains language and code page formatting information for the strings specified by the **Children** member.</span></span> <span data-ttu-id="4d9a0-109">Una página de códigos es un juego de caracteres ordenado.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-109">A code page is an ordered character set.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d9a0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d9a0-110">Syntax</span></span>


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a><span data-ttu-id="4d9a0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d9a0-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d9a0-112">**wLength**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-112">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="4d9a0-113">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-113">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4d9a0-114">La longitud, en bytes, de esta estructura **StringTable** , incluidas todas las estructuras indicadas por el miembro **secundario** .</span><span class="sxs-lookup"><span data-stu-id="4d9a0-114">The length, in bytes, of this **StringTable** structure, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="4d9a0-115">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-115">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="4d9a0-116">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4d9a0-117">Este miembro siempre es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-117">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4d9a0-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="4d9a0-119">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4d9a0-120">El tipo de datos del recurso de versión.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-120">The type of data in the version resource.</span></span> <span data-ttu-id="4d9a0-121">Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="4d9a0-122">**szKey**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="4d9a0-123">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="4d9a0-124">Número hexadecimal de 8 dígitos almacenado como una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-124">An 8-digit hexadecimal number stored as a Unicode string.</span></span> <span data-ttu-id="4d9a0-125">Los cuatro dígitos más significativos representan el identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-125">The four most significant digits represent the language identifier.</span></span> <span data-ttu-id="4d9a0-126">Los cuatro dígitos menos significativos representan la página de códigos para la que se da formato a los datos.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-126">The four least significant digits represent the code page for which the data is formatted.</span></span> <span data-ttu-id="4d9a0-127">Cada identificador de idioma de Microsoft Standard contiene dos partes: los bits de orden inferior 10 especifican el idioma principal y los 6 bits de orden superior especifican el subidioma.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-127">Each Microsoft Standard Language identifier contains two parts: the low-order 10 bits specify the major language, and the high-order 6 bits specify the sublanguage.</span></span> <span data-ttu-id="4d9a0-128">Para obtener una tabla de identificadores válidos, vea.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-128">For a table of valid identifiers see .</span></span>

</dd> <dt>

<span data-ttu-id="4d9a0-129">**Relleno**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-129">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="4d9a0-130">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-130">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4d9a0-131">Tantas palabras como sea necesario para alinear el miembro **secundario** en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-131">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="4d9a0-132">**Children**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-132">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="4d9a0-133">Tipo: **[ **String**](string-str.md)**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-133">Type: **[**String**](string-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4d9a0-134">Una matriz de una o más estructuras de [**cadena**](string-str.md) .</span><span class="sxs-lookup"><span data-stu-id="4d9a0-134">An array of one or more [**String**](string-str.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d9a0-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d9a0-135">Remarks</span></span>

<span data-ttu-id="4d9a0-136">Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-136">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="4d9a0-137">Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-137">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="4d9a0-138">El miembro **secundario** de la estructura [**StringFileInfo**](stringfileinfo.md) contiene al menos una estructura **StringTable** .</span><span class="sxs-lookup"><span data-stu-id="4d9a0-138">The **Children** member of the [**StringFileInfo**](stringfileinfo.md) structure contains at least one **StringTable** structure.</span></span>

<span data-ttu-id="4d9a0-139">Establezca la parte de la página de códigos del miembro **szKey** en el valor hexadecimal 0x04b0 para indicar la página de códigos Unicode o en el valor hexadecimal de la página de códigos que sea adecuado para el componente de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-139">Set the code page portion of the **szKey** member to the hexadecimal value 0x04b0 to indicate the Unicode code page, or to the hexadecimal value of the code page that is appropriate for the language component.</span></span> <span data-ttu-id="4d9a0-140">Después de elegir el valor de la página de códigos, debe continuar usando el mismo valor en las revisiones posteriores del archivo.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-140">After you choose the value for the code page you should continue to use the same value in later revisions to the file.</span></span>

<span data-ttu-id="4d9a0-141">Un archivo ejecutable o DLL que admita varios idiomas debe tener un recurso de versión para cada idioma, en lugar de un único recurso de versión que contenga cadenas en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="4d9a0-141">An executable file or DLL that supports multiple languages should have a version resource for each language, rather than a single version resource that contains strings in several languages.</span></span> <span data-ttu-id="4d9a0-142">Sin embargo, si usa la estructura [**var**](var-str.md) para enumerar los idiomas que admite la aplicación, el número de estructuras **StringTable** en el recurso de versión está directamente relacionado con el número de pares de identificador de idioma/página de códigos en el miembro de **valor** de la estructura **var** .</span><span class="sxs-lookup"><span data-stu-id="4d9a0-142">However, if you use the [**Var**](var-str.md) structure to list the languages that your application supports, the number of **StringTable** structures in the version resource is directly related to the number of language/code page identifier pairs in the **Value** member of the **Var** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d9a0-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d9a0-143">Requirements</span></span>



| <span data-ttu-id="4d9a0-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d9a0-144">Requirement</span></span> | <span data-ttu-id="4d9a0-145">Value</span><span class="sxs-lookup"><span data-stu-id="4d9a0-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4d9a0-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d9a0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4d9a0-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4d9a0-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4d9a0-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d9a0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4d9a0-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4d9a0-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4d9a0-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d9a0-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="4d9a0-151">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4d9a0-152">**String@**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-152">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="4d9a0-153">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-153">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="4d9a0-154">**Distribuidor**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-154">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="4d9a0-155">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-155">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="4d9a0-156">**VS \_ versionInfo**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-156">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="4d9a0-157">**Vista**</span><span class="sxs-lookup"><span data-stu-id="4d9a0-157">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4d9a0-158">Información de versión</span><span class="sxs-lookup"><span data-stu-id="4d9a0-158">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





