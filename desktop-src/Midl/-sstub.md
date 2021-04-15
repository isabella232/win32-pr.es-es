---
title: modificador/sstub
description: El modificador/sstub especifica el nombre del archivo de código auxiliar del servidor para una interfaz RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub modificador MIDL
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676314"
---
# <a name="sstub-switch"></a><span data-ttu-id="386f7-104">modificador/sstub</span><span class="sxs-lookup"><span data-stu-id="386f7-104">/sstub switch</span></span>

<span data-ttu-id="386f7-105">El modificador **/sstub** especifica el nombre del archivo de código auxiliar del servidor para una interfaz RPC.</span><span class="sxs-lookup"><span data-stu-id="386f7-105">The **/sstub** switch specifies the name of the server stub file for an RPC interface.</span></span>

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="386f7-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="386f7-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="386f7-107">*\_nombre del archivo de código auxiliar \_*</span><span class="sxs-lookup"><span data-stu-id="386f7-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="386f7-108">Especifica un nombre de archivo que invalida el nombre del archivo de código auxiliar del servidor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="386f7-108">Specifies a file name that overrides the default server stub file name.</span></span> <span data-ttu-id="386f7-109">Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete los caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="386f7-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="386f7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="386f7-110">Remarks</span></span>

<span data-ttu-id="386f7-111">El nombre de archivo especificado reemplaza el nombre de archivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="386f7-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="386f7-112">De forma predeterminada, el nombre de archivo se obtiene agregando \_ S. C al nombre del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="386f7-112">By default, the file name is obtained by adding \_S.C to the name of the IDL file.</span></span> <span data-ttu-id="386f7-113">Este modificador no afecta a las interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="386f7-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="386f7-114">Cuando se importan archivos, el nombre de archivo especificado se aplica a un solo archivo de código auxiliar: el archivo de código auxiliar que corresponde al archivo IDL especificado en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="386f7-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="386f7-115">Si *el \_ \_ nombre del archivo stub* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el modificador [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="386f7-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="386f7-116">Una ruta de acceso explícita en el *\_ \_ nombre de archivo de código auxiliar* invalida la especificación del modificador **/out** .</span><span class="sxs-lookup"><span data-stu-id="386f7-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="386f7-117">El modificador none de **/Server** tiene prioridad sobre el modificador **/sstub**</span><span class="sxs-lookup"><span data-stu-id="386f7-117">The **/server** none switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="386f7-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="386f7-118">Examples</span></span>

<span data-ttu-id="386f7-119">**/sstub MIDL My \_ sstub. c nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="386f7-119">**midl /sstub my\_sstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="386f7-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="386f7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="386f7-121">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="386f7-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="386f7-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="386f7-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="386f7-123">**/header**</span><span class="sxs-lookup"><span data-stu-id="386f7-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="386f7-124">**/out**</span><span class="sxs-lookup"><span data-stu-id="386f7-124">**/out**</span></span>](-out.md)
</dt> </dl>

 

 




