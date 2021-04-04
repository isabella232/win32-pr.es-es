---
title: modificador/Server
description: El modificador/Server indica al compilador de MIDL que genere archivos de origen de C del lado servidor para una interfaz RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- modificador de/Server (MIDL)
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076766"
---
# <a name="server-switch"></a><span data-ttu-id="50cc9-104">modificador/Server</span><span class="sxs-lookup"><span data-stu-id="50cc9-104">/server switch</span></span>

<span data-ttu-id="50cc9-105">El modificador **/Server** indica al compilador de MIDL que genere archivos de origen de C del lado servidor para una interfaz RPC.</span><span class="sxs-lookup"><span data-stu-id="50cc9-105">The **/server** switch directs the MIDL compiler to generate server-side C source files for an RPC interface.</span></span>

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="50cc9-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="50cc9-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="50cc9-107"><span id="stub"></span><span id="STUB"></span>código auxiliar \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="50cc9-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="50cc9-108">Genera los archivos del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="50cc9-108">Generates the server-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="50cc9-109"><span id="none"></span><span id="NONE"></span>ninguno \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="50cc9-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="50cc9-110">No genera archivos del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="50cc9-110">Does not generate server-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50cc9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50cc9-111">Remarks</span></span>

<span data-ttu-id="50cc9-112">Cuando no se especifica el modificador **/Server** , el compilador MIDL genera el archivo de código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="50cc9-112">When the **/server** switch is not specified, the MIDL compiler generates the server stub file.</span></span> <span data-ttu-id="50cc9-113">Este modificador no afecta a las interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="50cc9-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="50cc9-114">La opción **None** no hace que se generen archivos.</span><span class="sxs-lookup"><span data-stu-id="50cc9-114">The **none** option causes no files to be generated.</span></span>

<span data-ttu-id="50cc9-115">El modificador **/Server** tiene prioridad sobre el modificador **/sstub**</span><span class="sxs-lookup"><span data-stu-id="50cc9-115">The **/server** switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="50cc9-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="50cc9-116">Examples</span></span>

<span data-ttu-id="50cc9-117">**MIDL/Server None**</span><span class="sxs-lookup"><span data-stu-id="50cc9-117">**midl /server none**</span></span>

<span data-ttu-id="50cc9-118">**código auxiliar de MIDL/Server**</span><span class="sxs-lookup"><span data-stu-id="50cc9-118">**midl /server stub**</span></span>

## <a name="see-also"></a><span data-ttu-id="50cc9-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="50cc9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50cc9-120">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="50cc9-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="50cc9-121">**/Client**</span><span class="sxs-lookup"><span data-stu-id="50cc9-121">**/client**</span></span>](-client.md)
</dt> <dt>

[<span data-ttu-id="50cc9-122">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="50cc9-122">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




