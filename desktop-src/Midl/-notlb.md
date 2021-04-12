---
title: modificador/notlb
description: El modificador/notlb evita que el compilador de MIDL genere un archivo de biblioteca de tipos (TLB).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb modificador MIDL
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487146"
---
# <a name="notlb-switch"></a><span data-ttu-id="0299b-104">modificador/notlb</span><span class="sxs-lookup"><span data-stu-id="0299b-104">/notlb switch</span></span>

<span data-ttu-id="0299b-105">El modificador **/notlb** evita que el compilador de MIDL genere un archivo de biblioteca de tipos (TLB).</span><span class="sxs-lookup"><span data-stu-id="0299b-105">The **/notlb** switch prevents the MIDL compiler from generating a type library (TLB) file.</span></span>

``` syntax
midl /notlb
```

## <a name="switch-options"></a><span data-ttu-id="0299b-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="0299b-106">Switch Options</span></span>

<span data-ttu-id="0299b-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0299b-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0299b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0299b-108">Remarks</span></span>

<span data-ttu-id="0299b-109">De forma predeterminada, el compilador MIDL generará un archivo TLB siempre que encuentre una instrucción [**Library**](library.md) .</span><span class="sxs-lookup"><span data-stu-id="0299b-109">By default, the MIDL compiler will generate a TLB file whenever it encounters a [**LIBRARY**](library.md) statement.</span></span> <span data-ttu-id="0299b-110">Este modificador invalida el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0299b-110">This switch overrides the default behavior.</span></span>

<span data-ttu-id="0299b-111">Cuando se especifica la opción **/notlb** , todos los demás códigos auxiliares, encabezados, etc. se generan como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="0299b-111">When the **/notlb** option is specified, all other stubs, headers, etc. are generated as usual.</span></span>

## <a name="see-also"></a><span data-ttu-id="0299b-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="0299b-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0299b-113">**/TLB**</span><span class="sxs-lookup"><span data-stu-id="0299b-113">**/tlb**</span></span>](-tlb.md)
</dt> </dl>

 

 




