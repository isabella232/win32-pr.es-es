---
title: /Client (modificador)
description: El modificador/Client indica al compilador de MIDL que genere archivos de origen de C del lado cliente para una interfaz RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- parámetro/Client del modificador MIDL
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358247"
---
# <a name="client-switch"></a><span data-ttu-id="d3ff6-104">/Client (modificador)</span><span class="sxs-lookup"><span data-stu-id="d3ff6-104">/client switch</span></span>

<span data-ttu-id="d3ff6-105">El modificador **/Client** indica al compilador de MIDL que genere archivos de origen de C del lado cliente para una interfaz RPC.</span><span class="sxs-lookup"><span data-stu-id="d3ff6-105">The **/client** switch directs the MIDL compiler to generate client-side C source files for an RPC interface.</span></span>

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="d3ff6-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="d3ff6-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="d3ff6-107"><span id="stub"></span><span id="STUB"></span>código auxiliar \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d3ff6-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d3ff6-108">Genera los archivos del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="d3ff6-108">Generates the client-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="d3ff6-109"><span id="none"></span><span id="NONE"></span>ninguno \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d3ff6-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d3ff6-110">No genera ningún archivo del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="d3ff6-110">Does not generate any client-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3ff6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3ff6-111">Remarks</span></span>

<span data-ttu-id="d3ff6-112">Cuando no se especifica el modificador **/Client** , el compilador MIDL genera el archivo de código auxiliar del cliente.</span><span class="sxs-lookup"><span data-stu-id="d3ff6-112">When the **/client** switch is not specified, the MIDL compiler generates the client stub file.</span></span> <span data-ttu-id="d3ff6-113">Este modificador no afecta a las interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="d3ff6-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="d3ff6-114">El modificador **/Client** tiene prioridad sobre el modificador [**/cstub**](-cstub.md)</span><span class="sxs-lookup"><span data-stu-id="d3ff6-114">The **/client** switch takes precedence over the [**/cstub**](-cstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="d3ff6-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d3ff6-115">Examples</span></span>

<span data-ttu-id="d3ff6-116">**MIDL/Client None nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="d3ff6-116">**midl /client none filename.idl**</span></span>

<span data-ttu-id="d3ff6-117">**archivo de código auxiliar de MIDL. idl**</span><span class="sxs-lookup"><span data-stu-id="d3ff6-117">**midl /client stub filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="d3ff6-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3ff6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ff6-119">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="d3ff6-119">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="d3ff6-120">**/Server**</span><span class="sxs-lookup"><span data-stu-id="d3ff6-120">**/server**</span></span>](-server.md)
</dt> <dt>

[<span data-ttu-id="d3ff6-121">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="d3ff6-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




