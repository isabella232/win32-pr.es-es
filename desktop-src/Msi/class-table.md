---
description: La tabla de clases contiene información relacionada con el servidor COM que se debe generar como parte del anuncio del producto. Cada fila puede generar un conjunto de claves y valores del registro. La información asociada de ProgId se incluye en esta tabla.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Tabla de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666995"
---
# <a name="class-table"></a><span data-ttu-id="466c1-105">Tabla de clases</span><span class="sxs-lookup"><span data-stu-id="466c1-105">Class Table</span></span>

<span data-ttu-id="466c1-106">La tabla de clases contiene información relacionada con el servidor COM que se debe generar como parte del anuncio del producto.</span><span class="sxs-lookup"><span data-stu-id="466c1-106">The Class table contains COM server-related information that must be generated as a part of the product advertisement.</span></span> <span data-ttu-id="466c1-107">Cada fila puede generar un conjunto de claves y valores del registro.</span><span class="sxs-lookup"><span data-stu-id="466c1-107">Each row may generate a set of registry keys and values.</span></span> <span data-ttu-id="466c1-108">La información asociada de ProgId se incluye en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="466c1-108">The associated ProgId information is included in this table.</span></span>

<span data-ttu-id="466c1-109">La tabla de la clase tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="466c1-109">The Class table has the following columns.</span></span>



| <span data-ttu-id="466c1-110">Columna</span><span class="sxs-lookup"><span data-stu-id="466c1-110">Column</span></span>           | <span data-ttu-id="466c1-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="466c1-111">Type</span></span>                         | <span data-ttu-id="466c1-112">Clave</span><span class="sxs-lookup"><span data-stu-id="466c1-112">Key</span></span> | <span data-ttu-id="466c1-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="466c1-113">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="466c1-114">CLSID</span><span class="sxs-lookup"><span data-stu-id="466c1-114">CLSID</span></span>            | [<span data-ttu-id="466c1-115">GUID</span><span class="sxs-lookup"><span data-stu-id="466c1-115">GUID</span></span>](guid.md)             | <span data-ttu-id="466c1-116">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-116">Y</span></span>   | <span data-ttu-id="466c1-117">N</span><span class="sxs-lookup"><span data-stu-id="466c1-117">N</span></span>        |
| <span data-ttu-id="466c1-118">Context</span><span class="sxs-lookup"><span data-stu-id="466c1-118">Context</span></span>          | [<span data-ttu-id="466c1-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="466c1-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="466c1-120">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-120">Y</span></span>   | <span data-ttu-id="466c1-121">N</span><span class="sxs-lookup"><span data-stu-id="466c1-121">N</span></span>        |
| <span data-ttu-id="466c1-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="466c1-122">Component\_</span></span>      | [<span data-ttu-id="466c1-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="466c1-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="466c1-124">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-124">Y</span></span>   | <span data-ttu-id="466c1-125">N</span><span class="sxs-lookup"><span data-stu-id="466c1-125">N</span></span>        |
| <span data-ttu-id="466c1-126">\_Valor predeterminado de ProgID</span><span class="sxs-lookup"><span data-stu-id="466c1-126">ProgId\_Default</span></span>  | [<span data-ttu-id="466c1-127">Texto</span><span class="sxs-lookup"><span data-stu-id="466c1-127">Text</span></span>](text.md)             | <span data-ttu-id="466c1-128">N</span><span class="sxs-lookup"><span data-stu-id="466c1-128">N</span></span>   | <span data-ttu-id="466c1-129">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-129">Y</span></span>        |
| <span data-ttu-id="466c1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="466c1-130">Description</span></span>      | [<span data-ttu-id="466c1-131">Texto</span><span class="sxs-lookup"><span data-stu-id="466c1-131">Text</span></span>](text.md)             | <span data-ttu-id="466c1-132">N</span><span class="sxs-lookup"><span data-stu-id="466c1-132">N</span></span>   | <span data-ttu-id="466c1-133">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-133">Y</span></span>        |
| <span data-ttu-id="466c1-134">AppId\_</span><span class="sxs-lookup"><span data-stu-id="466c1-134">AppId\_</span></span>          | [<span data-ttu-id="466c1-135">GUID</span><span class="sxs-lookup"><span data-stu-id="466c1-135">GUID</span></span>](guid.md)             | <span data-ttu-id="466c1-136">N</span><span class="sxs-lookup"><span data-stu-id="466c1-136">N</span></span>   | <span data-ttu-id="466c1-137">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-137">Y</span></span>        |
| <span data-ttu-id="466c1-138">FileTypeMask</span><span class="sxs-lookup"><span data-stu-id="466c1-138">FileTypeMask</span></span>     | [<span data-ttu-id="466c1-139">Texto</span><span class="sxs-lookup"><span data-stu-id="466c1-139">Text</span></span>](text.md)             | <span data-ttu-id="466c1-140">N</span><span class="sxs-lookup"><span data-stu-id="466c1-140">N</span></span>   | <span data-ttu-id="466c1-141">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-141">Y</span></span>        |
| <span data-ttu-id="466c1-142">Icono\_</span><span class="sxs-lookup"><span data-stu-id="466c1-142">Icon\_</span></span>           | [<span data-ttu-id="466c1-143">Identificador</span><span class="sxs-lookup"><span data-stu-id="466c1-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="466c1-144">N</span><span class="sxs-lookup"><span data-stu-id="466c1-144">N</span></span>   | <span data-ttu-id="466c1-145">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-145">Y</span></span>        |
| <span data-ttu-id="466c1-146">IconIndex</span><span class="sxs-lookup"><span data-stu-id="466c1-146">IconIndex</span></span>        | [<span data-ttu-id="466c1-147">Entero</span><span class="sxs-lookup"><span data-stu-id="466c1-147">Integer</span></span>](integer.md)       | <span data-ttu-id="466c1-148">N</span><span class="sxs-lookup"><span data-stu-id="466c1-148">N</span></span>   | <span data-ttu-id="466c1-149">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-149">Y</span></span>        |
| <span data-ttu-id="466c1-150">DefInprocHandler</span><span class="sxs-lookup"><span data-stu-id="466c1-150">DefInprocHandler</span></span> | [<span data-ttu-id="466c1-151">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="466c1-151">Filename</span></span>](filename.md)     | <span data-ttu-id="466c1-152">N</span><span class="sxs-lookup"><span data-stu-id="466c1-152">N</span></span>   | <span data-ttu-id="466c1-153">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-153">Y</span></span>        |
| <span data-ttu-id="466c1-154">Argumento</span><span class="sxs-lookup"><span data-stu-id="466c1-154">Argument</span></span>         | [<span data-ttu-id="466c1-155">Formatea</span><span class="sxs-lookup"><span data-stu-id="466c1-155">Formatted</span></span>](formatted.md)   | <span data-ttu-id="466c1-156">N</span><span class="sxs-lookup"><span data-stu-id="466c1-156">N</span></span>   | <span data-ttu-id="466c1-157">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-157">Y</span></span>        |
| <span data-ttu-id="466c1-158">Característica\_</span><span class="sxs-lookup"><span data-stu-id="466c1-158">Feature\_</span></span>        | [<span data-ttu-id="466c1-159">Identificador</span><span class="sxs-lookup"><span data-stu-id="466c1-159">Identifier</span></span>](identifier.md) | <span data-ttu-id="466c1-160">N</span><span class="sxs-lookup"><span data-stu-id="466c1-160">N</span></span>   | <span data-ttu-id="466c1-161">N</span><span class="sxs-lookup"><span data-stu-id="466c1-161">N</span></span>        |
| <span data-ttu-id="466c1-162">Atributos</span><span class="sxs-lookup"><span data-stu-id="466c1-162">Attributes</span></span>       | [<span data-ttu-id="466c1-163">Entero</span><span class="sxs-lookup"><span data-stu-id="466c1-163">Integer</span></span>](integer.md)       | <span data-ttu-id="466c1-164">N</span><span class="sxs-lookup"><span data-stu-id="466c1-164">N</span></span>   | <span data-ttu-id="466c1-165">Y</span><span class="sxs-lookup"><span data-stu-id="466c1-165">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="466c1-166">Información de columna</span><span class="sxs-lookup"><span data-stu-id="466c1-166">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="466c1-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span><span class="sxs-lookup"><span data-stu-id="466c1-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="466c1-168">Identificador de clase (ID.) de un servidor COM.</span><span class="sxs-lookup"><span data-stu-id="466c1-168">The Class identifier (ID) of a COM server.</span></span>

</dd> <dt>

<span data-ttu-id="466c1-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Contexto</span><span class="sxs-lookup"><span data-stu-id="466c1-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Context</span></span>
</dt> <dd>

<span data-ttu-id="466c1-170">El contexto de servidor para este servidor.</span><span class="sxs-lookup"><span data-stu-id="466c1-170">The server context for this server.</span></span> <span data-ttu-id="466c1-171">Escriba uno de los siguientes valores para la clave CLSID.</span><span class="sxs-lookup"><span data-stu-id="466c1-171">Enter one of the following values for the CLSID Key.</span></span>



| <span data-ttu-id="466c1-172">CLAVE CLSID</span><span class="sxs-lookup"><span data-stu-id="466c1-172">CLSID KEY</span></span>                             | <span data-ttu-id="466c1-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="466c1-173">Description</span></span>                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="466c1-174">LocalServer</span><span class="sxs-lookup"><span data-stu-id="466c1-174">LocalServer</span></span>](../com/localserver.md)       | <span data-ttu-id="466c1-175">Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="466c1-175">Specifies the full path to a 16-bit local server application.</span></span>             |
| [<span data-ttu-id="466c1-176">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="466c1-176">LocalServer32</span></span>](../com/localserver32.md)   | <span data-ttu-id="466c1-177">Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="466c1-177">Specifies the full path to a 32-bit local server application.</span></span>             |
| [<span data-ttu-id="466c1-178">InprocServer</span><span class="sxs-lookup"><span data-stu-id="466c1-178">InprocServer</span></span>](../com/inprocserver.md)     | <span data-ttu-id="466c1-179">Especifica la ruta de acceso a un archivo DLL de servidor en proceso.</span><span class="sxs-lookup"><span data-stu-id="466c1-179">Specifies the path to an in-process server DLL.</span></span>                           |
| [<span data-ttu-id="466c1-180">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="466c1-180">InprocServer32</span></span>](../com/inprocserver32.md) | <span data-ttu-id="466c1-181">Especifica la ruta de acceso a un servidor de proceso de 32 bits y al modelo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="466c1-181">Specifies the path to a 32-bit in-process server and the threading model.</span></span> |



 

</dd> <dt>

<span data-ttu-id="466c1-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="466c1-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="466c1-183">Clave externa en la [tabla de componentes](component-table.md) que especifica el componente cuyo archivo de clave proporciona el servidor com.</span><span class="sxs-lookup"><span data-stu-id="466c1-183">External key into the [Component table](component-table.md) specifying the component whose key file provides the COM server.</span></span>

</dd> <dt>

<span data-ttu-id="466c1-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>\_Valor predeterminado de ProgID</span><span class="sxs-lookup"><span data-stu-id="466c1-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId\_Default</span></span>
</dt> <dd>

<span data-ttu-id="466c1-185">IDENTIFICADOR de programa predeterminado asociado a este identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="466c1-185">The default Program ID associated with this Class ID.</span></span> <span data-ttu-id="466c1-186">Esta columna es una clave externa de la [tabla ProgID](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="466c1-186">This column is a foreign key into the [ProgID table](progid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="466c1-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="466c1-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="466c1-188">Descripción localizada asociada con el identificador de clase y el ID. de programa.</span><span class="sxs-lookup"><span data-stu-id="466c1-188">Localized description associated with the Class ID and Program ID.</span></span>

</dd> <dt>

<span data-ttu-id="466c1-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span><span class="sxs-lookup"><span data-stu-id="466c1-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span></span>
</dt> <dd>

<span data-ttu-id="466c1-190">IDENTIFICADOR de la aplicación que contiene información de DCOM para la aplicación asociada ( [GUID](guid.md)de cadena).</span><span class="sxs-lookup"><span data-stu-id="466c1-190">Application ID containing DCOM information for the associated application (string [GUID](guid.md)).</span></span> <span data-ttu-id="466c1-191">Esta columna es una clave externa en la [tabla AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="466c1-191">This column is a foreign key into the [AppId table](appid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="466c1-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span><span class="sxs-lookup"><span data-stu-id="466c1-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span></span>
</dt> <dd>

<span data-ttu-id="466c1-193">Contiene información de la clave HKCR (este CLSID).</span><span class="sxs-lookup"><span data-stu-id="466c1-193">Contains information for the HKCR (this CLSID) key.</span></span>

<span data-ttu-id="466c1-194">Si existen varios patrones, deben delimitarse con un punto y coma, y se generan subclaves numéricas: 0, 1, 2... Para obtener más información acerca de esta funcionalidad, vea [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span><span class="sxs-lookup"><span data-stu-id="466c1-194">If multiple patterns exist, they must be delimited by a semicolon, and numeric subkeys are generated: 0, 1, 2... For more information about this functionality, see [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span></span>

</dd> <dt>

<span data-ttu-id="466c1-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icono\_</span><span class="sxs-lookup"><span data-stu-id="466c1-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="466c1-196">Archivo que proporciona el icono asociado a este CLSID.</span><span class="sxs-lookup"><span data-stu-id="466c1-196">The file providing the icon associated with this CLSID.</span></span> <span data-ttu-id="466c1-197">El instalador escribe la entrada en esta columna en la clave DefaultIcon asociada al ProgId.</span><span class="sxs-lookup"><span data-stu-id="466c1-197">The installer writes the entry in this column under the DefaultIcon key associated with the ProgId.</span></span> <span data-ttu-id="466c1-198">Si no es null, la columna es una clave externa en la [tabla de iconos](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="466c1-198">If it is not null, the column is a foreign key into the [Icon table](icon-table.md).</span></span> <span data-ttu-id="466c1-199">Si es null, el servidor COM proporciona el recurso de icono.</span><span class="sxs-lookup"><span data-stu-id="466c1-199">If it is null, the COM server provides the icon resource.</span></span> <span data-ttu-id="466c1-200">Los accesos directos y las asociaciones de archivos anunciados requieren un valor distinto de NULL en esta columna para que se muestren correctamente.</span><span class="sxs-lookup"><span data-stu-id="466c1-200">Advertised file associations and shortcuts require a non-null value in this column to display properly.</span></span>

</dd> <dt>

<span data-ttu-id="466c1-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="466c1-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="466c1-202">Índice del icono en el archivo de icono.</span><span class="sxs-lookup"><span data-stu-id="466c1-202">Icon index into the icon file.</span></span> <span data-ttu-id="466c1-203">Puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="466c1-203">This can be null.</span></span>

<span data-ttu-id="466c1-204">Solo números no negativos.</span><span class="sxs-lookup"><span data-stu-id="466c1-204">Non-negative numbers only.</span></span>

</dd> <dt>

<span data-ttu-id="466c1-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span><span class="sxs-lookup"><span data-stu-id="466c1-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span></span>
</dt> <dd>

<span data-ttu-id="466c1-206">Este campo especifica el controlador de in-Process predeterminado para el contexto de servidor especificado en el campo de contexto.</span><span class="sxs-lookup"><span data-stu-id="466c1-206">This field specifies the default in-process handler for the server context specified in the Context field.</span></span>

<span data-ttu-id="466c1-207">Este campo debe ser null si aparece una clave CLSID de InprocServer o InprocServer en el campo de contexto.</span><span class="sxs-lookup"><span data-stu-id="466c1-207">This field must be Null if an InprocServer or InprocServer CLSID key appears in the Context field.</span></span>

<span data-ttu-id="466c1-208">Si aparece una clave CLSID de LocalServer o LocalServer32 en el campo de contexto, el valor del campo DefInprocHandler identifica el controlador en proceso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="466c1-208">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the value in the DefInprocHandler field identifies the default in-process handler.</span></span>



| <span data-ttu-id="466c1-209">Value</span><span class="sxs-lookup"><span data-stu-id="466c1-209">Value</span></span>                | <span data-ttu-id="466c1-210">Descripción</span><span class="sxs-lookup"><span data-stu-id="466c1-210">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="466c1-211">valor no numérico</span><span class="sxs-lookup"><span data-stu-id="466c1-211">non-numeric value</span></span>    | <span data-ttu-id="466c1-212">El instalador trata un valor no numérico en el campo DefInprocHandler como un archivo del sistema que actúa como el controlador en proceso de 32 bits especificado por la clave InprocHandler32.</span><span class="sxs-lookup"><span data-stu-id="466c1-212">The installer treats a non-numeric value in the DefInprocHandler field as a system file serving as the 32-bit in-process handler specified by the InprocHandler32 key.</span></span>                                                                                                            |
| <span data-ttu-id="466c1-213">Null</span><span class="sxs-lookup"><span data-stu-id="466c1-213">Null</span></span>                 | <span data-ttu-id="466c1-214">Los campos DefInprocHandler y argument pueden ser null para una clave CLSID LocalServer o LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="466c1-214">The DefInprocHandler and Argument fields can both be Null for a LocalServer or LocalServer32 CLSID key.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="466c1-215">1 = valor predeterminado (sistema)</span><span class="sxs-lookup"><span data-stu-id="466c1-215">1 = default (system)</span></span> | <span data-ttu-id="466c1-216">El valor predeterminado es el controlador en proceso de 16 bits especificado por InprocHandler.</span><span class="sxs-lookup"><span data-stu-id="466c1-216">The default is the 16-bit in-process handler specified by InprocHandler.</span></span> <span data-ttu-id="466c1-217">En este caso, el valor de InprocHandler es el nombre del registro en el que se almacena el valor del controlador en proceso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="466c1-217">In this case, the value of InprocHandler is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="466c1-218">Por ejemplo, HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="466c1-218">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span>     |
| <span data-ttu-id="466c1-219">2 = valor predeterminado (sistema)</span><span class="sxs-lookup"><span data-stu-id="466c1-219">2 = default (system)</span></span> | <span data-ttu-id="466c1-220">El valor predeterminado es el controlador en proceso de 32 bits especificado por InprocHandler32.</span><span class="sxs-lookup"><span data-stu-id="466c1-220">The default is the 32-bit in-process handler specified by InprocHandler32.</span></span> <span data-ttu-id="466c1-221">En este caso, el valor de InprocHandler32 es el nombre del registro en el que se almacena el valor del controlador en proceso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="466c1-221">In this case, the value of InprocHandler32 is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="466c1-222">Por ejemplo, HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="466c1-222">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span> |
| <span data-ttu-id="466c1-223">3 = valor predeterminado (sistema)</span><span class="sxs-lookup"><span data-stu-id="466c1-223">3 = default (system)</span></span> | <span data-ttu-id="466c1-224">El valor predeterminado es un controlador en proceso de 16 ó 32 bits.</span><span class="sxs-lookup"><span data-stu-id="466c1-224">The default is a 16-bit or 32-bit in-process handler.</span></span>                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="466c1-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span><span class="sxs-lookup"><span data-stu-id="466c1-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="466c1-226">Si aparece una clave CLSID de LocalServer o LocalServer32 en el campo de contexto, el texto de este campo se registra como argumento en el servidor y COM lo usa para invocar el servidor.</span><span class="sxs-lookup"><span data-stu-id="466c1-226">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the text in this field is registered as the argument against the server and is used by COM to invoke the server.</span></span> <span data-ttu-id="466c1-227">Los campos DefInprocHandler y argument pueden ser null si se muestra LocalServer o LocalServer32 en el campo de contexto.</span><span class="sxs-lookup"><span data-stu-id="466c1-227">The DefInprocHandler and Argument fields can both be Null if LocalServer or LocalServer32 appears in the Context field.</span></span>

<span data-ttu-id="466c1-228">Tenga en cuenta que la resolución de propiedades en el campo argumento es limitada.</span><span class="sxs-lookup"><span data-stu-id="466c1-228">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="466c1-229">Una propiedad con formato \[ \] de propiedad en este campo solo se puede resolver si la propiedad ya tiene el valor previsto cuando el componente propietario de la clase está instalado.</span><span class="sxs-lookup"><span data-stu-id="466c1-229">A property formatted as \[Property\] in this field can only be resolved if the property already has the intended value when the component owning the class is installed.</span></span> <span data-ttu-id="466c1-230">Por ejemplo, para que el argumento " \[ \#MyDoc.doc\] " resuelva el valor correcto, el mismo proceso debe instalar el archivo MyDoc.doc y el componente que posee la clase.</span><span class="sxs-lookup"><span data-stu-id="466c1-230">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the class.</span></span>

</dd> <dt>

<span data-ttu-id="466c1-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_</span><span class="sxs-lookup"><span data-stu-id="466c1-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="466c1-232">Clave externa en la [tabla de características](feature-table.md) que especifica la característica que proporciona el servidor com.</span><span class="sxs-lookup"><span data-stu-id="466c1-232">External key into the [Feature table](feature-table.md) specifying the feature that provides the COM server.</span></span>

<span data-ttu-id="466c1-233">Clave externa para la columna uno de la tabla de características.</span><span class="sxs-lookup"><span data-stu-id="466c1-233">External key to column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="466c1-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus</span><span class="sxs-lookup"><span data-stu-id="466c1-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="466c1-235">Si **msidbClassAttributesRelativePath** se establece en esta columna, el nombre de archivo no operativo se puede usar para servidores com.</span><span class="sxs-lookup"><span data-stu-id="466c1-235">If **msidbClassAttributesRelativePath** is set in this column, the bare file name can be used for COM servers.</span></span> <span data-ttu-id="466c1-236">El instalador solo registra el nombre de archivo en lugar de la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="466c1-236">The installer registers the file name only instead of the complete path.</span></span> <span data-ttu-id="466c1-237">Esto permite que el servidor del directorio actual tenga prioridad y permita varias copias del mismo componente.</span><span class="sxs-lookup"><span data-stu-id="466c1-237">This enables the server in the current directory to take precedence and allows multiple copies of the same component.</span></span>



| <span data-ttu-id="466c1-238">Atributo</span><span class="sxs-lookup"><span data-stu-id="466c1-238">Attribute</span></span>                            | <span data-ttu-id="466c1-239">Decimal</span><span class="sxs-lookup"><span data-stu-id="466c1-239">Decimal</span></span> | <span data-ttu-id="466c1-240">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="466c1-240">Hexadecimal</span></span> |
|--------------------------------------|---------|-------------|
| <span data-ttu-id="466c1-241">**msidbClassAttributesRelativePath**</span><span class="sxs-lookup"><span data-stu-id="466c1-241">**msidbClassAttributesRelativePath**</span></span> | <span data-ttu-id="466c1-242">1</span><span class="sxs-lookup"><span data-stu-id="466c1-242">1</span></span>       | <span data-ttu-id="466c1-243">0x001</span><span class="sxs-lookup"><span data-stu-id="466c1-243">0x001</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="466c1-244">Observaciones</span><span class="sxs-lookup"><span data-stu-id="466c1-244">Remarks</span></span>

<span data-ttu-id="466c1-245">Se hace referencia a esta tabla cuando se ejecuta la acción [RegisterClassInfo](registerclassinfo-action.md) o la [acción UnregisterClassInfo](unregisterclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="466c1-245">This table is referred to when the [RegisterClassInfo action](registerclassinfo-action.md) or the [UnregisterClassInfo action](unregisterclassinfo-action.md) are executed.</span></span>

## <a name="validation"></a><span data-ttu-id="466c1-246">Validación</span><span class="sxs-lookup"><span data-stu-id="466c1-246">Validation</span></span>

<dl>

[<span data-ttu-id="466c1-247">ICE03</span><span class="sxs-lookup"><span data-stu-id="466c1-247">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="466c1-248">ICE06</span><span class="sxs-lookup"><span data-stu-id="466c1-248">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="466c1-249">ICE19</span><span class="sxs-lookup"><span data-stu-id="466c1-249">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="466c1-250">ICE32</span><span class="sxs-lookup"><span data-stu-id="466c1-250">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="466c1-251">ICE36</span><span class="sxs-lookup"><span data-stu-id="466c1-251">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="466c1-252">ICE41</span><span class="sxs-lookup"><span data-stu-id="466c1-252">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="466c1-253">ICE42</span><span class="sxs-lookup"><span data-stu-id="466c1-253">ICE42</span></span>](ice42.md)  
[<span data-ttu-id="466c1-254">ICE46</span><span class="sxs-lookup"><span data-stu-id="466c1-254">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="466c1-255">ICE66</span><span class="sxs-lookup"><span data-stu-id="466c1-255">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="466c1-256">ICE69</span><span class="sxs-lookup"><span data-stu-id="466c1-256">ICE69</span></span>](ice69.md)  
</dl>

 

 
