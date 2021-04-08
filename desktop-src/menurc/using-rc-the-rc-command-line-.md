---
title: Using RC (The RC Command Line) [Uso de RC (la línea de comandos de RC)]
description: Para iniciar RC, use el siguiente comando.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995182"
---
# <a name="using-rc-the-rc-command-line"></a><span data-ttu-id="d9798-103">Using RC (The RC Command Line) [Uso de RC (la línea de comandos de RC)]</span><span class="sxs-lookup"><span data-stu-id="d9798-103">Using RC (The RC Command Line)</span></span>

<span data-ttu-id="d9798-104">Para iniciar RC, use el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="d9798-104">To start RC, use the following command.</span></span>

<span data-ttu-id="d9798-105">**RC** \[ *Opciones* \] de *archivo de script*</span><span class="sxs-lookup"><span data-stu-id="d9798-105">**RC** \[*options*\] *script-file*</span></span>

<span data-ttu-id="d9798-106">El parámetro *script-File* especifica el nombre del archivo de definición de recursos que contiene los nombres, tipos, nombres de archivo y descripciones de los recursos que se van a compilar.</span><span class="sxs-lookup"><span data-stu-id="d9798-106">The *script-file* parameter specifies the name of the resource-definition file that contains the names, types, filenames, and descriptions of the resources to be compiled.</span></span>

<span data-ttu-id="d9798-107">RC puede generar archivos de recursos independientes para las aplicaciones que tienen recursos independientes del idioma y específicos del idioma.</span><span class="sxs-lookup"><span data-stu-id="d9798-107">RC can generate separate resource files for applications that have both language-neutral and language-specific resources.</span></span> <span data-ttu-id="d9798-108">Los desarrolladores pueden usar un [archivo de configuración de recursos](/windows/desktop/Intl/preparing-resources) o establecer opciones de línea de comandos para seleccionar qué tipos de recursos y elementos son recursos no localizables del [archivo independiente del lenguaje (LN)](/windows/desktop/Intl/mui-resource-management) y cuáles son recursos localizables de archivos mui específicos del idioma.</span><span class="sxs-lookup"><span data-stu-id="d9798-108">Developers can use a [resource configuration file](/windows/desktop/Intl/preparing-resources) or set command-line options to select which resource types and items are non-localizable resources of the [language-neutral (LN) file](/windows/desktop/Intl/mui-resource-management) and which are localizable resources of language-specific MUI files.</span></span> <span data-ttu-id="d9798-109">Para obtener más información, consulte la [interfaz de usuario multilingüe](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="d9798-109">For more information, see the [Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="d9798-110">El parámetro *Options* puede ser una o varias de las siguientes opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d9798-110">The *options* parameter can be one or more of the following command-line options.</span></span>

## <a name="options"></a><span data-ttu-id="d9798-111">Opciones</span><span class="sxs-lookup"><span data-stu-id="d9798-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="d9798-112"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="d9798-112"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-113">Muestra una lista de opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d9798-113">Displays a list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-114"><span id="_c"></span><span id="_C"></span>**/c**</span><span class="sxs-lookup"><span data-stu-id="d9798-114"><span id="_c"></span><span id="_C"></span>**/c**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-115">Define una página de códigos que utiliza la conversión de NLS.</span><span class="sxs-lookup"><span data-stu-id="d9798-115">Defines a code page used by NLS conversion.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-116"><span id="_d"></span><span id="_D"></span>**/d.**</span><span class="sxs-lookup"><span data-stu-id="d9798-116"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-117">Define un símbolo para el preprocesador que se puede probar con la directiva [**\# ifdef**](-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="d9798-117">Defines a symbol for the preprocessor that you can test with the [**\#ifdef**](-ifdef.md) directive.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/FM** *mresname*</span><span class="sxs-lookup"><span data-stu-id="d9798-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*</span></span>
</dt> <dd>

<span data-ttu-id="d9798-119">RC crea un independiente del idioma. Archivo RES y una dependiente del lenguaje (MUI). Archivo RES con *el archivo de script*.</span><span class="sxs-lookup"><span data-stu-id="d9798-119">RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file using *script-file*.</span></span> <span data-ttu-id="d9798-120">Esta opción debe usarse junto con la opción **/FO** *resname* .</span><span class="sxs-lookup"><span data-stu-id="d9798-120">This option must be used together with the **/fo** *resname* option.</span></span> <span data-ttu-id="d9798-121">RC da nombre al idioma neutro. Archivo RES *resname. res* y el nombre depende del idioma (MUI). Archivo RES *mresname. res*.</span><span class="sxs-lookup"><span data-stu-id="d9798-121">RC names the language-neutral .RES file *resname.res* and names the language-dependent (MUI) .RES file *mresname.res*.</span></span>

<span data-ttu-id="d9798-122">**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las funciones [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.</span><span class="sxs-lookup"><span data-stu-id="d9798-122">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/FO** *resname*</span><span class="sxs-lookup"><span data-stu-id="d9798-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*</span></span>
</dt> <dd>

<span data-ttu-id="d9798-124">RC crea un. Archivo RES denominado *resname* con *el archivo de script*.</span><span class="sxs-lookup"><span data-stu-id="d9798-124">RC creates a .RES file named *resname* using *script-file*.</span></span>

<span data-ttu-id="d9798-125">Si también se establece la opción **/FM** *mresname* , RC crea un independiente del idioma. Archivo RES y una dependiente del lenguaje (MUI). Archivo RES.</span><span class="sxs-lookup"><span data-stu-id="d9798-125">If the **/fm** *mresname* option is also set, RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file.</span></span>

<span data-ttu-id="d9798-126">**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las funciones [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.</span><span class="sxs-lookup"><span data-stu-id="d9798-126">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-127"><span id="_g1"></span><span id="_G1"></span>**/G1**</span><span class="sxs-lookup"><span data-stu-id="d9798-127"><span id="_g1"></span><span id="_G1"></span>**/g1**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-128">Si se establece/G1, RC genera un archivo MUI si el único recurso traducible que se incluye en el archivo MUI es un recurso de versión.</span><span class="sxs-lookup"><span data-stu-id="d9798-128">If /g1, is set, RC generates a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span> <span data-ttu-id="d9798-129">Si no se establece/G1, RC no generará un archivo MUI si el único recurso traducible que se incluye en el archivo MUI es un recurso de versión.</span><span class="sxs-lookup"><span data-stu-id="d9798-129">If /g1 is not set, RC will not generate a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-130"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="d9798-130"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-131">Muestra la lista de opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d9798-131">Displays the list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-132"><span id="_I"></span><span id="_i"></span>**/I**</span><span class="sxs-lookup"><span data-stu-id="d9798-132"><span id="_I"></span><span id="_i"></span>**/I**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-133">Busca en el directorio especificado antes de buscar en los directorios especificados por la variable de entorno INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="d9798-133">Searches the specified directory before searching the directories specified by the INCLUDE environment variable.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *LOCTYPE*</span><span class="sxs-lookup"><span data-stu-id="d9798-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span></span>
</dt> <dd>

<span data-ttu-id="d9798-135">Los tipos de recursos localizables RC colocan en el dependiente del lenguaje (MUI). Archivo RES.</span><span class="sxs-lookup"><span data-stu-id="d9798-135">Localizable resource types RC places into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="d9798-136">Si también se establece la opción **/q** , se omite esta opción y la información del archivo de configuración RC tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="d9798-136">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="d9798-137">**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las funciones [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.</span><span class="sxs-lookup"><span data-stu-id="d9798-137">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** - *sobretype*</span><span class="sxs-lookup"><span data-stu-id="d9798-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *overtype*</span></span>
</dt> <dd>

<span data-ttu-id="d9798-139">Los tipos de recursos superpuestos que RC colocan en el lenguaje neutro. RES y el dependiente del lenguaje (MUI). Archivos RES.</span><span class="sxs-lookup"><span data-stu-id="d9798-139">Overlapping resource types that RC places into both the language-neutral .RES and the language-dependent (MUI).RES files.</span></span> <span data-ttu-id="d9798-140">Los tipos de recursos especificados por la opción **/k** deben ser un subconjunto de los especificados por la opción **/j** .</span><span class="sxs-lookup"><span data-stu-id="d9798-140">The resource types that are specified by the **/k** option must be a subset of those that are specified by the **/j** option.</span></span> <span data-ttu-id="d9798-141">Por ejemplo,? J2? J3? K3 especifica que RC coloca el tipo de recurso 3 en los archivos independientes del idioma y del idioma (MUI).</span><span class="sxs-lookup"><span data-stu-id="d9798-141">For example, ?J2 ?J3 ?K3 specifies that RC places resource type 3 in both the language-neutral and language-dependent (MUI) files.</span></span> <span data-ttu-id="d9798-142">Si también se establece la opción **/q** , se omite esta opción y la información del archivo de configuración RC tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="d9798-142">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="d9798-143">**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las funciones [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.</span><span class="sxs-lookup"><span data-stu-id="d9798-143">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*</span><span class="sxs-lookup"><span data-stu-id="d9798-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*</span></span>
</dt> <dd>

<span data-ttu-id="d9798-145">Especifica el idioma predeterminado para la compilación.</span><span class="sxs-lookup"><span data-stu-id="d9798-145">Specifies the default language for compilation.</span></span> <span data-ttu-id="d9798-146">Por ejemplo,-l409 es equivalente a incluir la siguiente instrucción en la parte superior del archivo de script de recursos: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span><span class="sxs-lookup"><span data-stu-id="d9798-146">For example, -l409 is equivalent to including the following statement at the top of the resource script file: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span></span>

<span data-ttu-id="d9798-147">Para obtener más información, vea [identificadores de idioma](/windows/desktop/Intl/language-identifiers).</span><span class="sxs-lookup"><span data-stu-id="d9798-147">For more information, see [Language Identifiers](/windows/desktop/Intl/language-identifiers).</span></span>

</dd> <dt>

<span data-ttu-id="d9798-148"><span id="_n"></span><span id="_N"></span>**/n**</span><span class="sxs-lookup"><span data-stu-id="d9798-148"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-149">Null finaliza todas las cadenas de la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="d9798-149">Null terminates all strings in the string table.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *MUI. RCConfig*</span><span class="sxs-lookup"><span data-stu-id="d9798-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *Mui.RCConfig*</span></span>
</dt> <dd>

<span data-ttu-id="d9798-151">Un archivo de configuración RC que sigue el formato del archivo de configuración RC.</span><span class="sxs-lookup"><span data-stu-id="d9798-151">An RC configuration file that follows the RC Configuration File format.</span></span> <span data-ttu-id="d9798-152">El formato de archivo de configuración RC permite a los componentes describir automáticamente la información de recursos, como el control de versiones de recursos, la ruta de acceso del archivo MUI, los tipos de recursos y los elementos.</span><span class="sxs-lookup"><span data-stu-id="d9798-152">The RC Configuration File format enables components to self-describe resource information such as resource versioning, MUI file path, resource types and items.</span></span> <span data-ttu-id="d9798-153">Este archivo especifica qué recursos entran en el idioma neutro. Archivo RES y los recursos que se incluyen en el lenguaje (MUI). Archivo RES.</span><span class="sxs-lookup"><span data-stu-id="d9798-153">This file specifies which resources go into the language-neutral .RES file and which resources go into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="d9798-154">Esta opción y la información proporcionada en el archivo de configuración RC invalidan las opciones de línea de comandos **/j** y **/k**.</span><span class="sxs-lookup"><span data-stu-id="d9798-154">This option, and the information provided in the RC Configuration file, override the command line options **/j** and **/k**.</span></span>

<span data-ttu-id="d9798-155">**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las funciones [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.</span><span class="sxs-lookup"><span data-stu-id="d9798-155">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-156"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="d9798-156"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-157">ignorado.</span><span class="sxs-lookup"><span data-stu-id="d9798-157">Ignored.</span></span> <span data-ttu-id="d9798-158">Se proporciona para ofrecer compatibilidad con los archivos make existentes.</span><span class="sxs-lookup"><span data-stu-id="d9798-158">Provided for compatibility with existing makefiles.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-159"><span id="_u"></span><span id="_U"></span>**/u**</span><span class="sxs-lookup"><span data-stu-id="d9798-159"><span id="_u"></span><span id="_U"></span>**/u**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-160">Anula la definición de un símbolo para el preprocesador.</span><span class="sxs-lookup"><span data-stu-id="d9798-160">Undefines a symbol for the preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-161"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="d9798-161"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-162">Muestra mensajes que informan sobre el progreso del compilador.</span><span class="sxs-lookup"><span data-stu-id="d9798-162">Displays messages that report on the progress of the compiler.</span></span>

</dd> <dt>

<span data-ttu-id="d9798-163"><span id="_x"></span><span id="_X"></span>**/x**</span><span class="sxs-lookup"><span data-stu-id="d9798-163"><span id="_x"></span><span id="_X"></span>**/x**</span></span>
</dt> <dd>

<span data-ttu-id="d9798-164">Impide que RC Compruebe la variable de entorno INCLUDE al buscar archivos de encabezado o archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9798-164">Prevents RC from checking the INCLUDE environment variable when searching for header files or resource files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9798-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9798-165">Remarks</span></span>

<span data-ttu-id="d9798-166">Las opciones no distinguen mayúsculas de minúsculas y se puede usar un guion (-) en lugar de una barra diagonal (/).</span><span class="sxs-lookup"><span data-stu-id="d9798-166">Options are not case sensitive, and a hyphen (-) can be used in place of a slash mark (/).</span></span> <span data-ttu-id="d9798-167">Puede combinar las opciones de una sola letra si no requieren ningún parámetro adicional.</span><span class="sxs-lookup"><span data-stu-id="d9798-167">You can combine single-letter options if they do not require any additional parameters.</span></span>

<span data-ttu-id="d9798-168">RC no generará un archivo MUI en los casos siguientes.</span><span class="sxs-lookup"><span data-stu-id="d9798-168">RC will not generate a MUI file in the following cases.</span></span>

-   <span data-ttu-id="d9798-169">No existe ningún recurso traducible en el archivo. rc.</span><span class="sxs-lookup"><span data-stu-id="d9798-169">No localizable resources exist in the .rc file.</span></span>
-   <span data-ttu-id="d9798-170">El único identificador de idioma de recurso especificado en el archivo. RC es neutro (0X0).</span><span class="sxs-lookup"><span data-stu-id="d9798-170">The only resource language id specified in the .rc file is neutral (0x0).</span></span>
-   <span data-ttu-id="d9798-171">El archivo. rc tiene recursos que se especifican en más de un idioma.</span><span class="sxs-lookup"><span data-stu-id="d9798-171">The .rc file has resources that are specified in more than one language.</span></span> <span data-ttu-id="d9798-172">La excepción es si el archivo. RC contiene dos idiomas y un idioma es neutro (0X0), RC genera un archivo MUI.</span><span class="sxs-lookup"><span data-stu-id="d9798-172">The exception is if the .rc file contains two languages, and one language is neutral (0x0), RC generates a MUI file.</span></span>

<span data-ttu-id="d9798-173">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d9798-173">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d9798-174">Definir nombres para el preprocesador</span><span class="sxs-lookup"><span data-stu-id="d9798-174">Defining Names for the Preprocessor</span></span>](defining-names-for-the-preprocessor.md)
-   [<span data-ttu-id="d9798-175">Cambiar el nombre del archivo de recursos compilados</span><span class="sxs-lookup"><span data-stu-id="d9798-175">Renaming the Compiled Resource File</span></span>](renaming-the-compiled-resource-file.md)
-   [<span data-ttu-id="d9798-176">Buscar archivos</span><span class="sxs-lookup"><span data-stu-id="d9798-176">Searching for Files</span></span>](searching-for-files.md)
-   [<span data-ttu-id="d9798-177">Mostrar mensajes de progreso</span><span class="sxs-lookup"><span data-stu-id="d9798-177">Displaying Progress Messages</span></span>](displaying-progress-messages.md)
-   [<span data-ttu-id="d9798-178">RC mensajes de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="d9798-178">RC Diagnostic Messages</span></span>](rc-diagnostic-messages.md)

## <a name="related-topics"></a><span data-ttu-id="d9798-179">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9798-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9798-180">Interfaz de usuario multilingüe</span><span class="sxs-lookup"><span data-stu-id="d9798-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 