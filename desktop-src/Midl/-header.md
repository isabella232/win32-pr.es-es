---
title: modificador/header
description: El modificador/header especifica el nombre del archivo de encabezado.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- /header modificador MIDL
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419650"
---
# <a name="header-switch"></a><span data-ttu-id="1c898-104">modificador/header</span><span class="sxs-lookup"><span data-stu-id="1c898-104">/header switch</span></span>

<span data-ttu-id="1c898-105">El modificador **/Header** especifica el nombre del archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="1c898-105">The **/header** switch specifies the name of the header file.</span></span>

``` syntax
midl /header filename
```

## <a name="switch-options"></a><span data-ttu-id="1c898-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="1c898-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="1c898-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="1c898-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="1c898-108">Especifica un nombre de archivo de encabezado que invalida el nombre de archivo de encabezado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1c898-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="1c898-109">Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="1c898-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c898-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c898-110">Remarks</span></span>

<span data-ttu-id="1c898-111">El nombre de archivo especificado reemplaza el nombre de archivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1c898-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="1c898-112">El nombre de archivo predeterminado se obtiene reemplazando la extensión de nombre de archivo IDL (normalmente,. idl) por la extensión de nombre de archivo. h.</span><span class="sxs-lookup"><span data-stu-id="1c898-112">The default file name is obtained by replacing the IDL file name extension (usually .idl) with the file name extension .h.</span></span> <span data-ttu-id="1c898-113">En el caso de las interfaces OLE, el modificador **/Header** invalida el nombre predeterminado del archivo de encabezado de interfaz.</span><span class="sxs-lookup"><span data-stu-id="1c898-113">For OLE interfaces, the **/header** switch overrides the default name of the interface header file.</span></span>

<span data-ttu-id="1c898-114">Cuando se importan archivos, el nombre de archivo especificado se aplica a un solo archivo de encabezado: el archivo de encabezado que corresponde al archivo IDL especificado en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="1c898-114">When you are importing files, the specified file name applies to only one header file — the header file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="1c898-115">Si *filename* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el modificador [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="1c898-115">If *filename* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="1c898-116">Una ruta de acceso explícita en *filename* invalida la especificación del modificador **/out** .</span><span class="sxs-lookup"><span data-stu-id="1c898-116">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="1c898-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1c898-117">Examples</span></span>

<span data-ttu-id="1c898-118">**MIDL/header "bar. h" nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="1c898-118">**midl /header "bar.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1c898-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c898-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c898-120">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="1c898-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1c898-121">**/h**</span><span class="sxs-lookup"><span data-stu-id="1c898-121">**/h**</span></span>](-h.md)
</dt> <dt>

[<span data-ttu-id="1c898-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="1c898-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="1c898-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="1c898-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="1c898-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="1c898-124">**/sstub**</span></span>](-sstub.md)
</dt> <dt>

[<span data-ttu-id="1c898-125">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="1c898-125">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




