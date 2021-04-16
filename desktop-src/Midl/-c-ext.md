---
title: modificador/c_ext
description: Este modificador está obsoleto a partir de la versión 3,0 del compilador de MIDL. Sin embargo, el uso del \_ modificador ext de c no generará un error del compilador, por lo que no tendrá que quitar las referencias a/MS \_ ext o/c \_ ext de un archivo make existente.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext modificador MIDL
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685654"
---
# <a name="c_ext-switch"></a><span data-ttu-id="204d9-105">/c ( \_ modificador ext)</span><span class="sxs-lookup"><span data-stu-id="204d9-105">/c\_ext switch</span></span>

<span data-ttu-id="204d9-106">Este modificador está obsoleto a partir de la versión 3,0 del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="204d9-106">This switch is obsolete as of version 3.0 of the MIDL compiler.</span></span> <span data-ttu-id="204d9-107">Sin embargo, el uso del modificador **\_ ext de c** no generará un error del compilador, por lo que no tendrá que quitar las referencias a [**/MS \_ ext**](-ms-ext.md) o **/c \_ ext** de un archivo make existente.</span><span class="sxs-lookup"><span data-stu-id="204d9-107">However, using the **c\_ext** switch will not generate a compiler error, so you do not have to remove references to [**/ms\_ext**](-ms-ext.md) or **/c\_ext** from an existing makefile.</span></span>

``` syntax
midl /c_ext
```

## <a name="switch-options"></a><span data-ttu-id="204d9-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="204d9-108">Switch Options</span></span>

<span data-ttu-id="204d9-109">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="204d9-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="204d9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="204d9-110">Remarks</span></span>

<span data-ttu-id="204d9-111">Las siguientes características están ahora disponibles de forma predeterminada:</span><span class="sxs-lookup"><span data-stu-id="204d9-111">The following features are now available by default:</span></span>

-   <span data-ttu-id="204d9-112">Muchos archivos de encabezado existentes definen tipos con calificadores, como **Far** y **Stdcall**, que no forman parte del IDL de DCE.</span><span class="sxs-lookup"><span data-stu-id="204d9-112">Many existing header files define types with qualifiers, such as **far** and **stdcall**, that are not part of the DCE IDL.</span></span> <span data-ttu-id="204d9-113">Esos compiladores (y el compilador de MIDL en modo de compatibilidad de DCE) generan errores al intentar procesar estos calificadores.</span><span class="sxs-lookup"><span data-stu-id="204d9-113">Those compilers (and the MIDL compiler in DCE-compatibility mode) generate errors when they attempt to process these qualifiers.</span></span> <span data-ttu-id="204d9-114">El compilador MIDL le permite compilar archivos IDL que contienen estos calificadores.</span><span class="sxs-lookup"><span data-stu-id="204d9-114">The MIDL compiler allows you to compile IDL files that contain these qualifiers.</span></span> <span data-ttu-id="204d9-115">Los calificadores de tipo no afectan a la manera en que se transmiten los datos en la red.</span><span class="sxs-lookup"><span data-stu-id="204d9-115">The type qualifiers do not affect the way the data is transmitted on the network.</span></span>
-   <span data-ttu-id="204d9-116">Puede omitir atributos direccionales como [**\[ in \]**](in.md) o [**\[ out \]**](out-idl.md).</span><span class="sxs-lookup"><span data-stu-id="204d9-116">You can omit directional attributes such as [**\[in\]**](in.md) or [**\[out\]**](out-idl.md).</span></span>

<span data-ttu-id="204d9-117">Las siguientes extensiones del lenguaje C se admiten en el modo predeterminado:</span><span class="sxs-lookup"><span data-stu-id="204d9-117">The following C-language extensions are supported in default mode:</span></span>

-   <span data-ttu-id="204d9-118">Campos de bits en estructuras y uniones</span><span class="sxs-lookup"><span data-stu-id="204d9-118">Bit fields in structures and unions</span></span>
-   <span data-ttu-id="204d9-119">Comentarios que comienzan con dos caracteres de barra diagonal (//)</span><span class="sxs-lookup"><span data-stu-id="204d9-119">Comments that start with two slash characters (//)</span></span>
-   <span data-ttu-id="204d9-120">Declaraciones externas</span><span class="sxs-lookup"><span data-stu-id="204d9-120">External declarations</span></span>
-   <span data-ttu-id="204d9-121">Procedimientos con puntos suspensivos en la lista de parámetros (...)</span><span class="sxs-lookup"><span data-stu-id="204d9-121">Procedures with ellipses in the parameter list (…)</span></span>
-   <span data-ttu-id="204d9-122">En las plataformas de 32 bits, [**int**](int.md) es un tipo base de 32 bits nativo; en las plataformas de 16 bits, se reconoce **int** pero no es un tipo utilizable de forma remota.</span><span class="sxs-lookup"><span data-stu-id="204d9-122">On 32-bit platforms, [**int**](int.md) is a native 32-bit base type; on 16-bit platforms, **int** is recognized but is not a remotable type</span></span>
-   <span data-ttu-id="204d9-123">Tipo [**void \***](void.md) que no se usa en operaciones remotas</span><span class="sxs-lookup"><span data-stu-id="204d9-123">Type [**void \***](void.md) that is not used in remote operations</span></span>
-   <span data-ttu-id="204d9-124">Los calificadores de tipo, incluido el formulario con el prefijo compatible con ANSI, contienen dos caracteres de subrayado: **Cdecl**, **\_ \_ Cdecl**, [**const**](const.md), **\_ \_ const**, **Export**, **\_ \_ Export**, **Far**, **\_ \_ Far**, **loadds**, **\_ \_ loadds**, **Near**, **\_ \_ Near**, **Pascal**, **\_ \_ Pascal**, **Stdcall**, **\_ \_ Stdcall**, **volatile** y **\_ \_ volatile**.</span><span class="sxs-lookup"><span data-stu-id="204d9-124">Type qualifiers—including the form with the ANSI-conformant prefix—contain two underscore characters: **cdecl**, **\_\_cdecl**, [**const**](const.md), **\_\_const**, **export**, **\_\_export**, **far**, **\_\_far**, **loadds**, **\_\_loadds**, **near**, **\_\_near**, **pascal**, **\_\_pascal**, **stdcall**, **\_\_stdcall**, **volatile**, and **\_\_volatile**.</span></span>

<span data-ttu-id="204d9-125">Para obtener más información acerca de los calificadores de declaración, vea la documentación de Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="204d9-125">For more information about declaration qualifiers, see your Microsoft C/C++ documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="204d9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="204d9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="204d9-127">**configuración de/APP \_**</span><span class="sxs-lookup"><span data-stu-id="204d9-127">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="204d9-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="204d9-128">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="204d9-129">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="204d9-129">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




