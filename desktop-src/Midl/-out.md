---
title: /out (modificador)
description: El modificador/out especifica el directorio predeterminado donde el compilador MIDL escribe los archivos de salida.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- /out (modificador) MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676317"
---
# <a name="out-switch"></a><span data-ttu-id="f7d5f-104">/out (modificador)</span><span class="sxs-lookup"><span data-stu-id="f7d5f-104">/out switch</span></span>

<span data-ttu-id="f7d5f-105">El modificador **/out** especifica el directorio predeterminado donde el compilador MIDL escribe los archivos de salida.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-105">The **/out** switch specifies the default directory where the MIDL compiler writes output files.</span></span>

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a><span data-ttu-id="f7d5f-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="f7d5f-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="f7d5f-107">*Especificación de ruta de acceso*</span><span class="sxs-lookup"><span data-stu-id="f7d5f-107">*path-specification*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d5f-108">Especifica la ruta de acceso al directorio en el que se generan los archivos stub, header y switch.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-108">Specifies the path to the directory in which the stub, header, and switch files are generated.</span></span> <span data-ttu-id="f7d5f-109">Se puede especificar una especificación de unidad, una ruta de acceso absoluta al directorio o ambos.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-109">A drive specification, an absolute directory path, or both can be specified.</span></span> <span data-ttu-id="f7d5f-110">Las rutas de acceso se pueden entrecomillar explícitamente mediante comillas dobles (") para evitar que el shell interprete los caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-110">Paths can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7d5f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7d5f-111">Remarks</span></span>

<span data-ttu-id="f7d5f-112">El directorio de salida se puede especificar con una letra de unidad, un nombre de ruta de acceso absoluta o ambos.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-112">The output directory can be specified with a drive letter, an absolute path name, or both.</span></span> <span data-ttu-id="f7d5f-113">La opción **/out** se puede usar con cualquiera de los modificadores que habilitan la especificación de archivo de salida individual.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-113">The **/out** option can be used with any of the switches that enable individual output file specification.</span></span>

<span data-ttu-id="f7d5f-114">Cuando no se especifica el modificador **/out** , los archivos se escriben en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-114">When the **/out** switch is not specified, files are written to the current directory.</span></span>

<span data-ttu-id="f7d5f-115">El directorio predeterminado especificado por el modificador **/out** puede reemplazarse por un nombre de ruta de acceso explícito especificado como parte del modificador [**/cstub**](-cstub.md), [**/Header**](-header.md), [**/proxy**](-proxy.md)o [**/sstub**](-sstub.md) .</span><span class="sxs-lookup"><span data-stu-id="f7d5f-115">The default directory specified by the **/out** switch can be overridden by an explicit path name specified as part of the [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md), or [**/sstub**](-sstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="f7d5f-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f7d5f-116">Examples</span></span>

<span data-ttu-id="f7d5f-117">**MIDL/out c: \\ myDir \\ mysubdir \\ subdir2 más profundo nombre de archivo. idl**</span><span class="sxs-lookup"><span data-stu-id="f7d5f-117">**midl /out c:\\mydir\\mysubdir\\subdir2 deeper filename.idl**</span></span>

<span data-ttu-id="f7d5f-118">**MIDL/out c: nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="f7d5f-118">**midl /out c: filename.idl**</span></span>

<span data-ttu-id="f7d5f-119">**MIDL/out \\ myDir \\ mysubdir \\ otro nombre de archivo. idl**</span><span class="sxs-lookup"><span data-stu-id="f7d5f-119">**midl /out \\mydir\\mysubdir\\another filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="f7d5f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7d5f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d5f-121">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="f7d5f-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f7d5f-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="f7d5f-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="f7d5f-123">**/header**</span><span class="sxs-lookup"><span data-stu-id="f7d5f-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="f7d5f-124">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="f7d5f-124">**/proxy**</span></span>](-proxy.md)
</dt> <dt>

[<span data-ttu-id="f7d5f-125">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="f7d5f-125">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




