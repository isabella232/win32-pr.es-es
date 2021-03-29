---
title: Recurso VERSIONINFO
description: Define un recurso de información de versión. El recurso contiene información sobre el archivo como su número de versión, su sistema operativo previsto y su nombre de archivo original. El recurso está diseñado para usarse con las funciones de información de versión.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Menús de recursos VERSIONINFO y otros recursos
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "104359501"
---
# <a name="versioninfo-resource"></a><span data-ttu-id="2e20b-106">Recurso VERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="2e20b-106">VERSIONINFO resource</span></span>

<span data-ttu-id="2e20b-107">Define un recurso de información de versión.</span><span class="sxs-lookup"><span data-stu-id="2e20b-107">Defines a version-information resource.</span></span> <span data-ttu-id="2e20b-108">El recurso contiene información sobre el archivo como su número de versión, su sistema operativo previsto y su nombre de archivo original.</span><span class="sxs-lookup"><span data-stu-id="2e20b-108">The resource contains such information about the file as its version number, its intended operating system, and its original filename.</span></span> <span data-ttu-id="2e20b-109">El recurso está diseñado para usarse con las funciones de [información de versión](./version-information.md) .</span><span class="sxs-lookup"><span data-stu-id="2e20b-109">The resource is intended to be used with the [Version Information](./version-information.md) functions.</span></span>

<span data-ttu-id="2e20b-110">Hay dos maneras de dar formato a una instrucción **versionInfo** :</span><span class="sxs-lookup"><span data-stu-id="2e20b-110">There are two ways to format a **VERSIONINFO** statement:</span></span>

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

<span data-ttu-id="2e20b-111">\- o -</span><span class="sxs-lookup"><span data-stu-id="2e20b-111">\- or -</span></span>

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="2e20b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e20b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e20b-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span><span class="sxs-lookup"><span data-stu-id="2e20b-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span></span>
</dt> <dd>

<span data-ttu-id="2e20b-114">Identificador de recurso de información de versión.</span><span class="sxs-lookup"><span data-stu-id="2e20b-114">Version-information resource identifier.</span></span> <span data-ttu-id="2e20b-115">Este valor debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="2e20b-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="2e20b-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*Fixed-info*</span><span class="sxs-lookup"><span data-stu-id="2e20b-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*fixed-info*</span></span>
</dt> <dd>

<span data-ttu-id="2e20b-117">Información de versión, como la versión del archivo y el sistema operativo previsto.</span><span class="sxs-lookup"><span data-stu-id="2e20b-117">Version information, such as the file version and the intended operating system.</span></span> <span data-ttu-id="2e20b-118">Este parámetro consta de las siguientes instrucciones.</span><span class="sxs-lookup"><span data-stu-id="2e20b-118">This parameter consists of the following statements.</span></span>



| <span data-ttu-id="2e20b-119">.</span><span class="sxs-lookup"><span data-stu-id="2e20b-119">Statement</span></span>                         | <span data-ttu-id="2e20b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e20b-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e20b-121"> *Versión* FILEVERSION</span><span class="sxs-lookup"><span data-stu-id="2e20b-121">**FILEVERSION** *version*</span></span>         | <span data-ttu-id="2e20b-122">Número de versión binaria del archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-122">Binary version number for the file.</span></span> <span data-ttu-id="2e20b-123">La *versión* consta de enteros de 2 32 bits, definidos por enteros de 4 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2e20b-123">The *version* consists of two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="2e20b-124">Por ejemplo, "FILEVERSION 3, 10, 0, 61" se traduce en dos palabras dobles: 0x0003000a y 0x0000003d, en ese orden.</span><span class="sxs-lookup"><span data-stu-id="2e20b-124">For example, "FILEVERSION 3,10,0,61" is translated into two doublewords: 0x0003000a and 0x0000003d, in that order.</span></span> <span data-ttu-id="2e20b-125">Por lo tanto, si la *versión* está definida por los valores **DWORD** *DW1* y *Dw2*, deben aparecer en la instrucción **FILEVERSION** de la siguiente manera: `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` .</span><span class="sxs-lookup"><span data-stu-id="2e20b-125">Therefore, if *version* is defined by the **DWORD** values *dw1* and *dw2*, they need to appear in the **FILEVERSION** statement as follows: `HIWORD(dw1)`, `LOWORD(dw1)`, `HIWORD(dw2)`, `LOWORD(dw2)`.</span></span> |
| <span data-ttu-id="2e20b-126"> *Versión* de PRODUCTVERSION</span><span class="sxs-lookup"><span data-stu-id="2e20b-126">**PRODUCTVERSION** *version*</span></span>      | <span data-ttu-id="2e20b-127">Número de versión binaria del producto con el que se distribuye el archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-127">Binary version number for the product with which the file is distributed.</span></span> <span data-ttu-id="2e20b-128">El parámetro *version* es un entero de 2 32 bits, definido por enteros de 4 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2e20b-128">The *version* parameter is two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="2e20b-129">Para obtener más información acerca de la versión, consulte la **Descripción de la** versión de la *versión*.</span><span class="sxs-lookup"><span data-stu-id="2e20b-129">For more information about *version*, see the **FILEVERSION** description.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="2e20b-130">**FILEFLAGSMASK** *FILEFLAGSMASK*</span><span class="sxs-lookup"><span data-stu-id="2e20b-130">**FILEFLAGSMASK** *fileflagsmask*</span></span> | <span data-ttu-id="2e20b-131">Indica qué bits de la instrucción **FILEFLAGS** son válidos.</span><span class="sxs-lookup"><span data-stu-id="2e20b-131">Indicates which bits in the **FILEFLAGS** statement are valid.</span></span> <span data-ttu-id="2e20b-132">En Windows de 16 bits, este valor es 0x3F.</span><span class="sxs-lookup"><span data-stu-id="2e20b-132">For 16-bit Windows, this value is 0x3f.</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2e20b-133">**FILEFLAGS** *FILEFLAGS*</span><span class="sxs-lookup"><span data-stu-id="2e20b-133">**FILEFLAGS** *fileflags*</span></span>         | <span data-ttu-id="2e20b-134">Atributos del archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-134">Attributes of the file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2e20b-135"> *Archivos* de archivos</span><span class="sxs-lookup"><span data-stu-id="2e20b-135">**FILEOS** *fileos*</span></span>               | <span data-ttu-id="2e20b-136">Sistema operativo para el que se diseñó este archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-136">Operating system for which this file was designed.</span></span> <span data-ttu-id="2e20b-137">El parámetro *Fileos* puede ser uno de los valores del sistema operativo que se indican en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2e20b-137">The *fileos* parameter can be one of the operating system values given in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="2e20b-138"> *Filetype* filetype</span><span class="sxs-lookup"><span data-stu-id="2e20b-138">**FILETYPE** *filetype*</span></span>           | <span data-ttu-id="2e20b-139">Tipo general de archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-139">General type of file.</span></span> <span data-ttu-id="2e20b-140">El parámetro *filetype* puede ser uno de los valores de tipo de archivo que se muestran en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2e20b-140">The *filetype* parameter can be one of the file type values listed in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="2e20b-141">Subtipo **FILESUBTYPE** </span><span class="sxs-lookup"><span data-stu-id="2e20b-141">**FILESUBTYPE** *subtype*</span></span>         | <span data-ttu-id="2e20b-142">Función del archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-142">Function of the file.</span></span> <span data-ttu-id="2e20b-143">El parámetro *SubType* es cero a menos que el parámetro *filetype* de la instrucción **FILETYPE** sea VFT \_ drv, VFT \_ Font o VFT \_ vxd.</span><span class="sxs-lookup"><span data-stu-id="2e20b-143">The *subtype* parameter is zero unless the *filetype* parameter in the **FILETYPE** statement is VFT\_DRV, VFT\_FONT, or VFT\_VXD.</span></span> <span data-ttu-id="2e20b-144">Para obtener una lista de valores de subtipo de archivo, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2e20b-144">For a list of file subtype values, see the Remarks section.</span></span>                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="2e20b-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*Block-Statement*</span><span class="sxs-lookup"><span data-stu-id="2e20b-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block-statement*</span></span>
</dt> <dd>

<span data-ttu-id="2e20b-146">Especifica uno o más bloques de información de versión.</span><span class="sxs-lookup"><span data-stu-id="2e20b-146">Specifies one or more version-information blocks.</span></span> <span data-ttu-id="2e20b-147">Un bloque puede contener información de cadena o información de variables.</span><span class="sxs-lookup"><span data-stu-id="2e20b-147">A block can contain string information or variable information.</span></span> <span data-ttu-id="2e20b-148">Para obtener más información, vea bloque [**StringFileInfo**](stringfileinfo-block.md) o [**bloque VarFileInfo**](varfileinfo-block.md).</span><span class="sxs-lookup"><span data-stu-id="2e20b-148">For more information, see [**StringFileInfo Block**](stringfileinfo-block.md) or [**VarFileInfo Block**](varfileinfo-block.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e20b-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e20b-149">Remarks</span></span>

<span data-ttu-id="2e20b-150">Para usar las constantes especificadas con la instrucción **versionInfo** , debe incluir el archivo de encabezado winver. h o Windows. h en el archivo de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e20b-150">To use the constants specified with the **VERSIONINFO** statement, you must include the Winver.h or Windows.h header file in the resource-definition file.</span></span>

<span data-ttu-id="2e20b-151">En la lista siguiente se describen los parámetros que se usan en la instrucción **versionInfo** :</span><span class="sxs-lookup"><span data-stu-id="2e20b-151">The following list describes the parameters used in the **VERSIONINFO** statement:</span></span>

<dl> <dt>

<span data-ttu-id="2e20b-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*</span><span class="sxs-lookup"><span data-stu-id="2e20b-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*</span></span>
</dt> <dd>

<span data-ttu-id="2e20b-153">Una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2e20b-153">A combination of the following values.</span></span>



| <span data-ttu-id="2e20b-154">Value</span><span class="sxs-lookup"><span data-stu-id="2e20b-154">Value</span></span>                      | <span data-ttu-id="2e20b-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e20b-155">Description</span></span>                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e20b-156">**depuración de VS \_ FF \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-156">**VS\_FF\_DEBUG**</span></span>          | <span data-ttu-id="2e20b-157">El archivo contiene información de depuración o se compila con las características de depuración habilitadas.</span><span class="sxs-lookup"><span data-stu-id="2e20b-157">File contains debugging information or is compiled with debugging features enabled.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="2e20b-158">**VS \_ FF \_ revisado**</span><span class="sxs-lookup"><span data-stu-id="2e20b-158">**VS\_FF\_PATCHED**</span></span>        | <span data-ttu-id="2e20b-159">El archivo se ha modificado y no es idéntico al archivo de envío original del mismo número de versión.</span><span class="sxs-lookup"><span data-stu-id="2e20b-159">File has been modified and is not identical to the original shipping file of the same version number.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="2e20b-160">**\_ \_ versión preliminar de vs FF**</span><span class="sxs-lookup"><span data-stu-id="2e20b-160">**VS\_FF\_PRERELEASE**</span></span>     | <span data-ttu-id="2e20b-161">El archivo es una versión de desarrollo, no un producto publicado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2e20b-161">File is a development version, not a commercially released product.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="2e20b-162">**VS \_ FF \_ PRIVATEBUILD**</span><span class="sxs-lookup"><span data-stu-id="2e20b-162">**VS\_FF\_PRIVATEBUILD**</span></span>   | <span data-ttu-id="2e20b-163">El archivo no se compiló con procedimientos estándar de versión.</span><span class="sxs-lookup"><span data-stu-id="2e20b-163">File was not built using standard release procedures.</span></span> <span data-ttu-id="2e20b-164">Si se especifica este valor, el [**bloque StringFileInfo**](stringfileinfo-block.md) debe contener una cadena **PrivateBuild** .</span><span class="sxs-lookup"><span data-stu-id="2e20b-164">If this value is given, the [**StringFileInfo block**](stringfileinfo-block.md) must contain a **PrivateBuild** string.</span></span>                                                                                              |
| <span data-ttu-id="2e20b-165">**VS \_ FF \_ SPECIALBUILD**</span><span class="sxs-lookup"><span data-stu-id="2e20b-165">**VS\_FF\_SPECIALBUILD**</span></span>   | <span data-ttu-id="2e20b-166">El archivo fue creado por la empresa original mediante procedimientos estándar de versión, pero es una variación del archivo estándar del mismo número de versión.</span><span class="sxs-lookup"><span data-stu-id="2e20b-166">File was built by the original company using standard release procedures but is a variation of the standard file of the same version number.</span></span> <span data-ttu-id="2e20b-167">Si se especifica este valor, el bloque de [bloque **StringFileInfo**](stringfileinfo-block.md) debe contener una cadena **SpecialBuild** .</span><span class="sxs-lookup"><span data-stu-id="2e20b-167">If this value is given, the [**StringFileInfo** block](stringfileinfo-block.md) block must contain a **SpecialBuild** string.</span></span> |
| <span data-ttu-id="2e20b-168">**VS \_ FFI \_ FILEFLAGSMASK**</span><span class="sxs-lookup"><span data-stu-id="2e20b-168">**VS\_FFI\_FILEFLAGSMASK**</span></span> | <span data-ttu-id="2e20b-169">Combinación de todos los valores anteriores.</span><span class="sxs-lookup"><span data-stu-id="2e20b-169">A combination of all the preceding values.</span></span>                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="2e20b-170"><span id="fileos"></span><span id="FILEOS"></span>*archivos*</span><span class="sxs-lookup"><span data-stu-id="2e20b-170"><span id="fileos"></span><span id="FILEOS"></span>*fileos*</span></span>
</dt> <dd>

<span data-ttu-id="2e20b-171">Uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="2e20b-171">One of the following values.</span></span>



| <span data-ttu-id="2e20b-172">Valor</span><span class="sxs-lookup"><span data-stu-id="2e20b-172">Value</span></span>                   | <span data-ttu-id="2e20b-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e20b-173">Description</span></span>                                                      |
|-------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2e20b-174">**VOS \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="2e20b-174">**VOS\_UNKNOWN**</span></span>        | <span data-ttu-id="2e20b-175">El sistema operativo para el que se diseñó el archivo es desconocido.</span><span class="sxs-lookup"><span data-stu-id="2e20b-175">The operating system for which the file was designed is unknown.</span></span> |
| <span data-ttu-id="2e20b-176">**VOS \_ dos**</span><span class="sxs-lookup"><span data-stu-id="2e20b-176">**VOS\_DOS**</span></span>            | <span data-ttu-id="2e20b-177">El archivo se diseñó para MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="2e20b-177">File was designed for MS-DOS.</span></span>                                    |
| <span data-ttu-id="2e20b-178">**VOS \_ NT**</span><span class="sxs-lookup"><span data-stu-id="2e20b-178">**VOS\_NT**</span></span>             | <span data-ttu-id="2e20b-179">El archivo se diseñó para Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2e20b-179">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="2e20b-180">**VOS \_ \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="2e20b-180">**VOS\_\_WINDOWS16**</span></span>    | <span data-ttu-id="2e20b-181">El archivo se diseñó para Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2e20b-181">File was designed for 16-bit Windows.</span></span>                            |
| <span data-ttu-id="2e20b-182">**VOS \_ \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="2e20b-182">**VOS\_\_WINDOWS32**</span></span>    | <span data-ttu-id="2e20b-183">El archivo se diseñó para Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2e20b-183">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="2e20b-184">**VOS \_ dos \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="2e20b-184">**VOS\_DOS\_WINDOWS16**</span></span> | <span data-ttu-id="2e20b-185">El archivo se diseñó para Windows de 16 bits que se ejecuta con MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="2e20b-185">File was designed for 16-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="2e20b-186">**VOS \_ dos \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="2e20b-186">**VOS\_DOS\_WINDOWS32**</span></span> | <span data-ttu-id="2e20b-187">El archivo se diseñó para Windows de 32 bits que se ejecuta con MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="2e20b-187">File was designed for 32-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="2e20b-188">**VOS \_ NT \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="2e20b-188">**VOS\_NT\_WINDOWS32**</span></span>  | <span data-ttu-id="2e20b-189">El archivo se diseñó para Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2e20b-189">File was designed for 32-bit Windows.</span></span>                            |



 

<span data-ttu-id="2e20b-190">Los valores 0x00002L, 0x00003L, 0x20000L y 0x30000L están reservados.</span><span class="sxs-lookup"><span data-stu-id="2e20b-190">The values 0x00002L, 0x00003L, 0x20000L and 0x30000L are reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2e20b-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span><span class="sxs-lookup"><span data-stu-id="2e20b-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span></span>
</dt> <dd>

<span data-ttu-id="2e20b-192">Uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="2e20b-192">One of the following values.</span></span>



| <span data-ttu-id="2e20b-193">Valor</span><span class="sxs-lookup"><span data-stu-id="2e20b-193">Value</span></span>                | <span data-ttu-id="2e20b-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e20b-194">Description</span></span>                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e20b-195">**VFT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="2e20b-195">**VFT\_UNKNOWN**</span></span>     | <span data-ttu-id="2e20b-196">No se conoce el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-196">File type is unknown.</span></span>                                                                                                       |
| <span data-ttu-id="2e20b-197">**\_aplicación VFT**</span><span class="sxs-lookup"><span data-stu-id="2e20b-197">**VFT\_APP**</span></span>         | <span data-ttu-id="2e20b-198">El archivo contiene una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2e20b-198">File contains an application.</span></span>                                                                                               |
| <span data-ttu-id="2e20b-199">**\_dll VFT**</span><span class="sxs-lookup"><span data-stu-id="2e20b-199">**VFT\_DLL**</span></span>         | <span data-ttu-id="2e20b-200">El archivo contiene una biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="2e20b-200">File contains a dynamic-link library (DLL).</span></span>                                                                                 |
| <span data-ttu-id="2e20b-201">**VFT \_ DRV**</span><span class="sxs-lookup"><span data-stu-id="2e20b-201">**VFT\_DRV**</span></span>         | <span data-ttu-id="2e20b-202">El archivo contiene un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-202">File contains a device driver.</span></span> <span data-ttu-id="2e20b-203">Si *filetype* es **VFT \_ DRV**, *SubType* contiene una descripción más específica del controlador.</span><span class="sxs-lookup"><span data-stu-id="2e20b-203">If *filetype* is **VFT\_DRV**, *subtype* contains a more specific description of the driver.</span></span> |
| <span data-ttu-id="2e20b-204">**\_fuente VFT**</span><span class="sxs-lookup"><span data-stu-id="2e20b-204">**VFT\_FONT**</span></span>        | <span data-ttu-id="2e20b-205">El archivo contiene una fuente.</span><span class="sxs-lookup"><span data-stu-id="2e20b-205">File contains a font.</span></span> <span data-ttu-id="2e20b-206">Si *filetype* es VFT \_ Font, *SubType* contiene una descripción más específica de la fuente.</span><span class="sxs-lookup"><span data-stu-id="2e20b-206">If *filetype* is VFT\_FONT, *subtype* contains a more specific description of the font.</span></span>               |
| <span data-ttu-id="2e20b-207">**VXD de VFT \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-207">**VFT\_VXD**</span></span>         | <span data-ttu-id="2e20b-208">El archivo contiene un dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="2e20b-208">File contains a virtual device.</span></span>                                                                                             |
| <span data-ttu-id="2e20b-209">**\_biblioteca estática \_ VFT**</span><span class="sxs-lookup"><span data-stu-id="2e20b-209">**VFT\_STATIC\_LIB**</span></span> | <span data-ttu-id="2e20b-210">El archivo contiene una biblioteca de vínculos estáticos.</span><span class="sxs-lookup"><span data-stu-id="2e20b-210">File contains a static-link library.</span></span>                                                                                        |



 

<span data-ttu-id="2e20b-211">Todos los demás valores están reservados para su uso por parte de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2e20b-211">All other values are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="2e20b-212"><span id="subtype"></span><span id="SUBTYPE"></span>*subtipo*</span><span class="sxs-lookup"><span data-stu-id="2e20b-212"><span id="subtype"></span><span id="SUBTYPE"></span>*subtype*</span></span>
</dt> <dd>

<span data-ttu-id="2e20b-213">Información adicional sobre el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-213">Additional information about the file type.</span></span>

<span data-ttu-id="2e20b-214">Si *filetype* especifica **VFT \_ DRV**, este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2e20b-214">If *filetype* specifies **VFT\_DRV**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="2e20b-215">Value</span><span class="sxs-lookup"><span data-stu-id="2e20b-215">Value</span></span>                             | <span data-ttu-id="2e20b-216">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e20b-216">Description</span></span>                               |
|-----------------------------------|-------------------------------------------|
| <span data-ttu-id="2e20b-217">**VFT2 \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="2e20b-217">**VFT2\_UNKNOWN**</span></span>                 | <span data-ttu-id="2e20b-218">No se conoce el tipo de controlador.</span><span class="sxs-lookup"><span data-stu-id="2e20b-218">Driver type is unknown.</span></span>                   |
| <span data-ttu-id="2e20b-219">**VFT2 \_ DRV \_ COMM**</span><span class="sxs-lookup"><span data-stu-id="2e20b-219">**VFT2\_DRV\_COMM**</span></span>               | <span data-ttu-id="2e20b-220">El archivo contiene un controlador de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="2e20b-220">File contains a communications driver.</span></span>    |
| <span data-ttu-id="2e20b-221">**\_Impresora VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-221">**VFT2\_DRV\_PRINTER**</span></span>            | <span data-ttu-id="2e20b-222">El archivo contiene un controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="2e20b-222">File contains a printer driver.</span></span>           |
| <span data-ttu-id="2e20b-223">**\_Teclado VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-223">**VFT2\_DRV\_KEYBOARD**</span></span>           | <span data-ttu-id="2e20b-224">El archivo contiene un controlador de teclado.</span><span class="sxs-lookup"><span data-stu-id="2e20b-224">File contains a keyboard driver.</span></span>          |
| <span data-ttu-id="2e20b-225">**Idioma de VFT2 \_ DRV \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-225">**VFT2\_DRV\_LANGUAGE**</span></span>           | <span data-ttu-id="2e20b-226">El archivo contiene un controlador de idioma.</span><span class="sxs-lookup"><span data-stu-id="2e20b-226">File contains a language driver.</span></span>          |
| <span data-ttu-id="2e20b-227">**Pantalla de VFT2 \_ DRV \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-227">**VFT2\_DRV\_DISPLAY**</span></span>            | <span data-ttu-id="2e20b-228">El archivo contiene un controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2e20b-228">File contains a display driver.</span></span>           |
| <span data-ttu-id="2e20b-229">**\_Mouse VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-229">**VFT2\_DRV\_MOUSE**</span></span>              | <span data-ttu-id="2e20b-230">El archivo contiene un controlador de mouse.</span><span class="sxs-lookup"><span data-stu-id="2e20b-230">File contains a mouse driver.</span></span>             |
| <span data-ttu-id="2e20b-231">**\_Red VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-231">**VFT2\_DRV\_NETWORK**</span></span>            | <span data-ttu-id="2e20b-232">El archivo contiene un controlador de red.</span><span class="sxs-lookup"><span data-stu-id="2e20b-232">File contains a network driver.</span></span>           |
| <span data-ttu-id="2e20b-233">**\_Sistema VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-233">**VFT2\_DRV\_SYSTEM**</span></span>             | <span data-ttu-id="2e20b-234">El archivo contiene un controlador del sistema.</span><span class="sxs-lookup"><span data-stu-id="2e20b-234">File contains a system driver.</span></span>            |
| <span data-ttu-id="2e20b-235">**VFT2 \_ DRV \_ instalable**</span><span class="sxs-lookup"><span data-stu-id="2e20b-235">**VFT2\_DRV\_INSTALLABLE**</span></span>        | <span data-ttu-id="2e20b-236">El archivo contiene un controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="2e20b-236">File contains an installable driver.</span></span>      |
| <span data-ttu-id="2e20b-237">**\_Sonido VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-237">**VFT2\_DRV\_SOUND**</span></span>              | <span data-ttu-id="2e20b-238">El archivo contiene un controlador de sonido.</span><span class="sxs-lookup"><span data-stu-id="2e20b-238">File contains a sound driver.</span></span>             |
| <span data-ttu-id="2e20b-239">**\_Impresora con \_ versión VFT2 \_ DRV**</span><span class="sxs-lookup"><span data-stu-id="2e20b-239">**VFT2\_DRV\_VERSIONED\_PRINTER**</span></span> | <span data-ttu-id="2e20b-240">El archivo contiene un controlador de impresora con versión.</span><span class="sxs-lookup"><span data-stu-id="2e20b-240">File contains a versioned printer driver.</span></span> |



 

<span data-ttu-id="2e20b-241">Si *filetype* especifica **la \_ fuente VFT**, este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2e20b-241">If *filetype* specifies **VFT\_FONT**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="2e20b-242">Value</span><span class="sxs-lookup"><span data-stu-id="2e20b-242">Value</span></span>                    | <span data-ttu-id="2e20b-243">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e20b-243">Description</span></span>                    |
|--------------------------|--------------------------------|
| <span data-ttu-id="2e20b-244">**VFT2 \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="2e20b-244">**VFT2\_UNKNOWN**</span></span>        | <span data-ttu-id="2e20b-245">Tipo de fuente desconocido.</span><span class="sxs-lookup"><span data-stu-id="2e20b-245">Font type is unknown.</span></span>          |
| <span data-ttu-id="2e20b-246">**\_Trama de fuente VFT2 \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-246">**VFT2\_FONT\_RASTER**</span></span>   | <span data-ttu-id="2e20b-247">El archivo contiene una fuente de trama.</span><span class="sxs-lookup"><span data-stu-id="2e20b-247">File contains a raster font.</span></span>   |
| <span data-ttu-id="2e20b-248">**\_Vector de fuente VFT2 \_**</span><span class="sxs-lookup"><span data-stu-id="2e20b-248">**VFT2\_FONT\_VECTOR**</span></span>   | <span data-ttu-id="2e20b-249">El archivo contiene una fuente de vector.</span><span class="sxs-lookup"><span data-stu-id="2e20b-249">File contains a vector font.</span></span>   |
| <span data-ttu-id="2e20b-250">**VFT2 \_ fuente \_ TrueType**</span><span class="sxs-lookup"><span data-stu-id="2e20b-250">**VFT2\_FONT\_TRUETYPE**</span></span> | <span data-ttu-id="2e20b-251">El archivo contiene una fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="2e20b-251">File contains a TrueType font.</span></span> |



 

<span data-ttu-id="2e20b-252">Si *filetype* especifica VFT \_ VXD, este parámetro debe ser el identificador del dispositivo virtual incluido en el bloque de control del dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="2e20b-252">If *filetype* specifies VFT\_VXD, this parameter must be the virtual-device identifier included in the virtual-device control block.</span></span>

<span data-ttu-id="2e20b-253">Todos los valores de *subtipo* que no se enumeran aquí están reservados para su uso por parte de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2e20b-253">All *subtype* values not listed here are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="2e20b-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*ididioma*</span><span class="sxs-lookup"><span data-stu-id="2e20b-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="2e20b-255">Uno de los siguientes códigos de idioma.</span><span class="sxs-lookup"><span data-stu-id="2e20b-255">One of the following language codes.</span></span>



| <span data-ttu-id="2e20b-256">Código</span><span class="sxs-lookup"><span data-stu-id="2e20b-256">Code</span></span>   | <span data-ttu-id="2e20b-257">Idioma</span><span class="sxs-lookup"><span data-stu-id="2e20b-257">Language</span></span>            | <span data-ttu-id="2e20b-258">Código</span><span class="sxs-lookup"><span data-stu-id="2e20b-258">Code</span></span>   | <span data-ttu-id="2e20b-259">Idioma</span><span class="sxs-lookup"><span data-stu-id="2e20b-259">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="2e20b-260">0x0401</span><span class="sxs-lookup"><span data-stu-id="2e20b-260">0x0401</span></span> | <span data-ttu-id="2e20b-261">Árabe</span><span class="sxs-lookup"><span data-stu-id="2e20b-261">Arabic</span></span>              | <span data-ttu-id="2e20b-262">0x0415</span><span class="sxs-lookup"><span data-stu-id="2e20b-262">0x0415</span></span> | <span data-ttu-id="2e20b-263">Polaco</span><span class="sxs-lookup"><span data-stu-id="2e20b-263">Polish</span></span>                    |
| <span data-ttu-id="2e20b-264">0x0402</span><span class="sxs-lookup"><span data-stu-id="2e20b-264">0x0402</span></span> | <span data-ttu-id="2e20b-265">Búlgaro</span><span class="sxs-lookup"><span data-stu-id="2e20b-265">Bulgarian</span></span>           | <span data-ttu-id="2e20b-266">0x0416</span><span class="sxs-lookup"><span data-stu-id="2e20b-266">0x0416</span></span> | <span data-ttu-id="2e20b-267">Portugués (Brasil)</span><span class="sxs-lookup"><span data-stu-id="2e20b-267">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="2e20b-268">0x0403</span><span class="sxs-lookup"><span data-stu-id="2e20b-268">0x0403</span></span> | <span data-ttu-id="2e20b-269">Catalán</span><span class="sxs-lookup"><span data-stu-id="2e20b-269">Catalan</span></span>             | <span data-ttu-id="2e20b-270">0x0417</span><span class="sxs-lookup"><span data-stu-id="2e20b-270">0x0417</span></span> | <span data-ttu-id="2e20b-271">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="2e20b-271">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="2e20b-272">0x0404</span><span class="sxs-lookup"><span data-stu-id="2e20b-272">0x0404</span></span> | <span data-ttu-id="2e20b-273">Chino tradicional</span><span class="sxs-lookup"><span data-stu-id="2e20b-273">Traditional Chinese</span></span> | <span data-ttu-id="2e20b-274">0x0418</span><span class="sxs-lookup"><span data-stu-id="2e20b-274">0x0418</span></span> | <span data-ttu-id="2e20b-275">Rumano</span><span class="sxs-lookup"><span data-stu-id="2e20b-275">Romanian</span></span>                  |
| <span data-ttu-id="2e20b-276">0x0405</span><span class="sxs-lookup"><span data-stu-id="2e20b-276">0x0405</span></span> | <span data-ttu-id="2e20b-277">Checo</span><span class="sxs-lookup"><span data-stu-id="2e20b-277">Czech</span></span>               | <span data-ttu-id="2e20b-278">0x0419</span><span class="sxs-lookup"><span data-stu-id="2e20b-278">0x0419</span></span> | <span data-ttu-id="2e20b-279">Ruso</span><span class="sxs-lookup"><span data-stu-id="2e20b-279">Russian</span></span>                   |
| <span data-ttu-id="2e20b-280">0x0406</span><span class="sxs-lookup"><span data-stu-id="2e20b-280">0x0406</span></span> | <span data-ttu-id="2e20b-281">Danés</span><span class="sxs-lookup"><span data-stu-id="2e20b-281">Danish</span></span>              | <span data-ttu-id="2e20b-282">0x041A</span><span class="sxs-lookup"><span data-stu-id="2e20b-282">0x041A</span></span> | <span data-ttu-id="2e20b-283">Croato-Serbian (Latín)</span><span class="sxs-lookup"><span data-stu-id="2e20b-283">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="2e20b-284">0x0407</span><span class="sxs-lookup"><span data-stu-id="2e20b-284">0x0407</span></span> | <span data-ttu-id="2e20b-285">Alemán</span><span class="sxs-lookup"><span data-stu-id="2e20b-285">German</span></span>              | <span data-ttu-id="2e20b-286">0x041B</span><span class="sxs-lookup"><span data-stu-id="2e20b-286">0x041B</span></span> | <span data-ttu-id="2e20b-287">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="2e20b-287">Slovak</span></span>                    |
| <span data-ttu-id="2e20b-288">0x0408</span><span class="sxs-lookup"><span data-stu-id="2e20b-288">0x0408</span></span> | <span data-ttu-id="2e20b-289">Griego</span><span class="sxs-lookup"><span data-stu-id="2e20b-289">Greek</span></span>               | <span data-ttu-id="2e20b-290">0x041C</span><span class="sxs-lookup"><span data-stu-id="2e20b-290">0x041C</span></span> | <span data-ttu-id="2e20b-291">Albanés</span><span class="sxs-lookup"><span data-stu-id="2e20b-291">Albanian</span></span>                  |
| <span data-ttu-id="2e20b-292">0x0409</span><span class="sxs-lookup"><span data-stu-id="2e20b-292">0x0409</span></span> | <span data-ttu-id="2e20b-293">Inglés de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="2e20b-293">U.S. English</span></span>        | <span data-ttu-id="2e20b-294">0x041D</span><span class="sxs-lookup"><span data-stu-id="2e20b-294">0x041D</span></span> | <span data-ttu-id="2e20b-295">Sueco</span><span class="sxs-lookup"><span data-stu-id="2e20b-295">Swedish</span></span>                   |
| <span data-ttu-id="2e20b-296">0x040A</span><span class="sxs-lookup"><span data-stu-id="2e20b-296">0x040A</span></span> | <span data-ttu-id="2e20b-297">Castilian Español</span><span class="sxs-lookup"><span data-stu-id="2e20b-297">Castilian Spanish</span></span>   | <span data-ttu-id="2e20b-298">0x041E</span><span class="sxs-lookup"><span data-stu-id="2e20b-298">0x041E</span></span> | <span data-ttu-id="2e20b-299">Tailandés</span><span class="sxs-lookup"><span data-stu-id="2e20b-299">Thai</span></span>                      |
| <span data-ttu-id="2e20b-300">0x040B</span><span class="sxs-lookup"><span data-stu-id="2e20b-300">0x040B</span></span> | <span data-ttu-id="2e20b-301">Finés</span><span class="sxs-lookup"><span data-stu-id="2e20b-301">Finnish</span></span>             | <span data-ttu-id="2e20b-302">0x041F</span><span class="sxs-lookup"><span data-stu-id="2e20b-302">0x041F</span></span> | <span data-ttu-id="2e20b-303">Turco</span><span class="sxs-lookup"><span data-stu-id="2e20b-303">Turkish</span></span>                   |
| <span data-ttu-id="2e20b-304">0x040C</span><span class="sxs-lookup"><span data-stu-id="2e20b-304">0x040C</span></span> | <span data-ttu-id="2e20b-305">Francés</span><span class="sxs-lookup"><span data-stu-id="2e20b-305">French</span></span>              | <span data-ttu-id="2e20b-306">0x0420</span><span class="sxs-lookup"><span data-stu-id="2e20b-306">0x0420</span></span> | <span data-ttu-id="2e20b-307">Urdu</span><span class="sxs-lookup"><span data-stu-id="2e20b-307">Urdu</span></span>                      |
| <span data-ttu-id="2e20b-308">0x040D</span><span class="sxs-lookup"><span data-stu-id="2e20b-308">0x040D</span></span> | <span data-ttu-id="2e20b-309">Hebreo</span><span class="sxs-lookup"><span data-stu-id="2e20b-309">Hebrew</span></span>              | <span data-ttu-id="2e20b-310">0x0421</span><span class="sxs-lookup"><span data-stu-id="2e20b-310">0x0421</span></span> | <span data-ttu-id="2e20b-311">Bahasa</span><span class="sxs-lookup"><span data-stu-id="2e20b-311">Bahasa</span></span>                    |
| <span data-ttu-id="2e20b-312">0x040E</span><span class="sxs-lookup"><span data-stu-id="2e20b-312">0x040E</span></span> | <span data-ttu-id="2e20b-313">Húngaro</span><span class="sxs-lookup"><span data-stu-id="2e20b-313">Hungarian</span></span>           | <span data-ttu-id="2e20b-314">0x0804</span><span class="sxs-lookup"><span data-stu-id="2e20b-314">0x0804</span></span> | <span data-ttu-id="2e20b-315">Chino simplificado</span><span class="sxs-lookup"><span data-stu-id="2e20b-315">Simplified Chinese</span></span>        |
| <span data-ttu-id="2e20b-316">0x040F</span><span class="sxs-lookup"><span data-stu-id="2e20b-316">0x040F</span></span> | <span data-ttu-id="2e20b-317">Islandés</span><span class="sxs-lookup"><span data-stu-id="2e20b-317">Icelandic</span></span>           | <span data-ttu-id="2e20b-318">0x0807</span><span class="sxs-lookup"><span data-stu-id="2e20b-318">0x0807</span></span> | <span data-ttu-id="2e20b-319">Alemán suizo</span><span class="sxs-lookup"><span data-stu-id="2e20b-319">Swiss German</span></span>              |
| <span data-ttu-id="2e20b-320">0x0410</span><span class="sxs-lookup"><span data-stu-id="2e20b-320">0x0410</span></span> | <span data-ttu-id="2e20b-321">Italiano</span><span class="sxs-lookup"><span data-stu-id="2e20b-321">Italian</span></span>             | <span data-ttu-id="2e20b-322">0x0809</span><span class="sxs-lookup"><span data-stu-id="2e20b-322">0x0809</span></span> | <span data-ttu-id="2e20b-323">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="2e20b-323">U.K.</span></span> <span data-ttu-id="2e20b-324">Inglés</span><span class="sxs-lookup"><span data-stu-id="2e20b-324">English</span></span>              |
| <span data-ttu-id="2e20b-325">0x0411</span><span class="sxs-lookup"><span data-stu-id="2e20b-325">0x0411</span></span> | <span data-ttu-id="2e20b-326">Japonés</span><span class="sxs-lookup"><span data-stu-id="2e20b-326">Japanese</span></span>            | <span data-ttu-id="2e20b-327">0x080A</span><span class="sxs-lookup"><span data-stu-id="2e20b-327">0x080A</span></span> | <span data-ttu-id="2e20b-328">Español (México)</span><span class="sxs-lookup"><span data-stu-id="2e20b-328">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="2e20b-329">0x0412</span><span class="sxs-lookup"><span data-stu-id="2e20b-329">0x0412</span></span> | <span data-ttu-id="2e20b-330">Coreano</span><span class="sxs-lookup"><span data-stu-id="2e20b-330">Korean</span></span>              | <span data-ttu-id="2e20b-331">0x080C</span><span class="sxs-lookup"><span data-stu-id="2e20b-331">0x080C</span></span> | <span data-ttu-id="2e20b-332">Francés belga</span><span class="sxs-lookup"><span data-stu-id="2e20b-332">Belgian French</span></span>            |
| <span data-ttu-id="2e20b-333">0x0413</span><span class="sxs-lookup"><span data-stu-id="2e20b-333">0x0413</span></span> | <span data-ttu-id="2e20b-334">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="2e20b-334">Dutch</span></span>               | <span data-ttu-id="2e20b-335">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="2e20b-335">0x0C0C</span></span> | <span data-ttu-id="2e20b-336">Francés canadiense</span><span class="sxs-lookup"><span data-stu-id="2e20b-336">Canadian French</span></span>           |
| <span data-ttu-id="2e20b-337">0x0414</span><span class="sxs-lookup"><span data-stu-id="2e20b-337">0x0414</span></span> | <span data-ttu-id="2e20b-338">¿Noruego?</span><span class="sxs-lookup"><span data-stu-id="2e20b-338">Norwegian ?</span></span> <span data-ttu-id="2e20b-339">Bokmal</span><span class="sxs-lookup"><span data-stu-id="2e20b-339">Bokmal</span></span>  | <span data-ttu-id="2e20b-340">0x100C</span><span class="sxs-lookup"><span data-stu-id="2e20b-340">0x100C</span></span> | <span data-ttu-id="2e20b-341">Francés suizo</span><span class="sxs-lookup"><span data-stu-id="2e20b-341">Swiss French</span></span>              |
| <span data-ttu-id="2e20b-342">0x0810</span><span class="sxs-lookup"><span data-stu-id="2e20b-342">0x0810</span></span> | <span data-ttu-id="2e20b-343">Italiano suizo</span><span class="sxs-lookup"><span data-stu-id="2e20b-343">Swiss Italian</span></span>       | <span data-ttu-id="2e20b-344">0x0816</span><span class="sxs-lookup"><span data-stu-id="2e20b-344">0x0816</span></span> | <span data-ttu-id="2e20b-345">Portugués (Portugal)</span><span class="sxs-lookup"><span data-stu-id="2e20b-345">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="2e20b-346">0x0813</span><span class="sxs-lookup"><span data-stu-id="2e20b-346">0x0813</span></span> | <span data-ttu-id="2e20b-347">Holandés belga</span><span class="sxs-lookup"><span data-stu-id="2e20b-347">Belgian Dutch</span></span>       | <span data-ttu-id="2e20b-348">0x081A</span><span class="sxs-lookup"><span data-stu-id="2e20b-348">0x081A</span></span> | <span data-ttu-id="2e20b-349">Serbo-Croatian (cirílico)</span><span class="sxs-lookup"><span data-stu-id="2e20b-349">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="2e20b-350">0x0814</span><span class="sxs-lookup"><span data-stu-id="2e20b-350">0x0814</span></span> | <span data-ttu-id="2e20b-351">¿Noruego?</span><span class="sxs-lookup"><span data-stu-id="2e20b-351">Norwegian ?</span></span> <span data-ttu-id="2e20b-352">Nynorsk</span><span class="sxs-lookup"><span data-stu-id="2e20b-352">Nynorsk</span></span> |        |                           |



 

</dd> <dt>

<span data-ttu-id="2e20b-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span><span class="sxs-lookup"><span data-stu-id="2e20b-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="2e20b-354">Uno de los siguientes identificadores de juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2e20b-354">One of the following character-set identifiers.</span></span>



| <span data-ttu-id="2e20b-355">Decimal</span><span class="sxs-lookup"><span data-stu-id="2e20b-355">Decimal</span></span> | <span data-ttu-id="2e20b-356">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="2e20b-356">Hexadecimal</span></span> | <span data-ttu-id="2e20b-357">Juego de caracteres</span><span class="sxs-lookup"><span data-stu-id="2e20b-357">Character Set</span></span>              |
|---------|-------------|----------------------------|
| <span data-ttu-id="2e20b-358">0</span><span class="sxs-lookup"><span data-stu-id="2e20b-358">0</span></span>       | <span data-ttu-id="2e20b-359">0000</span><span class="sxs-lookup"><span data-stu-id="2e20b-359">0000</span></span>        | <span data-ttu-id="2e20b-360">ASCII de 7 bits</span><span class="sxs-lookup"><span data-stu-id="2e20b-360">7-bit ASCII</span></span>                |
| <span data-ttu-id="2e20b-361">932</span><span class="sxs-lookup"><span data-stu-id="2e20b-361">932</span></span>     | <span data-ttu-id="2e20b-362">03A4</span><span class="sxs-lookup"><span data-stu-id="2e20b-362">03A4</span></span>        | <span data-ttu-id="2e20b-363">Japón (Shift?</span><span class="sxs-lookup"><span data-stu-id="2e20b-363">Japan (Shift ?</span></span> <span data-ttu-id="2e20b-364">JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="2e20b-364">JIS X-0208)</span></span> |
| <span data-ttu-id="2e20b-365">949</span><span class="sxs-lookup"><span data-stu-id="2e20b-365">949</span></span>     | <span data-ttu-id="2e20b-366">03B5</span><span class="sxs-lookup"><span data-stu-id="2e20b-366">03B5</span></span>        | <span data-ttu-id="2e20b-367">Corea (Shift?</span><span class="sxs-lookup"><span data-stu-id="2e20b-367">Korea (Shift ?</span></span> <span data-ttu-id="2e20b-368">KSC 5601)</span><span class="sxs-lookup"><span data-stu-id="2e20b-368">KSC 5601)</span></span>   |
| <span data-ttu-id="2e20b-369">950</span><span class="sxs-lookup"><span data-stu-id="2e20b-369">950</span></span>     | <span data-ttu-id="2e20b-370">03B6</span><span class="sxs-lookup"><span data-stu-id="2e20b-370">03B6</span></span>        | <span data-ttu-id="2e20b-371">Taiwán (Big5)</span><span class="sxs-lookup"><span data-stu-id="2e20b-371">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="2e20b-372">1200</span><span class="sxs-lookup"><span data-stu-id="2e20b-372">1200</span></span>    | <span data-ttu-id="2e20b-373">04B0</span><span class="sxs-lookup"><span data-stu-id="2e20b-373">04B0</span></span>        | <span data-ttu-id="2e20b-374">Unicode</span><span class="sxs-lookup"><span data-stu-id="2e20b-374">Unicode</span></span>                    |
| <span data-ttu-id="2e20b-375">1250</span><span class="sxs-lookup"><span data-stu-id="2e20b-375">1250</span></span>    | <span data-ttu-id="2e20b-376">04E2</span><span class="sxs-lookup"><span data-stu-id="2e20b-376">04E2</span></span>        | <span data-ttu-id="2e20b-377">Latín-2 (Europa Oriental)</span><span class="sxs-lookup"><span data-stu-id="2e20b-377">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="2e20b-378">1251</span><span class="sxs-lookup"><span data-stu-id="2e20b-378">1251</span></span>    | <span data-ttu-id="2e20b-379">04E3</span><span class="sxs-lookup"><span data-stu-id="2e20b-379">04E3</span></span>        | <span data-ttu-id="2e20b-380">Cirílico</span><span class="sxs-lookup"><span data-stu-id="2e20b-380">Cyrillic</span></span>                   |
| <span data-ttu-id="2e20b-381">1252</span><span class="sxs-lookup"><span data-stu-id="2e20b-381">1252</span></span>    | <span data-ttu-id="2e20b-382">04E4</span><span class="sxs-lookup"><span data-stu-id="2e20b-382">04E4</span></span>        | <span data-ttu-id="2e20b-383">Entornos</span><span class="sxs-lookup"><span data-stu-id="2e20b-383">Multilingual</span></span>               |
| <span data-ttu-id="2e20b-384">1253</span><span class="sxs-lookup"><span data-stu-id="2e20b-384">1253</span></span>    | <span data-ttu-id="2e20b-385">04E5</span><span class="sxs-lookup"><span data-stu-id="2e20b-385">04E5</span></span>        | <span data-ttu-id="2e20b-386">Griego</span><span class="sxs-lookup"><span data-stu-id="2e20b-386">Greek</span></span>                      |
| <span data-ttu-id="2e20b-387">1254</span><span class="sxs-lookup"><span data-stu-id="2e20b-387">1254</span></span>    | <span data-ttu-id="2e20b-388">04E6</span><span class="sxs-lookup"><span data-stu-id="2e20b-388">04E6</span></span>        | <span data-ttu-id="2e20b-389">Turco</span><span class="sxs-lookup"><span data-stu-id="2e20b-389">Turkish</span></span>                    |
| <span data-ttu-id="2e20b-390">1255</span><span class="sxs-lookup"><span data-stu-id="2e20b-390">1255</span></span>    | <span data-ttu-id="2e20b-391">04E7</span><span class="sxs-lookup"><span data-stu-id="2e20b-391">04E7</span></span>        | <span data-ttu-id="2e20b-392">Hebreo</span><span class="sxs-lookup"><span data-stu-id="2e20b-392">Hebrew</span></span>                     |
| <span data-ttu-id="2e20b-393">1256</span><span class="sxs-lookup"><span data-stu-id="2e20b-393">1256</span></span>    | <span data-ttu-id="2e20b-394">04E8</span><span class="sxs-lookup"><span data-stu-id="2e20b-394">04E8</span></span>        | <span data-ttu-id="2e20b-395">Árabe</span><span class="sxs-lookup"><span data-stu-id="2e20b-395">Arabic</span></span>                     |



 

</dd> <dt>

<span data-ttu-id="2e20b-396"><span id="string-name"></span><span id="STRING-NAME"></span>*nombre de cadena*</span><span class="sxs-lookup"><span data-stu-id="2e20b-396"><span id="string-name"></span><span id="STRING-NAME"></span>*string-name*</span></span>
</dt> <dd>

<span data-ttu-id="2e20b-397">Uno de los siguientes nombres predefinidos.</span><span class="sxs-lookup"><span data-stu-id="2e20b-397">One of the following predefined names.</span></span>



| <span data-ttu-id="2e20b-398">Nombre</span><span class="sxs-lookup"><span data-stu-id="2e20b-398">Name</span></span>                 | <span data-ttu-id="2e20b-399">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e20b-399">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e20b-400">**Comentarios**</span><span class="sxs-lookup"><span data-stu-id="2e20b-400">**Comments**</span></span>         | <span data-ttu-id="2e20b-401">Información adicional que se debe mostrar con fines de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="2e20b-401">Additional information that should be displayed for diagnostic purposes.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="2e20b-402">**Compañía**</span><span class="sxs-lookup"><span data-stu-id="2e20b-402">**CompanyName**</span></span>      | <span data-ttu-id="2e20b-403">¿Compañía que generó el archivo? por ejemplo, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc."</span><span class="sxs-lookup"><span data-stu-id="2e20b-403">Company that produced the file?for example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span> <span data-ttu-id="2e20b-404">Esta cadena es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="2e20b-404">This string is required.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="2e20b-405">**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="2e20b-405">**FileDescription**</span></span>  | <span data-ttu-id="2e20b-406">Descripción del archivo que se va a presentar a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="2e20b-406">File description to be presented to users.</span></span> <span data-ttu-id="2e20b-407">Esta cadena se puede mostrar en un cuadro de lista cuando el usuario elige los archivos que se van a instalar. por ejemplo, "controlador de teclado para AT-Style teclados".</span><span class="sxs-lookup"><span data-stu-id="2e20b-407">This string may be displayed in a list box when the user is choosing files to install?for example, "Keyboard Driver for AT-Style Keyboards".</span></span> <span data-ttu-id="2e20b-408">Esta cadena es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="2e20b-408">This string is required.</span></span>                                                                                            |
| <span data-ttu-id="2e20b-409">**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="2e20b-409">**FileVersion**</span></span>      | <span data-ttu-id="2e20b-410">Número de versión del archivo, por ejemplo, "3,10" o "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="2e20b-410">Version number of the file?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="2e20b-411">Esta cadena es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="2e20b-411">This string is required.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="2e20b-412">**InternalName**</span><span class="sxs-lookup"><span data-stu-id="2e20b-412">**InternalName**</span></span>     | <span data-ttu-id="2e20b-413">Nombre interno del archivo, si existe uno, por ejemplo, un nombre de módulo si el archivo es una biblioteca de vínculos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="2e20b-413">Internal name of the file, if one exists?for example, a module name if the file is a dynamic-link library.</span></span> <span data-ttu-id="2e20b-414">Si el archivo no tiene ningún nombre interno, esta cadena debe ser el nombre de archivo original, sin extensión.</span><span class="sxs-lookup"><span data-stu-id="2e20b-414">If the file has no internal name, this string should be the original filename, without extension.</span></span> <span data-ttu-id="2e20b-415">Esta cadena es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="2e20b-415">This string is required.</span></span>                                                                       |
| <span data-ttu-id="2e20b-416">**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="2e20b-416">**LegalCopyright**</span></span>   | <span data-ttu-id="2e20b-417">Avisos de copyright que se aplican al archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-417">Copyright notices that apply to the file.</span></span> <span data-ttu-id="2e20b-418">Esto debe incluir el texto completo de todos los avisos, símbolos legales, fechas de copyright, etc.</span><span class="sxs-lookup"><span data-stu-id="2e20b-418">This should include the full text of all notices, legal symbols, copyright dates, and so on.</span></span> <span data-ttu-id="2e20b-419">Esta cadena es opcional.</span><span class="sxs-lookup"><span data-stu-id="2e20b-419">This string is optional.</span></span>                                                                                                                                             |
| <span data-ttu-id="2e20b-420">**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="2e20b-420">**LegalTrademarks**</span></span>  | <span data-ttu-id="2e20b-421">Marcas comerciales y marcas registradas que se aplican al archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-421">Trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="2e20b-422">Esto debe incluir el texto completo de todos los avisos, símbolos legales, números de marcas comerciales, etc.</span><span class="sxs-lookup"><span data-stu-id="2e20b-422">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="2e20b-423">Esta cadena es opcional.</span><span class="sxs-lookup"><span data-stu-id="2e20b-423">This string is optional.</span></span>                                                                                                                        |
| <span data-ttu-id="2e20b-424">**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="2e20b-424">**OriginalFilename**</span></span> | <span data-ttu-id="2e20b-425">Nombre original del archivo, sin incluir una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="2e20b-425">Original name of the file, not including a path.</span></span> <span data-ttu-id="2e20b-426">Esta información permite que una aplicación determine si un usuario ha cambiado el nombre de un archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-426">This information enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="2e20b-427">El formato del nombre depende del sistema de archivos para el que se creó el archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-427">The format of the name depends on the file system for which the file was created.</span></span> <span data-ttu-id="2e20b-428">Esta cadena es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="2e20b-428">This string is required.</span></span>                                                 |
| <span data-ttu-id="2e20b-429">**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="2e20b-429">**PrivateBuild**</span></span>     | <span data-ttu-id="2e20b-430">Información sobre una versión privada del archivo, por ejemplo, "compilado por TESTER1 en \\ TESTBED".</span><span class="sxs-lookup"><span data-stu-id="2e20b-430">Information about a private version of the file?for example, "Built by TESTER1 on \\TESTBED".</span></span> <span data-ttu-id="2e20b-431">Esta cadena solo debe estar presente si **vs \_ FF \_ PRIVATEBUILD** se especifica en el parámetro *fileflags* del bloque raíz.</span><span class="sxs-lookup"><span data-stu-id="2e20b-431">This string should be present only if **VS\_FF\_PRIVATEBUILD** is specified in the *fileflags* parameter of the root block.</span></span>                                                                                   |
| <span data-ttu-id="2e20b-432">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="2e20b-432">**ProductName**</span></span>      | <span data-ttu-id="2e20b-433">Nombre del producto con el que se distribuye el archivo.</span><span class="sxs-lookup"><span data-stu-id="2e20b-433">Name of the product with which the file is distributed.</span></span> <span data-ttu-id="2e20b-434">Esta cadena es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="2e20b-434">This string is required.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="2e20b-435">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="2e20b-435">**ProductVersion**</span></span>   | <span data-ttu-id="2e20b-436">Versión del producto con la que se distribuye el archivo, por ejemplo, "3,10" o "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="2e20b-436">Version of the product with which the file is distributed?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="2e20b-437">Esta cadena es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="2e20b-437">This string is required.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="2e20b-438">**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="2e20b-438">**SpecialBuild**</span></span>     | <span data-ttu-id="2e20b-439">Texto que indica el modo en que esta versión del archivo difiere de la versión estándar. por ejemplo, "compilación privada para la solución de problemas del mouse en equipos M250 y M250E".</span><span class="sxs-lookup"><span data-stu-id="2e20b-439">Text that indicates how this version of the file differs from the standard version?for example, "Private build for TESTER1 solving mouse problems on M250 and M250E computers".</span></span> <span data-ttu-id="2e20b-440">Esta cadena solo debe estar presente si **vs \_ FF \_ SPECIALBUILD** se especifica en el parámetro *fileflags* del bloque raíz.</span><span class="sxs-lookup"><span data-stu-id="2e20b-440">This string should be present only if **VS\_FF\_SPECIALBUILD** is specified in the *fileflags* parameter of the root block.</span></span> |



 

</dd> </dl>

<span data-ttu-id="2e20b-441">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="2e20b-441">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="2e20b-442">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="2e20b-442">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2e20b-443">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2e20b-443">Examples</span></span>

<span data-ttu-id="2e20b-444">En el ejemplo siguiente se define un recurso **versionInfo** :</span><span class="sxs-lookup"><span data-stu-id="2e20b-444">The following example defines a **VERSIONINFO** resource:</span></span>

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a><span data-ttu-id="2e20b-445">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e20b-445">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e20b-446">Usar información de versión</span><span class="sxs-lookup"><span data-stu-id="2e20b-446">Using Version Information</span></span>](./using-version-information.md)
</dt> <dt>

[<span data-ttu-id="2e20b-447">Información de versión</span><span class="sxs-lookup"><span data-stu-id="2e20b-447">Version Information</span></span>](./version-information.md)
</dt> </dl>

 

 