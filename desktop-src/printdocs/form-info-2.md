---
description: Contiene información sobre un formulario de impresión traducible.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: Estructura de FORM_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276659"
---
# <a name="form_info_2-structure"></a><span data-ttu-id="81374-103">Estructura del formulario de \_ información \_ 2</span><span class="sxs-lookup"><span data-stu-id="81374-103">FORM\_INFO\_2 structure</span></span>

<span data-ttu-id="81374-104">Contiene información sobre un formulario de impresión traducible.</span><span class="sxs-lookup"><span data-stu-id="81374-104">Contains information about a localizable print form.</span></span>

## <a name="syntax"></a><span data-ttu-id="81374-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81374-105">Syntax</span></span>


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a><span data-ttu-id="81374-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="81374-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="81374-107">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="81374-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="81374-108">Propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="81374-108">The form properties.</span></span> <span data-ttu-id="81374-109">Se definen los valores siguientes, pero solo se puede establecer uno.</span><span class="sxs-lookup"><span data-stu-id="81374-109">The following values are defined, but only one can be set.</span></span> <span data-ttu-id="81374-110">Cuando [**GetForm**](getform.md) o [**EnumForms**](enumforms.md)devuelven el **formulario de \_ información \_ 2** , **Flags** se establece en el valor actual de la base de datos de formularios.</span><span class="sxs-lookup"><span data-stu-id="81374-110">When the **FORM\_INFO\_2** is returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md), **Flags** is set to the current value in the forms database.</span></span>



| <span data-ttu-id="81374-111">Value</span><span class="sxs-lookup"><span data-stu-id="81374-111">Value</span></span>         | <span data-ttu-id="81374-112">Significado</span><span class="sxs-lookup"><span data-stu-id="81374-112">Meaning</span></span>                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81374-113">usuario de formulario \_</span><span class="sxs-lookup"><span data-stu-id="81374-113">FORM\_USER</span></span>    | <span data-ttu-id="81374-114">Si se establece esta marca de bits, el formulario lo ha definido el usuario.</span><span class="sxs-lookup"><span data-stu-id="81374-114">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="81374-115">Los formularios con este marcador se definen en el registro.</span><span class="sxs-lookup"><span data-stu-id="81374-115">Forms with this flag set are defined in the registry.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="81374-116">Builtin de formulario \_</span><span class="sxs-lookup"><span data-stu-id="81374-116">FORM\_BUILTIN</span></span> | <span data-ttu-id="81374-117">Si se establece esta marca de bits, el formulario forma parte del administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="81374-117">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="81374-118">Las definiciones de formulario con este marcador establecido no aparecen en el registro.</span><span class="sxs-lookup"><span data-stu-id="81374-118">Form definitions with this flag set do not appear in the registry.</span></span> <span data-ttu-id="81374-119">Los formularios integrados no se pueden modificar, por lo que no se debe establecer esta marca cuando la estructura se pasa a [**AddForm**](addform.md) o [**SetForm**](setform.md).</span><span class="sxs-lookup"><span data-stu-id="81374-119">Built-in forms cannot be modified, so this flag should not be set when the structure is passed to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> |
| <span data-ttu-id="81374-120">impresora de formulario \_</span><span class="sxs-lookup"><span data-stu-id="81374-120">FORM\_PRINTER</span></span> | <span data-ttu-id="81374-121">Si se establece esta marca de bits, el formulario está asociado a una impresora determinada y su definición aparece en el registro.</span><span class="sxs-lookup"><span data-stu-id="81374-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="81374-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="81374-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="81374-123">Puntero a una cadena terminada en null que especifica el nombre del formulario.</span><span class="sxs-lookup"><span data-stu-id="81374-123">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="81374-124">El nombre del formulario no puede superar los 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="81374-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="81374-125">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="81374-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="81374-126">Ancho y alto del formulario en milésimas de milímetro.</span><span class="sxs-lookup"><span data-stu-id="81374-126">The width and height of the form in thousandths of millimeters.</span></span>

</dd> <dt>

<span data-ttu-id="81374-127">**ImageableArea**</span><span class="sxs-lookup"><span data-stu-id="81374-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="81374-128">Ancho y alto, en milésimas de milímetro, del área de la página en la que la impresora puede imprimir.</span><span class="sxs-lookup"><span data-stu-id="81374-128">The width and height, in thousandths of millimeters, of the area of the page on which the printer can print.</span></span>

</dd> <dt>

<span data-ttu-id="81374-129">**pKeyword**</span><span class="sxs-lookup"><span data-stu-id="81374-129">**pKeyword**</span></span>
</dt> <dd>

<span data-ttu-id="81374-130">Un puntero a un identificador de cadena no traducible del formulario.</span><span class="sxs-lookup"><span data-stu-id="81374-130">A pointer to a non-localizable string identifier of the form.</span></span> <span data-ttu-id="81374-131">Cuando se pasa a [**AddForm**](addform.md) o [**SetForm**](setform.md), proporciona al llamador un medio para identificar el formulario en todas las configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="81374-131">When passed to [**AddForm**](addform.md) or [**SetForm**](setform.md), this gives the caller a means of identifying the form in all locales.</span></span>

</dd> <dt>

<span data-ttu-id="81374-132">**StringType**</span><span class="sxs-lookup"><span data-stu-id="81374-132">**StringType**</span></span>
</dt> <dd>

<span data-ttu-id="81374-133">Especifica cómo se obtiene un nombre para mostrar localizado del formulario en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="81374-133">Specifies how a localized display name for the form is obtained at runtime.</span></span> <span data-ttu-id="81374-134">Se definen los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="81374-134">The following values are defined.</span></span> <span data-ttu-id="81374-135">Solo se puede establecer una en una llamada determinada a [**AddForm**](addform.md) o [**SetForm**](setform.md).</span><span class="sxs-lookup"><span data-stu-id="81374-135">Only one can be set in any given call to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> <span data-ttu-id="81374-136">Tanto \_ la cadena MUIDLL como \_ la cadena LANGPAIR se pueden establecer con la **forma \_ info \_ 2** (s) devuelta por [**GetForm**](getform.md) o [**EnumForms**](enumforms.md).</span><span class="sxs-lookup"><span data-stu-id="81374-136">Both STRING\_MUIDLL and STRING\_LANGPAIR can be set in the **FORM\_INFO\_2** (s) returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md).</span></span> <span data-ttu-id="81374-137">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="81374-137">See Remarks.</span></span>



| <span data-ttu-id="81374-138">Value</span><span class="sxs-lookup"><span data-stu-id="81374-138">Value</span></span>            | <span data-ttu-id="81374-139">Significado</span><span class="sxs-lookup"><span data-stu-id="81374-139">Meaning</span></span>                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81374-140">CADENA \_ None</span><span class="sxs-lookup"><span data-stu-id="81374-140">STRING\_NONE</span></span>     | <span data-ttu-id="81374-141">No hay ningún nombre para mostrar localizado.</span><span class="sxs-lookup"><span data-stu-id="81374-141">There is no localized display name.</span></span>                                                                                                                                                            |
| <span data-ttu-id="81374-142">CADENA \_ MUIDLL</span><span class="sxs-lookup"><span data-stu-id="81374-142">STRING\_MUIDLL</span></span>   | <span data-ttu-id="81374-143">El nombre para mostrar se extrae de la DLL de recursos localizados de la [interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management) especificada en **pMuiDll**.</span><span class="sxs-lookup"><span data-stu-id="81374-143">The display name is extracted from the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resources DLL specified in **pMuiDll**.</span></span> <span data-ttu-id="81374-144">El identificador está en el miembro **dwResourceId** .</span><span class="sxs-lookup"><span data-stu-id="81374-144">The ID is in the **dwResourceId** member.</span></span> |
| <span data-ttu-id="81374-145">CADENA \_ LANGPAIR</span><span class="sxs-lookup"><span data-stu-id="81374-145">STRING\_LANGPAIR</span></span> | <span data-ttu-id="81374-146">El nombre para mostrar y el identificador de idioma se proporcionan directamente mediante **pDisplayName** y el idioma lo especifica **wLangId**.</span><span class="sxs-lookup"><span data-stu-id="81374-146">The display name and language ID are provided directly by **pDisplayName** and the language is specified by **wLangId**.</span></span>                                                                       |



 

</dd> <dt>

<span data-ttu-id="81374-147">**pMuiDll**</span><span class="sxs-lookup"><span data-stu-id="81374-147">**pMuiDll**</span></span>
</dt> <dd>

<span data-ttu-id="81374-148">La DLL de recursos localizados de la [interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management) que contiene el nombre para mostrar localizado.</span><span class="sxs-lookup"><span data-stu-id="81374-148">The [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resource DLL that contains the localized display name.</span></span>

</dd> <dt>

<span data-ttu-id="81374-149">**dwResourceId**</span><span class="sxs-lookup"><span data-stu-id="81374-149">**dwResourceId**</span></span>
</dt> <dd>

<span data-ttu-id="81374-150">El identificador de recurso del nombre para mostrar del formulario en **pMuiDll**.</span><span class="sxs-lookup"><span data-stu-id="81374-150">The resource ID of the form's display name in **pMuiDll**.</span></span>

</dd> <dt>

<span data-ttu-id="81374-151">**pDisplayName**</span><span class="sxs-lookup"><span data-stu-id="81374-151">**pDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="81374-152">Nombre para mostrar del formulario en el idioma especificado por **wLangId**.</span><span class="sxs-lookup"><span data-stu-id="81374-152">The form's display name in the language specified by **wLangId**.</span></span>

</dd> <dt>

<span data-ttu-id="81374-153">**wLangId**</span><span class="sxs-lookup"><span data-stu-id="81374-153">**wLangId**</span></span>
</dt> <dd>

<span data-ttu-id="81374-154">El idioma de **pDisplayName**.</span><span class="sxs-lookup"><span data-stu-id="81374-154">The language of the **pDisplayName**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81374-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81374-155">Remarks</span></span>

<span data-ttu-id="81374-156">En una llamada a [**AddForm**](addform.md) o [**SetForm**](setform.md):</span><span class="sxs-lookup"><span data-stu-id="81374-156">On a call to [**AddForm**](addform.md) or [**SetForm**](setform.md):</span></span>

-   <span data-ttu-id="81374-157">Si **StringType** es de tipo String \_ None, tanto **pMuiDll** como **pDisplayName** deben ser **null** y **dwResourceId** y **wLangId** deben ser 0.</span><span class="sxs-lookup"><span data-stu-id="81374-157">If **StringType** is STRING\_NONE, both **pMuiDll** and **pDisplayName** must be **NULL** and both **dwResourceId** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="81374-158">Si **StringType** es de tipo String \_ MUIDLL, **pDisplayName** debe ser **null** y **wLangId** debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="81374-158">If **StringType** is STRING\_MUIDLL, **pDisplayName** must be **NULL** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="81374-159">Si **StringType** es de tipo String \_ LANGPAIR, **pMuiDll** debe ser **null** y **dwResourceId** debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="81374-159">If **StringType** is STRING\_LANGPAIR, **pMuiDll** must be **NULL** and **dwResourceId** must be 0.</span></span>

<span data-ttu-id="81374-160">Para un **formulario de \_ información \_ 2** devuelto por una llamada a [**GetForm**](getform.md) o [**EnumForms**](enumforms.md):</span><span class="sxs-lookup"><span data-stu-id="81374-160">For a **FORM\_INFO\_2** returned by a call to [**GetForm**](getform.md) or [**EnumForms**](enumforms.md):</span></span>

-   <span data-ttu-id="81374-161">Si **StringType** es tanto String \_ MUIDLL como String \_ LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId** y **wLangId** tendrán valores válidos.</span><span class="sxs-lookup"><span data-stu-id="81374-161">If **StringType** is both STRING\_MUIDLL and STRING\_LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId**, and **wLangId** will all have valid values.</span></span>
-   <span data-ttu-id="81374-162">Si **StringType** es de tipo cadena \_ MUIDLL, **pMuiDll** y **dwResourceId** tendrán valores válidos.</span><span class="sxs-lookup"><span data-stu-id="81374-162">If **StringType** is STRING\_MUIDLL only, **pMuiDll** and **dwResourceId** will have valid values.</span></span> <span data-ttu-id="81374-163">**pDisplayName** será **null** y **wLangId** será 0.</span><span class="sxs-lookup"><span data-stu-id="81374-163">**pDisplayName** will be **NULL** and **wLangId** will be 0.</span></span>
-   <span data-ttu-id="81374-164">Si **StringType** es de tipo cadena \_ LANGPAIR, **pDisplayName** y **wLangId** tendrán valores válidos.</span><span class="sxs-lookup"><span data-stu-id="81374-164">If **StringType** is STRING\_LANGPAIR only, **pDisplayName** and **wLangId** will have valid values.</span></span> <span data-ttu-id="81374-165">**pMuiDll** será **null** y **dwResourceId** será 0.</span><span class="sxs-lookup"><span data-stu-id="81374-165">**pMuiDll** will be **NULL** and **dwResourceId** will be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="81374-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81374-166">Requirements</span></span>



| <span data-ttu-id="81374-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="81374-167">Requirement</span></span> | <span data-ttu-id="81374-168">Value</span><span class="sxs-lookup"><span data-stu-id="81374-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81374-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81374-169">Minimum supported client</span></span><br/> | <span data-ttu-id="81374-170">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="81374-170">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="81374-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81374-171">Minimum supported server</span></span><br/> | <span data-ttu-id="81374-172">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="81374-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="81374-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81374-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="81374-174"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81374-174"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="81374-175">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="81374-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="81374-176">**\_ Form \_ info \_ 2W** (Unicode) y **\_ Form \_ info \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="81374-176">**\_FORM\_INFO\_2W** (Unicode) and **\_FORM\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="81374-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="81374-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81374-178">Impresión</span><span class="sxs-lookup"><span data-stu-id="81374-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="81374-179">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="81374-179">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="81374-180">Interfaz de usuario multilingüe</span><span class="sxs-lookup"><span data-stu-id="81374-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[<span data-ttu-id="81374-181">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="81374-181">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="81374-182">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="81374-182">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="81374-183">**EnumForms**</span><span class="sxs-lookup"><span data-stu-id="81374-183">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="81374-184">**SetForm**</span><span class="sxs-lookup"><span data-stu-id="81374-184">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

