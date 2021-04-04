---
title: modificador/h
description: La opción/h es equivalente funcionalmente a la opción/header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h (modificador) MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076845"
---
# <a name="h-switch"></a><span data-ttu-id="214d2-104">modificador/h</span><span class="sxs-lookup"><span data-stu-id="214d2-104">/h switch</span></span>

<span data-ttu-id="214d2-105">La opción **/h** es equivalente funcionalmente a la opción [**/Header**](-header.md) .</span><span class="sxs-lookup"><span data-stu-id="214d2-105">The **/h** option is functionally equivalent to the [**/header**](-header.md) option.</span></span>

``` syntax
midl /h filename
```

## <a name="switch-options"></a><span data-ttu-id="214d2-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="214d2-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="214d2-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="214d2-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="214d2-108">Especifica un nombre de archivo de encabezado que invalida el nombre de archivo de encabezado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="214d2-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="214d2-109">Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="214d2-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="214d2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="214d2-110">Remarks</span></span>

<span data-ttu-id="214d2-111">El modificador **/h** especifica *filename* como el nombre de un archivo de encabezado que contiene todas las definiciones incluidas en el archivo IDL, sin la sintaxis IDL.</span><span class="sxs-lookup"><span data-stu-id="214d2-111">The **/h** switch specifies *filename* as the name for a header file that contains all the definitions contained in the IDL file, without the IDL syntax.</span></span> <span data-ttu-id="214d2-112">Este archivo se puede usar como un archivo de encabezado de C o C++.</span><span class="sxs-lookup"><span data-stu-id="214d2-112">This file can be used as a C or C++ header file.</span></span>

## <a name="examples"></a><span data-ttu-id="214d2-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="214d2-113">Examples</span></span>

<span data-ttu-id="214d2-114">**MIDL/h tlibhead. h nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="214d2-114">**midl /h tlibhead.h filename.idl**</span></span>

<span data-ttu-id="214d2-115">**MIDL/h "MIDL. h" FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="214d2-115">**midl /h "midl.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="214d2-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="214d2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214d2-117">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="214d2-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="214d2-118">**/header**</span><span class="sxs-lookup"><span data-stu-id="214d2-118">**/header**</span></span>](-header.md)
</dt> </dl>

 

 




