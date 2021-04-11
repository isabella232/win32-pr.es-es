---
description: Proporciona información a los métodos de la interfaz IQueryAssociations.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Enumeración ASSOCF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279851"
---
# <a name="assocf-enumeration"></a><span data-ttu-id="832cc-103">Enumeración ASSOCF</span><span class="sxs-lookup"><span data-stu-id="832cc-103">ASSOCF enumeration</span></span>

<span data-ttu-id="832cc-104">Proporciona información a los métodos de la interfaz [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .</span><span class="sxs-lookup"><span data-stu-id="832cc-104">Provides information to the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="832cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="832cc-105">Syntax</span></span>

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="832cc-106">C++</span><span class="sxs-lookup"><span data-stu-id="832cc-106">C++</span></span></th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a><span data-ttu-id="832cc-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="832cc-107">Constants</span></span>

 <span data-ttu-id="832cc-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="832cc-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF\_NONE**</span></span> 

<span data-ttu-id="832cc-109">No se ha establecido ninguna de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="832cc-109">None of the following options are set.</span></span>

 <span data-ttu-id="832cc-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ init \_ NOREMAPCLSID**</span><span class="sxs-lookup"><span data-stu-id="832cc-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF\_INIT\_NOREMAPCLSID**</span></span> 

<span data-ttu-id="832cc-111">Indica a los métodos de interfaz [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que no asignen valores CLSID a los valores ProgID.</span><span class="sxs-lookup"><span data-stu-id="832cc-111">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods not to map CLSID values to ProgID values.</span></span>

 <span data-ttu-id="832cc-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ init \_ BYEXENAME**</span><span class="sxs-lookup"><span data-stu-id="832cc-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF\_INIT\_BYEXENAME**</span></span> 

<span data-ttu-id="832cc-113">Identifica el valor del parámetro *pwszAssoc* de [**IQueryAssociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) como nombre de archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="832cc-113">Identifies the value of the *pwszAssoc* parameter of [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) as an executable file name.</span></span> <span data-ttu-id="832cc-114">Si no se establece esta marca, la clave raíz se establecerá en el identificador de programa (ProgID) asociado a la clave **. exe** en lugar del identificador de programa (ProgID) del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="832cc-114">If this flag is not set, the root key will be set to the ProgID associated with the **.exe** key instead of the executable file's ProgID.</span></span>

 <span data-ttu-id="832cc-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ abrir \_ BYEXENAME**</span><span class="sxs-lookup"><span data-stu-id="832cc-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF\_OPEN\_BYEXENAME**</span></span> 

<span data-ttu-id="832cc-116">Idéntico a **ASSOCF \_ init \_ BYEXENAME**.</span><span class="sxs-lookup"><span data-stu-id="832cc-116">Identical to **ASSOCF\_INIT\_BYEXENAME**.</span></span>

 <span data-ttu-id="832cc-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ init \_ DEFAULTTOSTAR**</span><span class="sxs-lookup"><span data-stu-id="832cc-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF\_INIT\_DEFAULTTOSTAR**</span></span> 

<span data-ttu-id="832cc-118">Especifica que cuando un método [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) no encuentra el valor solicitado bajo la clave raíz, debe intentar recuperar el valor comparable de la **\*** subclave.</span><span class="sxs-lookup"><span data-stu-id="832cc-118">Specifies that when an [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **\*** subkey.</span></span>

 <span data-ttu-id="832cc-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ init \_ DEFAULTTOFOLDER**</span><span class="sxs-lookup"><span data-stu-id="832cc-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF\_INIT\_DEFAULTTOFOLDER**</span></span> 

<span data-ttu-id="832cc-120">Especifica que cuando un método [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) no encuentra el valor solicitado bajo la clave raíz, debe intentar recuperar el valor comparable de la subclave de **carpeta** .</span><span class="sxs-lookup"><span data-stu-id="832cc-120">Specifies that when a [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **Folder** subkey.</span></span>

 <span data-ttu-id="832cc-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="832cc-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF\_NOUSERSETTINGS**</span></span> 

<span data-ttu-id="832cc-122">Especifica que solo se debe buscar en la **\_ \_ raíz de las clases HKEY** y que el **\_ \_ usuario actual de HKEY** debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="832cc-122">Specifies that only **HKEY\_CLASSES\_ROOT** should be searched, and that **HKEY\_CURRENT\_USER** should be ignored.</span></span>

 <span data-ttu-id="832cc-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOtruncate**</span><span class="sxs-lookup"><span data-stu-id="832cc-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF\_NOTRUNCATE**</span></span> 

<span data-ttu-id="832cc-124">Especifica que la cadena devuelta no se debe truncar.</span><span class="sxs-lookup"><span data-stu-id="832cc-124">Specifies that the return string should not be truncated.</span></span> <span data-ttu-id="832cc-125">En su lugar, devuelva un valor de error y el tamaño necesario para la cadena completa.</span><span class="sxs-lookup"><span data-stu-id="832cc-125">Instead, return an error value and the required size for the complete string.</span></span>

 <span data-ttu-id="832cc-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**\_comprobar ASSOCF**</span><span class="sxs-lookup"><span data-stu-id="832cc-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF\_VERIFY**</span></span> 

<span data-ttu-id="832cc-127">Indica a los métodos de [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que comprueben que los datos son precisos.</span><span class="sxs-lookup"><span data-stu-id="832cc-127">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to verify that data is accurate.</span></span> <span data-ttu-id="832cc-128">Esta configuración permite a los métodos de **IQueryAssociations** leer datos del disco duro del usuario para su comprobación.</span><span class="sxs-lookup"><span data-stu-id="832cc-128">This setting allows **IQueryAssociations** methods to read data from the user's hard disk for verification.</span></span> <span data-ttu-id="832cc-129">Por ejemplo, pueden comprobar el nombre descriptivo en el registro con el que se almacena en el archivo. exe.</span><span class="sxs-lookup"><span data-stu-id="832cc-129">For example, they can check the friendly name in the registry against the one stored in the .exe file.</span></span> <span data-ttu-id="832cc-130">Al establecer esta marca, normalmente se reduce la eficacia del método.</span><span class="sxs-lookup"><span data-stu-id="832cc-130">Setting this flag typically reduces the efficiency of the method.</span></span>

 <span data-ttu-id="832cc-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL**</span><span class="sxs-lookup"><span data-stu-id="832cc-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF\_REMAPRUNDLL**</span></span> 

<span data-ttu-id="832cc-132">Indica a los métodos de [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que omitan Rundll.exe y devuelvan información sobre su destino.</span><span class="sxs-lookup"><span data-stu-id="832cc-132">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to ignore Rundll.exe and return information about its target.</span></span> <span data-ttu-id="832cc-133">Normalmente, los métodos **IQueryAssociations** devuelven información sobre el primer archivo. exe o. dll en una cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="832cc-133">Typically **IQueryAssociations** methods return information about the first .exe or .dll in a command string.</span></span> <span data-ttu-id="832cc-134">Si un comando usa Rundll.exe, al establecer esta marca, se indica al método que omita Rundll.exe y devuelva información sobre su destino.</span><span class="sxs-lookup"><span data-stu-id="832cc-134">If a command uses Rundll.exe, setting this flag tells the method to ignore Rundll.exe and return information about its target.</span></span>

 <span data-ttu-id="832cc-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOfixups**</span><span class="sxs-lookup"><span data-stu-id="832cc-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF\_NOFIXUPS**</span></span> 

<span data-ttu-id="832cc-136">Indica a los métodos de [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que no corrijan los errores en el registro, como el nombre descriptivo de una función que no coincide con el encontrado en el archivo. exe.</span><span class="sxs-lookup"><span data-stu-id="832cc-136">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods not to fix errors in the registry, such as the friendly name of a function not matching the one found in the .exe file.</span></span>

 <span data-ttu-id="832cc-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS**</span><span class="sxs-lookup"><span data-stu-id="832cc-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF\_IGNOREBASECLASS**</span></span> 

<span data-ttu-id="832cc-138">Especifica que el valor de BaseClass debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="832cc-138">Specifies that the BaseClass value should be ignored.</span></span>

 <span data-ttu-id="832cc-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ init \_ IGNOREUNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="832cc-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF\_INIT\_IGNOREUNKNOWN**</span></span> 

<span data-ttu-id="832cc-140">**Introducido en Windows 7**.</span><span class="sxs-lookup"><span data-stu-id="832cc-140">**Introduced in Windows 7**.</span></span> <span data-ttu-id="832cc-141">Especifica que se debe omitir el ProgID "Unknown"; en su lugar, produce un error.</span><span class="sxs-lookup"><span data-stu-id="832cc-141">Specifies that the "Unknown" ProgID should be ignored; instead, fail.</span></span>

 <span data-ttu-id="832cc-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF \_ init \_ fixed \_ ProgID**</span><span class="sxs-lookup"><span data-stu-id="832cc-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF\_INIT\_FIXED\_PROGID**</span></span> 

<span data-ttu-id="832cc-143">**Introducido en Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="832cc-143">**Introduced in Windows 8**.</span></span> <span data-ttu-id="832cc-144">Especifica que el ProgID proporcionado debe asignarse utilizando los valores predeterminados del sistema, en lugar de los valores predeterminados del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="832cc-144">Specifies that the supplied ProgID should be mapped using the system defaults, rather than the current user defaults.</span></span>

 <span data-ttu-id="832cc-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ es \_ Protocol**</span><span class="sxs-lookup"><span data-stu-id="832cc-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF\_IS\_PROTOCOL**</span></span> 

<span data-ttu-id="832cc-146">**Introducido en Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="832cc-146">**Introduced in Windows 8**.</span></span> <span data-ttu-id="832cc-147">Especifica que el valor es un protocolo y debe asignarse con los valores predeterminados del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="832cc-147">Specifies that the value is a protocol, and should be mapped using the current user defaults.</span></span>

 <span data-ttu-id="832cc-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ init \_ para el \_ archivo**</span><span class="sxs-lookup"><span data-stu-id="832cc-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF\_INIT\_FOR\_FILE**</span></span> 

<span data-ttu-id="832cc-149">**Introducido en Windows 8.1**.</span><span class="sxs-lookup"><span data-stu-id="832cc-149">**Introduced in Windows 8.1**.</span></span> <span data-ttu-id="832cc-150">Especifica que el ProgID corresponde a una asociación basada en la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="832cc-150">Specifies that the ProgID corresponds with a file extension based association.</span></span> <span data-ttu-id="832cc-151">Úselo junto con **ASSOCF \_ init \_ fixed \_ ProgID**.</span><span class="sxs-lookup"><span data-stu-id="832cc-151">Use together with **ASSOCF\_INIT\_FIXED\_PROGID**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="832cc-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="832cc-152">Requirements</span></span>



| <span data-ttu-id="832cc-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="832cc-153">Requirement</span></span> | <span data-ttu-id="832cc-154">Value</span><span class="sxs-lookup"><span data-stu-id="832cc-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="832cc-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="832cc-155">Minimum supported client</span></span> | <span data-ttu-id="832cc-156">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="832cc-156">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span>               |
| <span data-ttu-id="832cc-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="832cc-157">Minimum supported server</span></span> | <span data-ttu-id="832cc-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="832cc-158">Windows 2000 Server \[desktop apps only\]</span></span>                                 |
| <span data-ttu-id="832cc-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="832cc-159">Header</span></span>                   |  <span data-ttu-id="832cc-160">Shlwapi. h</span><span class="sxs-lookup"><span data-stu-id="832cc-160">Shlwapi.h</span></span>  |



## <a name="see-also"></a><span data-ttu-id="832cc-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="832cc-161">See also</span></span>

 <span data-ttu-id="832cc-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span><span class="sxs-lookup"><span data-stu-id="832cc-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span></span> 

 

 

<span data-ttu-id="832cc-163">© 2017 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="832cc-163">© 2017 Microsoft.</span></span> <span data-ttu-id="832cc-164">Todos los derechos reservados.</span><span class="sxs-lookup"><span data-stu-id="832cc-164">All rights reserved.</span></span>
