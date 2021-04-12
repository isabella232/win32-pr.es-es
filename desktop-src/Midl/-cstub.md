---
title: modificador/cstub
description: El modificador/cstub especifica el nombre del archivo de código auxiliar de cliente para una interfaz RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub modificador MIDL
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358246"
---
# <a name="cstub-switch"></a><span data-ttu-id="56eb9-104">modificador/cstub</span><span class="sxs-lookup"><span data-stu-id="56eb9-104">/cstub switch</span></span>

<span data-ttu-id="56eb9-105">El modificador **/cstub** especifica el nombre del archivo de código auxiliar de cliente para una interfaz RPC.</span><span class="sxs-lookup"><span data-stu-id="56eb9-105">The **/cstub** switch specifies the name of the client stub file for an RPC interface.</span></span>

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="56eb9-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="56eb9-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="56eb9-107">*\_nombre del archivo de código auxiliar \_*</span><span class="sxs-lookup"><span data-stu-id="56eb9-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="56eb9-108">Especifica un nombre de archivo que invalida el nombre del archivo de código auxiliar de cliente predeterminado.</span><span class="sxs-lookup"><span data-stu-id="56eb9-108">Specifies a file name that overrides the default client stub file name.</span></span> <span data-ttu-id="56eb9-109">Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete los caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="56eb9-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56eb9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56eb9-110">Remarks</span></span>

<span data-ttu-id="56eb9-111">El nombre de archivo especificado reemplaza el nombre de archivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="56eb9-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="56eb9-112">De forma predeterminada, el nombre de archivo se obtiene agregando la extensión \_ c. c al nombre del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="56eb9-112">By default, the file name is obtained by adding the extension \_c.c to the name of the IDL file.</span></span> <span data-ttu-id="56eb9-113">Este modificador no afecta a las interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="56eb9-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="56eb9-114">Cuando se importan archivos, el nombre de archivo especificado se aplica a un solo archivo de código auxiliar: el archivo de código auxiliar que corresponde al archivo IDL especificado en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="56eb9-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="56eb9-115">Si *el \_ \_ nombre del archivo stub* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el modificador [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="56eb9-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="56eb9-116">Una ruta de acceso explícita en el *\_ \_ nombre de archivo de código auxiliar* invalida la especificación del modificador **/out** .</span><span class="sxs-lookup"><span data-stu-id="56eb9-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="56eb9-117">El modificador **/Client** no tiene prioridad sobre el modificador **/cstub**</span><span class="sxs-lookup"><span data-stu-id="56eb9-117">The **/client** none switch takes precedence over the **/cstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="56eb9-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="56eb9-118">Examples</span></span>

<span data-ttu-id="56eb9-119">**/cstub MIDL My \_ cstub. c nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="56eb9-119">**midl /cstub my\_cstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="56eb9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="56eb9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56eb9-121">**/header**</span><span class="sxs-lookup"><span data-stu-id="56eb9-121">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="56eb9-122">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="56eb9-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="56eb9-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="56eb9-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="56eb9-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="56eb9-124">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




