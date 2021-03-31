---
title: Estructura de VS_VERSIONINFO
description: Representa la organización de los datos en un recurso de versión de archivo. Es la estructura raíz que contiene todas las demás estructuras de información de versión de archivo.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- VS_VERSIONINFO menús de estructura y otros recursos
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151113"
---
# <a name="vs_versioninfo-structure"></a><span data-ttu-id="b506f-105">Estructura de VS \_ versionInfo</span><span class="sxs-lookup"><span data-stu-id="b506f-105">VS\_VERSIONINFO structure</span></span>

<span data-ttu-id="b506f-106">Representa la organización de los datos en un recurso de versión de archivo.</span><span class="sxs-lookup"><span data-stu-id="b506f-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="b506f-107">Es la estructura raíz que contiene todas las demás estructuras de información de versión de archivo.</span><span class="sxs-lookup"><span data-stu-id="b506f-107">It is the root structure that contains all other file-version information structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="b506f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b506f-108">Syntax</span></span>


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="b506f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b506f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b506f-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="b506f-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="b506f-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b506f-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b506f-112">La longitud, en bytes, de la estructura de **vs \_ versionInfo** .</span><span class="sxs-lookup"><span data-stu-id="b506f-112">The length, in bytes, of the **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="b506f-113">Esta longitud no incluye ningún relleno que alinee los datos de recursos de versiones posteriores en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b506f-113">This length does not include any padding that aligns any subsequent version resource data on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="b506f-114">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="b506f-114">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="b506f-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b506f-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b506f-116">La longitud, en bytes, del miembro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="b506f-116">The length, in bytes, of the **Value** member.</span></span> <span data-ttu-id="b506f-117">Este valor es cero si no hay ningún miembro de **valor** asociado a la estructura de la versión actual.</span><span class="sxs-lookup"><span data-stu-id="b506f-117">This value is zero if there is no **Value** member associated with the current version structure.</span></span>

</dd> <dt>

<span data-ttu-id="b506f-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="b506f-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="b506f-119">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b506f-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b506f-120">El tipo de datos del recurso de versión.</span><span class="sxs-lookup"><span data-stu-id="b506f-120">The type of data in the version resource.</span></span> <span data-ttu-id="b506f-121">Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.</span><span class="sxs-lookup"><span data-stu-id="b506f-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="b506f-122">**szKey**</span><span class="sxs-lookup"><span data-stu-id="b506f-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="b506f-123">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="b506f-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="b506f-124">Cadena Unicode L "información de \_ versión de vs \_ ".</span><span class="sxs-lookup"><span data-stu-id="b506f-124">The Unicode string L"VS\_VERSION\_INFO".</span></span>

</dd> <dt>

<span data-ttu-id="b506f-125">**Padding1**</span><span class="sxs-lookup"><span data-stu-id="b506f-125">**Padding1**</span></span>
</dt> <dd>

<span data-ttu-id="b506f-126">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b506f-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b506f-127">Contiene tantas palabras cero como sea necesario para alinear el miembro de **valor** en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b506f-127">Contains as many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="b506f-128">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b506f-128">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="b506f-129">Tipo: **[ **vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span><span class="sxs-lookup"><span data-stu-id="b506f-129">Type: **[**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span></span>

</dd> <dd>

<span data-ttu-id="b506f-130">Datos arbitrarios asociados con esta estructura de **vs \_ versionInfo** .</span><span class="sxs-lookup"><span data-stu-id="b506f-130">Arbitrary data associated with this **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="b506f-131">El miembro **wValueLength** especifica la longitud de este miembro; Si **wValueLength** es cero, este miembro no existe.</span><span class="sxs-lookup"><span data-stu-id="b506f-131">The **wValueLength** member specifies the length of this member; if **wValueLength** is zero, this member does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b506f-132">**Padding2**</span><span class="sxs-lookup"><span data-stu-id="b506f-132">**Padding2**</span></span>
</dt> <dd>

<span data-ttu-id="b506f-133">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b506f-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b506f-134">Tantas palabras como sea necesario para alinear el miembro **secundario** en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b506f-134">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span> <span data-ttu-id="b506f-135">Estos bytes no se incluyen en **wValueLength**.</span><span class="sxs-lookup"><span data-stu-id="b506f-135">These bytes are not included in **wValueLength**.</span></span> <span data-ttu-id="b506f-136">Este miembro es opcional.</span><span class="sxs-lookup"><span data-stu-id="b506f-136">This member is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b506f-137">**Children**</span><span class="sxs-lookup"><span data-stu-id="b506f-137">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="b506f-138">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b506f-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b506f-139">Una matriz de cero o una estructura [**StringFileInfo**](stringfileinfo.md) , y una o ninguna de las estructuras [**VarFileInfo**](varfileinfo.md) que son elementos secundarios de la estructura actual de **vs \_ versionInfo** .</span><span class="sxs-lookup"><span data-stu-id="b506f-139">An array of zero or one [**StringFileInfo**](stringfileinfo.md) structures, and zero or one [**VarFileInfo**](varfileinfo.md) structures that are children of the current **VS\_VERSIONINFO** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b506f-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b506f-140">Remarks</span></span>

<span data-ttu-id="b506f-141">Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="b506f-141">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="b506f-142">Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="b506f-142">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="b506f-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b506f-143">Requirements</span></span>



| <span data-ttu-id="b506f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b506f-144">Requirement</span></span> | <span data-ttu-id="b506f-145">Value</span><span class="sxs-lookup"><span data-stu-id="b506f-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b506f-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b506f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b506f-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b506f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b506f-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b506f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b506f-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b506f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b506f-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="b506f-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="b506f-151">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b506f-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b506f-152">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="b506f-152">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="b506f-153">**VerQueryValue**</span><span class="sxs-lookup"><span data-stu-id="b506f-153">**VerQueryValue**</span></span>](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[<span data-ttu-id="b506f-154">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="b506f-154">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="b506f-155">**VS \_ FIXEDFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="b506f-155">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

<span data-ttu-id="b506f-156">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b506f-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b506f-157">Información de versión</span><span class="sxs-lookup"><span data-stu-id="b506f-157">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





