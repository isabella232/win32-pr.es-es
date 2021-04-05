---
title: modificador/IID
description: El modificador/IID especifica el nombre del archivo de identificador de interfaz para una interfaz COM, invalidando el nombre predeterminado obtenido agregando \_ i. c al nombre de archivo IDL.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- /IID modificador MIDL
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419648"
---
# <a name="iid-switch"></a><span data-ttu-id="11aa2-104">modificador/IID</span><span class="sxs-lookup"><span data-stu-id="11aa2-104">/iid switch</span></span>

<span data-ttu-id="11aa2-105">El modificador **/IID** especifica el nombre del archivo de identificador de interfaz para una interfaz com, invalidando el nombre predeterminado obtenido agregando \_ i. c al nombre de archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="11aa2-105">The **/iid** switch specifies the name of the interface identifier file for a COM interface, overriding the default name obtained by adding \_i.c to the IDL file name.</span></span>

``` syntax
midl /iid filename
```

## <a name="switch-options"></a><span data-ttu-id="11aa2-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="11aa2-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="11aa2-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="11aa2-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="11aa2-108">Especifica un nombre de archivo de identificador de interfaz que invalida el nombre de archivo del identificador de interfaz predeterminado para una interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="11aa2-108">Specifies an interface identifier file name that overrides the default interface identifier file name for a COM interface.</span></span> <span data-ttu-id="11aa2-109">Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete los caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="11aa2-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11aa2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11aa2-110">Remarks</span></span>

<span data-ttu-id="11aa2-111">El modificador **/IID** no afecta a las interfaces RPC.</span><span class="sxs-lookup"><span data-stu-id="11aa2-111">The **/iid** switch does not affect RPC interfaces.</span></span>

<span data-ttu-id="11aa2-112">Si *filename* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el modificador [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="11aa2-112">If *filename* does not include an explicit path, the file is written to the current directory or to the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="11aa2-113">Una ruta de acceso explícita en *filename* invalida la especificación del modificador **/out** .</span><span class="sxs-lookup"><span data-stu-id="11aa2-113">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="11aa2-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="11aa2-114">Examples</span></span>

<span data-ttu-id="11aa2-115">**/IID de MIDL "My \_ IID. c" FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="11aa2-115">**midl /iid "my\_iid.c" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="11aa2-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="11aa2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11aa2-117">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="11aa2-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="11aa2-118">**/header**</span><span class="sxs-lookup"><span data-stu-id="11aa2-118">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="11aa2-119">**/out**</span><span class="sxs-lookup"><span data-stu-id="11aa2-119">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="11aa2-120">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="11aa2-120">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




