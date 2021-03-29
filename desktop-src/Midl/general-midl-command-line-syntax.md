---
title: Sintaxis de línea de comandos de MIDL general
description: El compilador MIDL procesa un archivo IDL y un archivo de configuración de la aplicación (ACF) opcional para generar un conjunto de archivos de salida.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- referencia de la línea de comandos MIDL, sintaxis general
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903824"
---
# <a name="general-midl-command-line-syntax"></a><span data-ttu-id="f83be-104">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="f83be-104">General MIDL Command-line Syntax</span></span>

<span data-ttu-id="f83be-105">El compilador MIDL procesa un archivo IDL y un archivo de configuración de la aplicación (ACF) opcional para generar un conjunto de archivos de salida.</span><span class="sxs-lookup"><span data-stu-id="f83be-105">The MIDL compiler processes an IDL file and an optional application configuration file (ACF) to generate a set of output files.</span></span> <span data-ttu-id="f83be-106">Los atributos especificados en la lista de atributos de interfaz del archivo IDL determinan si el compilador genera archivos de origen para una interfaz RPC o para una interfaz OLE personalizada.</span><span class="sxs-lookup"><span data-stu-id="f83be-106">The attributes specified in the IDL file's interface attribute list determine whether the compiler generates source files for an RPC interface or for a custom OLE interface.</span></span>

## <a name="switch-options"></a><span data-ttu-id="f83be-107">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="f83be-107">Switch Options</span></span>

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span data-ttu-id="f83be-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*modificador de línea de comandos*</span><span class="sxs-lookup"><span data-stu-id="f83be-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*command-line-switch*</span></span>
</dt> <dd>

<span data-ttu-id="f83be-109">Especifica los modificadores de la línea de comandos del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="f83be-109">Specifies MIDL compiler command-line switches.</span></span> <span data-ttu-id="f83be-110">Los modificadores pueden aparecer en cualquier secuencia.</span><span class="sxs-lookup"><span data-stu-id="f83be-110">Switches can appear in any sequence.</span></span>

</dd> <dt>

<span data-ttu-id="f83be-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*Switch-Options*</span><span class="sxs-lookup"><span data-stu-id="f83be-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*switch-options*</span></span>
</dt> <dd>

<span data-ttu-id="f83be-112">Especifica las opciones asociadas a cada modificador.</span><span class="sxs-lookup"><span data-stu-id="f83be-112">Specifies options associated with each switch.</span></span> <span data-ttu-id="f83be-113">Las opciones válidas se describen en la entrada de referencia para cada conmutador de compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="f83be-113">Valid options are described in the reference entry for each MIDL compiler switch.</span></span>

</dd> <dt>

<span data-ttu-id="f83be-114"><span id="filename"></span><span id="FILENAME"></span>*extensión*</span><span class="sxs-lookup"><span data-stu-id="f83be-114"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="f83be-115">Especifica el nombre del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f83be-115">Specifies the name of the IDL file.</span></span> <span data-ttu-id="f83be-116">Normalmente, este archivo tiene la extensión. idl, pero puede tener otro o ninguno.</span><span class="sxs-lookup"><span data-stu-id="f83be-116">This file usually has the extension .idl, but it can have another or none.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f83be-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f83be-117">Remarks</span></span>

<span data-ttu-id="f83be-118">En las listas siguientes se muestran los nombres predeterminados de los archivos generados para un archivo IDL denominado Name. idl.</span><span class="sxs-lookup"><span data-stu-id="f83be-118">The following lists show the default names of the files generated for an IDL file named Name.idl.</span></span> <span data-ttu-id="f83be-119">Puede usar modificadores de la línea de comandos para invalidar estos nombres predeterminados.</span><span class="sxs-lookup"><span data-stu-id="f83be-119">You can use command-line switches to override these default names.</span></span> <span data-ttu-id="f83be-120">Tenga en cuenta que el nombre del archivo IDL puede tener una extensión que no sea. idl o ninguna extensión.</span><span class="sxs-lookup"><span data-stu-id="f83be-120">Note that the name of the IDL file can have an extension other than .idl, or no extension at all.</span></span>

<span data-ttu-id="f83be-121">De forma predeterminada (es decir, si la lista de atributos de interfaz no contiene el [**objeto**](object.md) o el atributo [**local**](local.md) ), el compilador genera los siguientes archivos para una [interfaz RPC](files-generated-for-an-rpc-interface.md):</span><span class="sxs-lookup"><span data-stu-id="f83be-121">By default (that is, if the interface attribute list does not contain the [**object**](object.md) or [**local**](local.md) attribute), the compiler generates the following files for an [RPC interface](files-generated-for-an-rpc-interface.md):</span></span>

-   <span data-ttu-id="f83be-122">Código auxiliar de cliente (nombre \_ c. c)</span><span class="sxs-lookup"><span data-stu-id="f83be-122">Client stub (name\_c.c)</span></span>
-   <span data-ttu-id="f83be-123">Código auxiliar de servidor (name \_ s. c)</span><span class="sxs-lookup"><span data-stu-id="f83be-123">Server stub (name\_s.c)</span></span>
-   <span data-ttu-id="f83be-124">Archivo de encabezado (Name. h)</span><span class="sxs-lookup"><span data-stu-id="f83be-124">Header file (name.h)</span></span>

<span data-ttu-id="f83be-125">Cuando el atributo de [**objeto**](object.md) aparece en la lista de atributos de interfaz, el compilador genera los siguientes archivos para una interfaz com:</span><span class="sxs-lookup"><span data-stu-id="f83be-125">When the [**object**](object.md) attribute appears in the interface attribute list, the compiler generates the following files for a COM interface:</span></span>

-   <span data-ttu-id="f83be-126">Archivo de proxy de interfaz (nombre \_ p. c)</span><span class="sxs-lookup"><span data-stu-id="f83be-126">Interface proxy file (name\_p.c)</span></span>
-   <span data-ttu-id="f83be-127">Archivo de encabezado de interfaz (Name. h)</span><span class="sxs-lookup"><span data-stu-id="f83be-127">Interface header file (name.h)</span></span>
-   <span data-ttu-id="f83be-128">Archivo UUID de interfaz (nombre \_ I. c)</span><span class="sxs-lookup"><span data-stu-id="f83be-128">Interface UUID file (name\_I.c)</span></span>

<span data-ttu-id="f83be-129">Cuando el atributo [**local**](local.md) aparece en la lista de atributos de interfaz, el compilador genera solo el archivo de encabezado de interfaz, Name. h.</span><span class="sxs-lookup"><span data-stu-id="f83be-129">When the [**local**](local.md) attribute appears in the interface attribute list, the compiler generates only the interface header file, Name.h.</span></span>

<span data-ttu-id="f83be-130">El compilador MIDL proporcionado con Microsoft RPC invoca el preprocesador de C según sea necesario para procesar el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f83be-130">The MIDL compiler provided with Microsoft RPC invokes the C preprocessor as needed to process the IDL file.</span></span> <span data-ttu-id="f83be-131">No invoca automáticamente el compilador de C para compilar los archivos generados.</span><span class="sxs-lookup"><span data-stu-id="f83be-131">It does not automatically invoke the C compiler to compile generated files.</span></span>

> [!Note]  
> <span data-ttu-id="f83be-132">El compilador MIDL proporcionado con Microsoft RPC utiliza una sintaxis de línea de comandos diferente de la del compilador de DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="f83be-132">The MIDL compiler provided with Microsoft RPC uses a different command-line syntax than the DCE IDL compiler.</span></span>

 

<span data-ttu-id="f83be-133">El compilador MIDL cambia [**/env**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)y [**/out**](-out.md) afectan al archivo de código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="f83be-133">The MIDL compiler switches [**/env**](-env.md), [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

<span data-ttu-id="f83be-134">A partir de la versión 6.0.359 de MIDL, la opción de línea de comandos predeterminada para el  [](-robust.md)compilador MIDL es [**/Oicf**](-oi.md).</span><span class="sxs-lookup"><span data-stu-id="f83be-134">Starting with MIDL version 6.0.359, the default command line option for the MIDL compiler is [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md).</span></span> <span data-ttu-id="f83be-135">Para deshabilitar/Robust, especifique la opción [**/no \_ Robust**](-no-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="f83be-135">To disable /robust, specify the [**/no\_robust**](-no-robust.md) option.</span></span>

## <a name="the-header-file"></a><span data-ttu-id="f83be-136">El archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="f83be-136">The Header File</span></span>

<span data-ttu-id="f83be-137">El archivo de encabezado contiene definiciones de todos los tipos de datos y las operaciones declaradas en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f83be-137">The header file contains definitions of all the data types and operations declared in the IDL file.</span></span> <span data-ttu-id="f83be-138">El archivo de encabezado debe estar incluido en todos los módulos de aplicación que llaman a las operaciones definidas, implementan las operaciones definidas o manipulan los tipos definidos.</span><span class="sxs-lookup"><span data-stu-id="f83be-138">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="f83be-139">El compilador MIDL cambia [**/Header**](-header.md) y [**/out**](-out.md) afectan al archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="f83be-139">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




