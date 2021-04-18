---
title: Sintaxis
description: Esta es la sintaxis para llamar a FXC.exe, la herramienta de compilador de efectos. Para obtener un ejemplo, vea compilaciones sin conexión.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- FXC, sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105695786"
---
# <a name="syntax"></a><span data-ttu-id="d5c3a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5c3a-105">Syntax</span></span>

<span data-ttu-id="d5c3a-106">Esta es la sintaxis para llamar a FXC.exe, la herramienta de compilador de efectos.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-106">Here is the syntax for calling FXC.exe, the effect-compiler tool.</span></span> <span data-ttu-id="d5c3a-107">Para obtener un ejemplo, vea [compilaciones sin conexión](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="d5c3a-107">For an example, see [Offline Compiling](dx-graphics-tools-fxc-using.md).</span></span>

-   [<span data-ttu-id="d5c3a-108">Uso</span><span class="sxs-lookup"><span data-stu-id="d5c3a-108">Usage</span></span>](#usage)
-   [<span data-ttu-id="d5c3a-109">Argumentos</span><span class="sxs-lookup"><span data-stu-id="d5c3a-109">Arguments</span></span>](#arguments)
-   [<span data-ttu-id="d5c3a-110">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="d5c3a-110">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="d5c3a-111">Perfiles</span><span class="sxs-lookup"><span data-stu-id="d5c3a-111">Profiles</span></span>](#profiles)
-   [<span data-ttu-id="d5c3a-112">Notas de la versión</span><span class="sxs-lookup"><span data-stu-id="d5c3a-112">Version notes</span></span>](#version-notes)
-   [<span data-ttu-id="d5c3a-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5c3a-113">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="d5c3a-114">Uso</span><span class="sxs-lookup"><span data-stu-id="d5c3a-114">Usage</span></span>

<span data-ttu-id="d5c3a-115">*nombres de archivo* de **FXC** *SwitchOptions*</span><span class="sxs-lookup"><span data-stu-id="d5c3a-115">**fxc** *SwitchOptions* *Filenames*</span></span>

## <a name="arguments"></a><span data-ttu-id="d5c3a-116">Argumentos</span><span class="sxs-lookup"><span data-stu-id="d5c3a-116">Arguments</span></span>
<span data-ttu-id="d5c3a-117">Separe cada opción de modificador con un espacio o dos puntos.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-117">Separate each switch option with a space or a colon.</span></span>

### <a name="switchoptions"></a><span data-ttu-id="d5c3a-118">*SwitchOptions*</span><span class="sxs-lookup"><span data-stu-id="d5c3a-118">*SwitchOptions*</span></span>
<span data-ttu-id="d5c3a-119">\[en \] Opciones de compilación.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-119">\[in\] Compile options.</span></span> <span data-ttu-id="d5c3a-120">Hay solo una opción obligatoria y muchas más que son opcionales.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-120">There is just one required option, and many more that are optional.</span></span> <span data-ttu-id="d5c3a-121">Separe cada uno con un espacio o dos puntos.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-121">Separate each with a space or colon.</span></span>

#### <a name="required-option"></a><span data-ttu-id="d5c3a-122">Opción required</span><span class="sxs-lookup"><span data-stu-id="d5c3a-122">Required option</span></span>
##### <a name="t-profile"></a><span data-ttu-id="d5c3a-123">/T <*perfil*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-123">/T <*profile*></span></span>
<span data-ttu-id="d5c3a-124">Modelo de sombreador (consulte [perfiles](#profiles)).</span><span class="sxs-lookup"><span data-stu-id="d5c3a-124">Shader model (see [Profiles](#profiles)).</span></span>

#### <a name="optional-options"></a><span data-ttu-id="d5c3a-125">Opciones no necesarias</span><span class="sxs-lookup"><span data-stu-id="d5c3a-125">Optional options</span></span>
##### <a name="-help"></a><span data-ttu-id="d5c3a-126">/?, /help</span><span class="sxs-lookup"><span data-stu-id="d5c3a-126">/?, /help</span></span>
<span data-ttu-id="d5c3a-127">Ayuda de impresión para `FXC.exe` .</span><span class="sxs-lookup"><span data-stu-id="d5c3a-127">Print help for `FXC.exe`.</span></span>

##### <a name="commandoptionfile"></a><span data-ttu-id="d5c3a-128">@<*comando. Option. File*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-128">@<*command.option.file*></span></span>
<span data-ttu-id="d5c3a-129">Archivo que contiene opciones de compilación adicionales.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-129">File that contains additional compile options.</span></span> <span data-ttu-id="d5c3a-130">Esta opción se puede mezclar con otras opciones de compilación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-130">This option can be mixed with other command line compile options.</span></span> <span data-ttu-id="d5c3a-131">El *comando. Option. File* solo debe contener una opción por línea.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-131">The *command.option.file* must contain only one option per line.</span></span> <span data-ttu-id="d5c3a-132">El *comando. Option. File* no puede contener ninguna línea en blanco.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-132">The *command.option.file* cannot contain any blank lines.</span></span> <span data-ttu-id="d5c3a-133">Las opciones especificadas en el archivo no deben contener espacios iniciales ni finales.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-133">Options specified in the file must not contain any leading or trailing spaces.</span></span>

##### <a name="all_resources_bound"></a><span data-ttu-id="d5c3a-134">/all_resources_bound</span><span class="sxs-lookup"><span data-stu-id="d5c3a-134">/all_resources_bound</span></span>
<span data-ttu-id="d5c3a-135">Habilite el aplanamiento agresivo en SM 5.1 +.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-135">Enable aggressive flattening in SM5.1+.</span></span> <span data-ttu-id="d5c3a-136">Novedades de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-136">New for Direct3D 12.</span></span>

##### <a name="cc"></a><span data-ttu-id="d5c3a-137">/CC</span><span class="sxs-lookup"><span data-stu-id="d5c3a-137">/Cc</span></span>
<span data-ttu-id="d5c3a-138">Ensamblado con codificación de color de salida.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-138">Output color-coded assembly.</span></span>

##### <a name="compress"></a><span data-ttu-id="d5c3a-139">/compress</span><span class="sxs-lookup"><span data-stu-id="d5c3a-139">/compress</span></span>
<span data-ttu-id="d5c3a-140">Comprimir el código de bytes del sombreador de contenido DX10 desde archivos.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-140">Compress DX10 shader bytecode from files.</span></span>

##### <a name="d-idtext"></a><span data-ttu-id="d5c3a-141">/D < >=< *texto* de identificador></span><span class="sxs-lookup"><span data-stu-id="d5c3a-141">/D <*id*>=<*text*></span></span>
<span data-ttu-id="d5c3a-142">Definir macro.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-142">Define macro.</span></span>

##### <a name="decompress"></a><span data-ttu-id="d5c3a-143">/decompress</span><span class="sxs-lookup"><span data-stu-id="d5c3a-143">/decompress</span></span>
<span data-ttu-id="d5c3a-144">Descomprime el código de bytes del sombreador de contenido DX10 del primer archivo.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-144">Decompress DX10 shader bytecode from first file.</span></span> <span data-ttu-id="d5c3a-145">Los archivos de salida deben aparecer en el orden en que se encontraban durante la compresión.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-145">Output files should be listed in the order they were in during compression.</span></span>

##### <a name="dumpbin"></a><span data-ttu-id="d5c3a-146">/dumpbin</span><span class="sxs-lookup"><span data-stu-id="d5c3a-146">/dumpbin</span></span>
<span data-ttu-id="d5c3a-147">Carga un archivo binario en lugar de compilar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-147">Loads a binary file rather than compiling a shader.</span></span>

##### <a name="e-name"></a><span data-ttu-id="d5c3a-148">/E <name></span><span class="sxs-lookup"><span data-stu-id="d5c3a-148">/E <name></span></span>
<span data-ttu-id="d5c3a-149">Punto de entrada del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-149">Shader entry point.</span></span> <span data-ttu-id="d5c3a-150">Si no se proporciona ningún punto de entrada, se considera que **Main** es el nombre de la entrada del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-150">If no entry point is given, **main** is considered to be the shader entry name.</span></span>

##### <a name="enable_unbounded_descriptor_tables"></a><span data-ttu-id="d5c3a-151">/enable_unbounded_descriptor_tables</span><span class="sxs-lookup"><span data-stu-id="d5c3a-151">/enable_unbounded_descriptor_tables</span></span>
<span data-ttu-id="d5c3a-152">Habilita las tablas de descriptores sin enlazar.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-152">Enables unbounded descriptor tables.</span></span> <span data-ttu-id="d5c3a-153">Novedades de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-153">New for Direct3D 12.</span></span>

##### <a name="extractrootsignature-file"></a><span data-ttu-id="d5c3a-154">/extractrootsignature <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-154">/extractrootsignature <*file*></span></span>
<span data-ttu-id="d5c3a-155">Extraiga la firma raíz del código de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-155">Extract root signature from shader bytecode.</span></span> <span data-ttu-id="d5c3a-156">Novedades de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-156">New for Direct3D 12.</span></span>

##### <a name="fc-file"></a><span data-ttu-id="d5c3a-157">/FC <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-157">/Fc <*file*></span></span>
<span data-ttu-id="d5c3a-158">Archivo de lista de código de ensamblado de salida.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-158">Output assembly code listing file.</span></span>

##### <a name="fd-file"></a><span data-ttu-id="d5c3a-159">/FD <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-159">/Fd <*file*></span></span>
<span data-ttu-id="d5c3a-160">Extraiga la información de la base de datos de programa (PDB) del sombreador y escriba en el archivo especificado. Al compilar el sombreador, utilice/FD para generar un archivo PDB con información de depuración de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-160">Extract shader program database (PDB) info and write to the given file.When you compile the shader, use /Fd to generate a PDB file with shader debugging info.</span></span>

##### <a name="fe-file"></a><span data-ttu-id="d5c3a-161">/Fe <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-161">/Fe <*file*></span></span>
<span data-ttu-id="d5c3a-162">Genera advertencias y errores en el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-162">Output warnings and errors to the given file.</span></span>

##### <a name="fh-file"></a><span data-ttu-id="d5c3a-163">/FH <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-163">/Fh <*file*></span></span>
<span data-ttu-id="d5c3a-164">Archivo de encabezado de salida que contiene el código de objeto.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-164">Output header file containing object code.</span></span>

##### <a name="fl-file"></a><span data-ttu-id="d5c3a-165">/FL <*archivo*</span><span class="sxs-lookup"><span data-stu-id="d5c3a-165">/Fl <*file*</span></span>
<span data-ttu-id="d5c3a-166">Generar una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-166">Output a library.</span></span> <span data-ttu-id="d5c3a-167">Requiere el \_47.dll D3dcompiler o una versión posterior del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-167">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="fo-file"></a><span data-ttu-id="d5c3a-168">/FO <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-168">/Fo <*file*></span></span>
<span data-ttu-id="d5c3a-169">Archivo de objeto de salida.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-169">Output object file.</span></span> <span data-ttu-id="d5c3a-170">A menudo, dada la extensión &quot; . FXC &quot; , aunque se usan otras extensiones, como &quot; . o &quot; , &quot; . obj &quot; o &quot; . dxbc &quot; .</span><span class="sxs-lookup"><span data-stu-id="d5c3a-170">Often given the extension &quot;.fxc&quot;, though other extensions are used, such as &quot;.o&quot;, &quot;.obj&quot; or &quot;.dxbc&quot;.</span></span>

##### <a name="fx-file"></a><span data-ttu-id="d5c3a-171">/FX ( *archivo* <)></span><span class="sxs-lookup"><span data-stu-id="d5c3a-171">/Fx <*file*></span></span>
<span data-ttu-id="d5c3a-172">Código de ensamblado de salida y archivo de lista hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-172">Output assembly code and hex listing file.</span></span>

##### <a name="gch"></a><span data-ttu-id="d5c3a-173">/Gch</span><span class="sxs-lookup"><span data-stu-id="d5c3a-173">/Gch</span></span>
<span data-ttu-id="d5c3a-174">Compilar como efecto secundario para los perfiles de fx_4_x.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-174">Compile as a child effect for fx_4_x profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="d5c3a-175">La compatibilidad con los perfiles de efectos heredados está en desuso.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-175">Support for legacy Effects profiles is deprecated.</span></span>

##### <a name="gdp"></a><span data-ttu-id="d5c3a-176">/Gdp</span><span class="sxs-lookup"><span data-stu-id="d5c3a-176">/Gdp</span></span>
<span data-ttu-id="d5c3a-177">Deshabilitar el modo de rendimiento de efecto.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-177">Disable effect performance mode.</span></span>

##### <a name="gec"></a><span data-ttu-id="d5c3a-178">/Gec</span><span class="sxs-lookup"><span data-stu-id="d5c3a-178">/Gec</span></span>
<span data-ttu-id="d5c3a-179">Habilite el modo de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-179">Enable backward compatibility mode.</span></span>

##### <a name="ges"></a><span data-ttu-id="d5c3a-180">/Ges</span><span class="sxs-lookup"><span data-stu-id="d5c3a-180">/Ges</span></span>
<span data-ttu-id="d5c3a-181">Habilita el modo STRICT.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-181">Enable strict mode.</span></span>

##### <a name="getprivate-file"></a><span data-ttu-id="d5c3a-182">/getprivate <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-182">/getprivate <*file*></span></span>
<span data-ttu-id="d5c3a-183">Guarde los datos privados del BLOB del sombreador (binario del sombreador compilado) en el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-183">Save private data from the shader blob (compiled shader binary) to the given file.</span></span> <span data-ttu-id="d5c3a-184">Extrae los datos privados, insertados previamente por/setprivate, del BLOB de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-184">Extracts private data, previously embedded by /setprivate, from the shader blob.</span></span>

<span data-ttu-id="d5c3a-185">Debe especificar la opción/DUMPBIN con/getprivate.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-185">You must specify the /dumpbin option with /getprivate.</span></span> <span data-ttu-id="d5c3a-186">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d5c3a-186">For example:</span></span>

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a><span data-ttu-id="d5c3a-187">/Gfa</span><span class="sxs-lookup"><span data-stu-id="d5c3a-187">/Gfa</span></span>
<span data-ttu-id="d5c3a-188">Evite las construcciones de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-188">Avoid flow control constructs.</span></span>

##### <a name="gfp"></a><span data-ttu-id="d5c3a-189">/GFP</span><span class="sxs-lookup"><span data-stu-id="d5c3a-189">/Gfp</span></span>
<span data-ttu-id="d5c3a-190">Prefiere construcciones de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-190">Prefer flow control constructs.</span></span>

##### <a name="gis"></a><span data-ttu-id="d5c3a-191">/Gis</span><span class="sxs-lookup"><span data-stu-id="d5c3a-191">/Gis</span></span>
<span data-ttu-id="d5c3a-192">Forzar la limitación IEEE.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-192">Force IEEE strictness.</span></span>

##### <a name="gpp"></a><span data-ttu-id="d5c3a-193">/Gpp</span><span class="sxs-lookup"><span data-stu-id="d5c3a-193">/Gpp</span></span>
<span data-ttu-id="d5c3a-194">Forzar precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-194">Force partial precision.</span></span>
    
##### <a name="i-include"></a><span data-ttu-id="d5c3a-195">/I <*incluir*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-195">/I <*include*></span></span>
<span data-ttu-id="d5c3a-196">Ruta de acceso de inclusión adicional.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-196">Additional include path.</span></span>

##### <a name="lx"></a><span data-ttu-id="d5c3a-197">/Lx</span><span class="sxs-lookup"><span data-stu-id="d5c3a-197">/Lx</span></span>
<span data-ttu-id="d5c3a-198">Los literales hexadecimales de salida.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-198">Output hexadecimal literals.</span></span> <span data-ttu-id="d5c3a-199">Requiere el \_47.dll D3dcompiler o una versión posterior del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-199">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="matchuavs"></a><span data-ttu-id="d5c3a-200">/matchUAVs</span><span class="sxs-lookup"><span data-stu-id="d5c3a-200">/matchUAVs</span></span>
<span data-ttu-id="d5c3a-201">Coincide con las asignaciones de ranura UAV del sombreador de plantilla en el sombreador actual.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-201">Match template shader UAV slot allocations in the current shader.</span></span> <span data-ttu-id="d5c3a-202">Para obtener más información, vea la <a href="#remarks">sección Comentarios</a>.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-202">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="mergeuavs"></a><span data-ttu-id="d5c3a-203">/mergeUAVs</span><span class="sxs-lookup"><span data-stu-id="d5c3a-203">/mergeUAVs</span></span>
<span data-ttu-id="d5c3a-204">Combine las asignaciones de ranura UAV del sombreador de plantilla y del sombreador actual.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-204">Merge UAV slot allocations of template shader and the current shader.</span></span> <span data-ttu-id="d5c3a-205">Para obtener más información, vea la <a href=""></a> <a href="#remarks">sección Comentarios</a>.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-205">For more info, see <a href=""></a><a href="#remarks">Remarks</a>.</span></span>

##### <a name="ni"></a><span data-ttu-id="d5c3a-206">/Ni</span><span class="sxs-lookup"><span data-stu-id="d5c3a-206">/Ni</span></span>
<span data-ttu-id="d5c3a-207">Números de instrucciones de salida en listas de ensamblados.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-207">Output instruction numbers in assembly listings.</span></span>

##### <a name="no"></a><span data-ttu-id="d5c3a-208">/No</span><span class="sxs-lookup"><span data-stu-id="d5c3a-208">/No</span></span>
<span data-ttu-id="d5c3a-209">Desplazamiento de bytes de instrucción de salida en listas de ensamblados.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-209">Output instruction byte offset in assembly listings.</span></span> <span data-ttu-id="d5c3a-210">Al generar el ensamblado, utilice/no para anotarlo con el desplazamiento de bytes de cada instrucción.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-210">When you produce assembly, use /No to annotate it with the byte offset for each instruction.</span></span>

##### <a name="nologo"></a><span data-ttu-id="d5c3a-211">/nologo</span><span class="sxs-lookup"><span data-stu-id="d5c3a-211">/nologo</span></span>
<span data-ttu-id="d5c3a-212">Se suprime el mensaje de copyright.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-212">Suppress copyright message.</span></span>

##### <a name="od"></a><span data-ttu-id="d5c3a-213">/Od</span><span class="sxs-lookup"><span data-stu-id="d5c3a-213">/Od</span></span>
<span data-ttu-id="d5c3a-214">Deshabilite las optimizaciones.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-214">Disable optimizations.</span></span> <span data-ttu-id="d5c3a-215">/OD implica/GFP, aunque la salida no puede ser idéntica a/OD/GFP.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-215">/Od implies /Gfp, though output may not be identical to /Od /Gfp.</span></span>

##### <a name="op"></a><span data-ttu-id="d5c3a-216">/OP</span><span class="sxs-lookup"><span data-stu-id="d5c3a-216">/Op</span></span>
<span data-ttu-id="d5c3a-217">Deshabilitar los sombreadores (en desuso).</span><span class="sxs-lookup"><span data-stu-id="d5c3a-217">Disable preshaders (deprecated).</span></span>

##### <a name="o0-o1-o2-o3"></a><span data-ttu-id="d5c3a-218">/O0/O1,/O2,/O3</span><span class="sxs-lookup"><span data-stu-id="d5c3a-218">/O0 /O1, /O2, /O3</span></span>
<span data-ttu-id="d5c3a-219">Niveles de optimización.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-219">Optimization levels.</span></span> <span data-ttu-id="d5c3a-220">O1 es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-220">O1 is the default setting.</span></span>
- <span data-ttu-id="d5c3a-221">O0: deshabilita la reordenación de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-221">O0 - Disables instruction reordering.</span></span> <span data-ttu-id="d5c3a-222">Esto ayuda a reducir la carga de registro y permite una simulación de bucle más rápida.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-222">This helps reduce register load and enables faster loop simulation.</span></span>
- <span data-ttu-id="d5c3a-223">O1: deshabilita la reordenación de instrucciones para ps_3_0 y up.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-223">O1 - Disables instruction reordering for ps_3_0 and up.</span></span>
- <span data-ttu-id="d5c3a-224">O2: igual que O1.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-224">O2 - Same as O1.</span></span> <span data-ttu-id="d5c3a-225">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-225">Reserved for future use.</span></span>
- <span data-ttu-id="d5c3a-226">O3: igual que O1.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-226">O3 - Same as O1.</span></span> <span data-ttu-id="d5c3a-227">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-227">Reserved for future use.</span></span>

##### <a name="p-file"></a><span data-ttu-id="d5c3a-228">/P <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-228">/P <*file*></span></span>
<span data-ttu-id="d5c3a-229">Preprocesar para archivo (debe usarse por sí solo).</span><span class="sxs-lookup"><span data-stu-id="d5c3a-229">Preprocess to file (must be used alone).</span></span>

##### <a name="qstrip_debug"></a><span data-ttu-id="d5c3a-230">/Qstrip_debug</span><span class="sxs-lookup"><span data-stu-id="d5c3a-230">/Qstrip_debug</span></span>
<span data-ttu-id="d5c3a-231">Quitar datos de depuración del código de bytes del sombreador para perfiles de 4_0 +.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-231">Strip debug data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_priv"></a><span data-ttu-id="d5c3a-232">/Qstrip_priv</span><span class="sxs-lookup"><span data-stu-id="d5c3a-232">/Qstrip_priv</span></span>
<span data-ttu-id="d5c3a-233">Quite los datos privados del código de bytes de 4_0 + Shader.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-233">Strip the private data from 4_0+ shader bytecode.</span></span> <span data-ttu-id="d5c3a-234">Quita los datos privados (secuencia arbitraria de bytes) del BLOB del sombreador (binario del sombreador compilado) que se incrustó anteriormente con la `/setprivate <file>` opción.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-234">Removes private data (arbitrary sequence of bytes) from the shader blob (compiled shader binary) that you previously embedded with the `/setprivate <file>` option.</span></span>

<span data-ttu-id="d5c3a-235">Debe especificar la opción/DUMPBIN con/Qstrip_priv.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-235">You must specify the /dumpbin option with /Qstrip_priv.</span></span> <span data-ttu-id="d5c3a-236">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d5c3a-236">For example:</span></span>

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a><span data-ttu-id="d5c3a-237">/Qstrip_reflect</span><span class="sxs-lookup"><span data-stu-id="d5c3a-237">/Qstrip_reflect</span></span>
<span data-ttu-id="d5c3a-238">Quitar datos de reflexión del código de bytes del sombreador para perfiles de 4_0 +.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-238">Strip reflection data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_rootsignature"></a><span data-ttu-id="d5c3a-239">/Qstrip_rootsignature</span><span class="sxs-lookup"><span data-stu-id="d5c3a-239">/Qstrip_rootsignature</span></span>
<span data-ttu-id="d5c3a-240">Quitar la firma raíz del código de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-240">Strip root signature from shader bytecode.</span></span> <span data-ttu-id="d5c3a-241">Novedades de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-241">New for Direct3D 12.</span></span>

##### <a name="res_may_alias"></a><span data-ttu-id="d5c3a-242">/res_may_alias</span><span class="sxs-lookup"><span data-stu-id="d5c3a-242">/res_may_alias</span></span>
<span data-ttu-id="d5c3a-243">Supongamos que UAVs/SRVs puede tener un alias para cs_5_0 +.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-243">Assume that UAVs/SRVs may alias for cs_5_0+.</span></span> <span data-ttu-id="d5c3a-244">Requiere el \_47.dll D3dcompiler o una versión posterior del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-244">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="setprivate-file"></a><span data-ttu-id="d5c3a-245">/setprivate <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-245">/setprivate <*file*></span></span>
<span data-ttu-id="d5c3a-246">Agregue los datos privados del archivo especificado al BLOB del sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-246">Add private data in the given file to the compiled shader blob.</span></span> <span data-ttu-id="d5c3a-247">Inserta el archivo dado, que se trata como un búfer sin formato, en el BLOB del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-247">Embeds the given file, which is treated as a raw buffer, to the shader blob.</span></span> <span data-ttu-id="d5c3a-248">Use/setprivate para agregar datos privados al compilar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-248">Use /setprivate to add private data when you compile a shader.</span></span> <span data-ttu-id="d5c3a-249">O bien, use la opción/DUMPBIN con/setprivate para cargar un objeto de sombreador existente y, después, después de que el objeto esté en memoria, para agregar el BLOB de datos privados.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-249">Or, use the /dumpbin option with /setprivate to load an existing shader object, and then after the object is in memory, to add the private data blob.</span></span> <span data-ttu-id="d5c3a-250">Por ejemplo, use un solo comando con/setprivate para agregar datos privados a un BLOB de sombreador compilado:</span><span class="sxs-lookup"><span data-stu-id="d5c3a-250">For example, use either a single command with /setprivate to add private data to a compiled shader blob:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
<span data-ttu-id="d5c3a-251">O bien, use dos comandos en los que el segundo comando cargue un objeto de sombreador y, a continuación, agregue datos privados:</span><span class="sxs-lookup"><span data-stu-id="d5c3a-251">Or, use two commands where the second command loads a shader object and then adds private data:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a><span data-ttu-id="d5c3a-252">/setrootsignature <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-252">/setrootsignature <*file*></span></span>
<span data-ttu-id="d5c3a-253">Adjunte la firma raíz al código de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-253">Attach root signature to shader bytecode.</span></span> <span data-ttu-id="d5c3a-254">Novedades de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-254">New for Direct3D 12.</span></span>

##### <a name="shtemplate-file"></a><span data-ttu-id="d5c3a-255">/shtemplate <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-255">/shtemplate <*file*></span></span>
<span data-ttu-id="d5c3a-256">Use un archivo de sombreador de plantilla dado para los recursos de combinación (/mergeUAVs) y coincidentes (/matchUAVs).</span><span class="sxs-lookup"><span data-stu-id="d5c3a-256">Use given template shader file for merging (/mergeUAVs) and matching (/matchUAVs) resources.</span></span> <span data-ttu-id="d5c3a-257">Para obtener más información, vea la <a href="#remarks">sección Comentarios</a>.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-257">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="vd"></a><span data-ttu-id="d5c3a-258">/Vd</span><span class="sxs-lookup"><span data-stu-id="d5c3a-258">/Vd</span></span>
<span data-ttu-id="d5c3a-259">Deshabilite la validación.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-259">Disable validation.</span></span>

##### <a name="verifyrootsignature-file"></a><span data-ttu-id="d5c3a-260">/verifyrootsignature <*archivo*></span><span class="sxs-lookup"><span data-stu-id="d5c3a-260">/verifyrootsignature <*file*></span></span>
<span data-ttu-id="d5c3a-261">Compruebe el código de bytes del sombreador con la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-261">Verify shader bytecode against root signature.</span></span> <span data-ttu-id="d5c3a-262">Novedades de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-262">New for Direct3D 12.</span></span>

##### <a name="vi"></a><span data-ttu-id="d5c3a-263">/Vi</span><span class="sxs-lookup"><span data-stu-id="d5c3a-263">/Vi</span></span>
<span data-ttu-id="d5c3a-264">Muestra detalles sobre el proceso de inclusión.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-264">Display details about the include process.</span></span>

##### <a name="vn-name"></a><span data-ttu-id="d5c3a-265">/VN *nombre* de <></span><span class="sxs-lookup"><span data-stu-id="d5c3a-265">/Vn <*name*></span></span>
<span data-ttu-id="d5c3a-266">Use Name como nombre de variable en el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-266">Use name as variable name in header file.</span></span>

##### <a name="wx"></a><span data-ttu-id="d5c3a-267">/WX</span><span class="sxs-lookup"><span data-stu-id="d5c3a-267">/WX</span></span>
<span data-ttu-id="d5c3a-268">Trata las advertencias como errores.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-268">Treat warnings as errors.</span></span>

##### <a name="zi"></a><span data-ttu-id="d5c3a-269">/ZI</span><span class="sxs-lookup"><span data-stu-id="d5c3a-269">/Zi</span></span>
<span data-ttu-id="d5c3a-270">Habilite la información de depuración.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-270">Enable debugging information.</span></span>

##### <a name="zpc"></a><span data-ttu-id="d5c3a-271">/Zpc</span><span class="sxs-lookup"><span data-stu-id="d5c3a-271">/Zpc</span></span>
<span data-ttu-id="d5c3a-272">Empaquetar matrices en orden principal de columna.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-272">Pack matrices in column-major order.</span></span>

##### <a name="zpr"></a><span data-ttu-id="d5c3a-273">/Zpr</span><span class="sxs-lookup"><span data-stu-id="d5c3a-273">/Zpr</span></span>
<span data-ttu-id="d5c3a-274">Empaquetar matrices en orden principal de fila.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-274">Pack matrices in row-major order.</span></span>

### <a name="filenames"></a><span data-ttu-id="d5c3a-275">*Nombres de archivo*</span><span class="sxs-lookup"><span data-stu-id="d5c3a-275">*Filenames*</span></span>

<span data-ttu-id="d5c3a-276">\[en \] los archivos que contienen los sombreadores y/o los efectos (s).</span><span class="sxs-lookup"><span data-stu-id="d5c3a-276">\[in\] The files that contains the shader(s) and/or the effect(s).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5c3a-277">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5c3a-277">Remarks</span></span>

<span data-ttu-id="d5c3a-278">Use las `/mergeUAVs` `/matchUAVs` Opciones, y `/shtemplate` para alinear las ranuras de enlace UAV para una cadena de sombreadores.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-278">Use the `/mergeUAVs`, `/matchUAVs`, and `/shtemplate` options to align the UAV binding slots for a chain of shaders.</span></span>

<span data-ttu-id="d5c3a-279">Supongamos que tiene sombreadores A. FX, B. FX y C. FX.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-279">Suppose you have shaders A.fx, B.fx, and C.fx.</span></span> <span data-ttu-id="d5c3a-280">Para alinear las ranuras de enlace UAV para esta cadena de sombreadores, se necesitan dos pasos de compilación:</span><span class="sxs-lookup"><span data-stu-id="d5c3a-280">To align the UAV binding slots for this chain of shaders, you need two passes of compilation:</span></span>

<span data-ttu-id="d5c3a-281">**Para alinear las ranuras de enlace UAV para una cadena de sombreadores**</span><span class="sxs-lookup"><span data-stu-id="d5c3a-281">**To align the UAV binding slots for a chain of shaders**</span></span>

1.  <span data-ttu-id="d5c3a-282">Use/mergeUAVs para compilar los sombreadores y especifique un BLOB de sombreador compilado previamente con/shtemplate.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-282">Use /mergeUAVs to compile shaders, and specify a previously-compiled shader blob with /shtemplate.</span></span> <span data-ttu-id="d5c3a-283">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d5c3a-283">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  <span data-ttu-id="d5c3a-284">Use/matchUAVs para compilar los sombreadores y especifique el último BLOB del sombreador del primer paso con/shtemplate.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-284">Use /matchUAVs to compile shaders, and specify the last shader blob from the first pass with /shtemplate.</span></span> <span data-ttu-id="d5c3a-285">Puede compilar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-285">You can compile in any order.</span></span> <span data-ttu-id="d5c3a-286">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d5c3a-286">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
<span data-ttu-id="d5c3a-287">No es necesario volver a compilar C. FX en el segundo paso.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-287">You don't have to recompile C.fx in the second pass.</span></span>

<span data-ttu-id="d5c3a-288">Después de realizar las dos fases anteriores de compilación, puede usar una. o, B. o y C. o como Blobs finales del sombreador con ranuras UAV alineadas.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-288">After you perform the preceding two compilation passes, you can use A.o, B.o, and C.o as final shader blobs with aligned UAV slots.</span></span>

## <a name="profiles"></a><span data-ttu-id="d5c3a-289">Profiles</span><span class="sxs-lookup"><span data-stu-id="d5c3a-289">Profiles</span></span>

<span data-ttu-id="d5c3a-290">Cada modelo de sombreador se etiqueta con un perfil de HLSL.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-290">Each shader model is labeled with an HLSL profile.</span></span> <span data-ttu-id="d5c3a-291">Para compilar un sombreador en un modelo de sombreador determinado, elija el perfil de sombreador adecuado en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-291">To compile a shader against a particular shader model, choose the appropriate shader profile from the following table.</span></span>

<table><thead><tr class="header"><th><span data-ttu-id="d5c3a-292">Tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d5c3a-292">Shader Type</span></span></th><th><span data-ttu-id="d5c3a-293">Profiles</span><span class="sxs-lookup"><span data-stu-id="d5c3a-293">Profiles</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="d5c3a-294">Sombreador de cálculo</span><span class="sxs-lookup"><span data-stu-id="d5c3a-294">Compute Shader</span></span></td><td><dl> <span data-ttu-id="d5c3a-295">cs_4_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-295">cs_4_0</span></span><br />
<span data-ttu-id="d5c3a-296">cs_4_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-296">cs_4_1</span></span><br />
<span data-ttu-id="d5c3a-297">cs_5_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-297">cs_5_0</span></span><br />
<span data-ttu-id="d5c3a-298">cs_5_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-298">cs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="d5c3a-299">Sombreador de dominios</span><span class="sxs-lookup"><span data-stu-id="d5c3a-299">Domain Shader</span></span></td><td><dl> <span data-ttu-id="d5c3a-300">ds_5_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-300">ds_5_0</span></span><br />
<span data-ttu-id="d5c3a-301">ds_5_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-301">ds_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="d5c3a-302">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="d5c3a-302">Geometry Shader</span></span></td><td><dl> <span data-ttu-id="d5c3a-303">gs_4_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-303">gs_4_0</span></span><br />
<span data-ttu-id="d5c3a-304">gs_4_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-304">gs_4_1</span></span><br />
<span data-ttu-id="d5c3a-305">gs_5_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-305">gs_5_0</span></span><br />
<span data-ttu-id="d5c3a-306">gs_5_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-306">gs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="d5c3a-307">Vinculación de sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="d5c3a-307">HLSL shader linking</span></span> </td><td><dl> <span data-ttu-id="d5c3a-308">lib_4_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-308">lib_4_0</span></span><br />
<span data-ttu-id="d5c3a-309">lib_4_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-309">lib_4_1</span></span><br />
<span data-ttu-id="d5c3a-310">lib_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-310">lib_4_0_level_9_1</span></span><br />
<span data-ttu-id="d5c3a-311">lib_4_0_level_9_1_vs_only</span><span class="sxs-lookup"><span data-stu-id="d5c3a-311">lib_4_0_level_9_1_vs_only</span></span><br />
<span data-ttu-id="d5c3a-312">lib_4_0_level_9_1_ps_only</span><span class="sxs-lookup"><span data-stu-id="d5c3a-312">lib_4_0_level_9_1_ps_only</span></span><br />
<span data-ttu-id="d5c3a-313">lib_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="d5c3a-313">lib_4_0_level_9_3</span></span><br />
<span data-ttu-id="d5c3a-314">lib_4_0_level_9_3_vs_only</span><span class="sxs-lookup"><span data-stu-id="d5c3a-314">lib_4_0_level_9_3_vs_only</span></span><br />
<span data-ttu-id="d5c3a-315">lib_4_0_level_9_3_ps_only</span><span class="sxs-lookup"><span data-stu-id="d5c3a-315">lib_4_0_level_9_3_ps_only</span></span><br />
<span data-ttu-id="d5c3a-316">lib_5_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-316">lib_5_0</span></span><br />
</dl> <span data-ttu-id="d5c3a-317">Para obtener más información sobre la vinculación del sombreador, vea <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> y <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-317">For more info about shader linking, see <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> and <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span></span> <br/></td></tr><tr class="odd"><td><span data-ttu-id="d5c3a-318">Sombreador de casco</span><span class="sxs-lookup"><span data-stu-id="d5c3a-318">Hull Shader</span></span></td><td><dl> <span data-ttu-id="d5c3a-319">hs_5_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-319">hs_5_0</span></span><br />
<span data-ttu-id="d5c3a-320">hs_5_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-320">hs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="d5c3a-321">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d5c3a-321">Pixel Shader</span></span></td><td><dl> <span data-ttu-id="d5c3a-322">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-322">ps_2_0</span></span><br />
<span data-ttu-id="d5c3a-323">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="d5c3a-323">ps_2_a</span></span><br />
<span data-ttu-id="d5c3a-324">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="d5c3a-324">ps_2_b</span></span><br />
<span data-ttu-id="d5c3a-325">ps_2_sw</span><span class="sxs-lookup"><span data-stu-id="d5c3a-325">ps_2_sw</span></span><br />
<span data-ttu-id="d5c3a-326">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-326">ps_3_0</span></span><br />
<span data-ttu-id="d5c3a-327">ps_3_sw</span><span class="sxs-lookup"><span data-stu-id="d5c3a-327">ps_3_sw</span></span><br />
<span data-ttu-id="d5c3a-328">ps_4_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-328">ps_4_0</span></span><br />
<span data-ttu-id="d5c3a-329">ps_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-329">ps_4_0_level_9_0</span></span><br />
<span data-ttu-id="d5c3a-330">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-330">ps_4_0_level_9_1</span></span><br />
<span data-ttu-id="d5c3a-331">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="d5c3a-331">ps_4_0_level_9_3</span></span><br />
<span data-ttu-id="d5c3a-332">ps_4_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-332">ps_4_1</span></span><br />
<span data-ttu-id="d5c3a-333">ps_5_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-333">ps_5_0</span></span><br />
<span data-ttu-id="d5c3a-334">ps_5_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-334">ps_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="d5c3a-335">Firma raíz</span><span class="sxs-lookup"><span data-stu-id="d5c3a-335">Root Signature</span></span></td><td><dl> <span data-ttu-id="d5c3a-336">rootsig_1_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-336">rootsig_1_0</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="d5c3a-337">Sombreador de textura</span><span class="sxs-lookup"><span data-stu-id="d5c3a-337">Texture Shader</span></span></td><td><dl> <span data-ttu-id="d5c3a-338">tx_1_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-338">tx_1_0</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="d5c3a-339">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="d5c3a-339">Vertex Shader</span></span></td><td><dl> <span data-ttu-id="d5c3a-340">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-340">vs_1_1</span></span><br />
<span data-ttu-id="d5c3a-341">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-341">vs_2_0</span></span><br />
<span data-ttu-id="d5c3a-342">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="d5c3a-342">vs_2_a</span></span><br />
<span data-ttu-id="d5c3a-343">vs_2_sw</span><span class="sxs-lookup"><span data-stu-id="d5c3a-343">vs_2_sw</span></span><br />
<span data-ttu-id="d5c3a-344">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-344">vs_3_0</span></span><br />
<span data-ttu-id="d5c3a-345">vs_3_sw</span><span class="sxs-lookup"><span data-stu-id="d5c3a-345">vs_3_sw</span></span><br />
<span data-ttu-id="d5c3a-346">vs_4_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-346">vs_4_0</span></span><br />
<span data-ttu-id="d5c3a-347">vs_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-347">vs_4_0_level_9_0</span></span><br />
<span data-ttu-id="d5c3a-348">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-348">vs_4_0_level_9_1</span></span><br />
<span data-ttu-id="d5c3a-349">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="d5c3a-349">vs_4_0_level_9_3</span></span><br />
<span data-ttu-id="d5c3a-350">vs_4_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-350">vs_4_1</span></span><br />
<span data-ttu-id="d5c3a-351">vs_5_0</span><span class="sxs-lookup"><span data-stu-id="d5c3a-351">vs_5_0</span></span><br />
<span data-ttu-id="d5c3a-352">vs_5_1</span><span class="sxs-lookup"><span data-stu-id="d5c3a-352">vs_5_1</span></span><br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a><span data-ttu-id="d5c3a-353">Notas de la versión</span><span class="sxs-lookup"><span data-stu-id="d5c3a-353">Version notes</span></span>

<span data-ttu-id="d5c3a-354">Para Direct3D 12, consulte [especificación de firmas raíz en HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [enlace de recursos en HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) y [indexación dinámica con HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span><span class="sxs-lookup"><span data-stu-id="d5c3a-354">For Direct3D 12 refer to [Specifying Root Signatures in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Resource Binding in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) and [Dynamic Indexing using HLSL 5.1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span></span>

<span data-ttu-id="d5c3a-355">En Direct3D 10, use la API para obtener el perfil de vértices, geometría y sombreador de píxeles más adecuado para un dispositivo determinado mediante una llamada a estas funciones: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)y [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="d5c3a-355">In Direct3D 10 use the API to get the vertex, geometry, and pixel-shader profile best suited to a given device by calling these functions: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile), and [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span></span>

<span data-ttu-id="d5c3a-356">En Direct3D 9, use los métodos [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) o [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) para recuperar los perfiles de sombreador de vértices y píxeles que admite un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5c3a-356">In Direct3D 9 use the [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) or [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) methods to retrieve the vertex and pixel-shader profiles supported by a device.</span></span> <span data-ttu-id="d5c3a-357">La estructura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) devuelta por esos métodos indica el vértice y los perfiles del sombreador de píxeles admitidos por un dispositivo en sus miembros **VertexShaderVersion** y **PixelShaderVersion** .</span><span class="sxs-lookup"><span data-stu-id="d5c3a-357">The [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure returned by those methods indicates the vertex and pixel-shader profiles supported by a device in its **VertexShaderVersion** and **PixelShaderVersion** members.</span></span>

<span data-ttu-id="d5c3a-358">Para obtener ejemplos, vea [compilar con el compilador actual](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="d5c3a-358">For examples, see [Compiling with the Current Compiler](dx-graphics-tools-fxc-using.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5c3a-359">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5c3a-359">Related topics</span></span>

* [<span data-ttu-id="d5c3a-360">Efecto: herramienta de compilador</span><span class="sxs-lookup"><span data-stu-id="d5c3a-360">Effect-Compiler Tool</span></span>](fxc.md)