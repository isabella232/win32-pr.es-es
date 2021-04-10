---
title: modificador/ACF
description: El modificador/ACF permite al usuario proporcionar un nombre de archivo ACF explícito. El modificador también permite el uso de diferentes nombres de interfaz en los archivos IDL y ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /ACF modificador MIDL
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994753"
---
# <a name="acf-switch"></a><span data-ttu-id="fc3cb-105">modificador/ACF</span><span class="sxs-lookup"><span data-stu-id="fc3cb-105">/acf switch</span></span>

<span data-ttu-id="fc3cb-106">El modificador **/ACF** permite al usuario proporcionar un nombre de archivo ACF explícito.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-106">The **/acf** switch allows the user to supply an explicit ACF file name.</span></span> <span data-ttu-id="fc3cb-107">El modificador también permite el uso de diferentes nombres de interfaz en los archivos IDL y ACF.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-107">The switch also allows the use of different interface names in the IDL and ACF files.</span></span>

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a><span data-ttu-id="fc3cb-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="fc3cb-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="fc3cb-109">*\_archivo ACF*</span><span class="sxs-lookup"><span data-stu-id="fc3cb-109">*acf\_filename*</span></span> 
</dt> <dd>

<span data-ttu-id="fc3cb-110">Especifica el nombre del ACF.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-110">Specifies the name of the ACF.</span></span> <span data-ttu-id="fc3cb-111">El espacio en blanco puede estar o no estar presente entre el modificador **/ACF** y el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-111">White space may or may not be present between the **/acf** switch and the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc3cb-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc3cb-112">Remarks</span></span>

<span data-ttu-id="fc3cb-113">De forma predeterminada, el compilador MIDL crea el nombre de ACF reemplazando la extensión de nombre de archivo IDL (normalmente. idl) por. ACF.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-113">By default, the MIDL compiler constructs the name of the ACF by replacing the IDL file name extension (usually .idl) with .acf.</span></span> <span data-ttu-id="fc3cb-114">Cuando el modificador **/ACF** está presente, el ACF toma el nombre del nombre de archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-114">When the **/acf** switch is present, the ACF takes its name from the specified file name.</span></span> <span data-ttu-id="fc3cb-115">El modificador **/ACF** solo se aplica al archivo IDL especificado en la línea de comandos del compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-115">The **/acf** switch applies only to the IDL file specified on the MIDL compiler command line.</span></span> <span data-ttu-id="fc3cb-116">No se aplica a los archivos importados.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-116">It does not apply to imported files.</span></span>

<span data-ttu-id="fc3cb-117">Cuando se usa el modificador **/ACF** , no es necesario que el nombre de la interfaz de ACF coincida con el nombre de la interfaz MIDL.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-117">When the **/acf** switch is used, the interface name in the ACF need not match the MIDL interface name.</span></span> <span data-ttu-id="fc3cb-118">Esta característica permite a las interfaces compartir una especificación ACF.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-118">This feature allows interfaces to share an ACF specification.</span></span>

<span data-ttu-id="fc3cb-119">Cuando no se especifica una ruta de acceso absoluta a un ACF, el compilador MIDL busca en el directorio actual, en los directorios proporcionados por la opción [**/i**](-i.md) y en los directorios de la ruta de acceso de inclusión.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-119">When an absolute path to an ACF is not specified, the MIDL compiler searches in the current directory, directories supplied by the [**/I**](-i.md) option, and directories in the INCLUDE path.</span></span>

<span data-ttu-id="fc3cb-120">Si no se encuentra el ACF, el compilador MIDL supone que no hay ningún ACF para esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="fc3cb-120">If the ACF is not found, the MIDL compiler assumes there is no ACF for this interface.</span></span> <span data-ttu-id="fc3cb-121">Para obtener más información acerca de la secuencia de directorios, consulte las entradas de referencia de los modificadores [**/i**](-i.md) y [**/no \_ Def \_ Idir**](-no-def-idir.md)</span><span class="sxs-lookup"><span data-stu-id="fc3cb-121">For more information about the sequence of directories, see the reference entries for the [**/I**](-i.md) and [**/no\_def\_idir**](-no-def-idir.md) switches.</span></span> <span data-ttu-id="fc3cb-122">Para obtener más información relacionada con **/ACF**, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="fc3cb-122">For more information relating to **/acf**, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fc3cb-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fc3cb-123">Examples</span></span>

<span data-ttu-id="fc3cb-124">**MIDL/ACF bar. ACF nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="fc3cb-124">**midl /acf bar.acf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="fc3cb-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc3cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc3cb-126">**/I**</span><span class="sxs-lookup"><span data-stu-id="fc3cb-126">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="fc3cb-127">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="fc3cb-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="fc3cb-128">**/no \_ Def \_ Idir**</span><span class="sxs-lookup"><span data-stu-id="fc3cb-128">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




