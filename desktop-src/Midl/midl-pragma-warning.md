---
title: midl_pragma atributo Warning
description: Use la \_ opción de advertencia pragma MIDL para invalidar temporalmente el comportamiento del mensaje de advertencia de MIDL en tiempo de compilación.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma el atributo de advertencia MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904014"
---
# <a name="midl_pragma-warning-attribute"></a><span data-ttu-id="6f315-104">\_pragma MIDL Warning (atributo)</span><span class="sxs-lookup"><span data-stu-id="6f315-104">midl\_pragma warning attribute</span></span>

<span data-ttu-id="6f315-105">Use la opción de **\_ ADVERTENCIA pragma MIDL** para invalidar temporalmente el comportamiento del mensaje de advertencia de MIDL en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="6f315-105">Use the **midl\_pragma warning** option to temporarily override MIDL's warning message behavior at compile time.</span></span>

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a><span data-ttu-id="6f315-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f315-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f315-107">*opción de advertencia \_*</span><span class="sxs-lookup"><span data-stu-id="6f315-107">*warning\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="6f315-108">La opción de advertencia puede ser una de las siguientes: deshabilitar, habilitar, valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6f315-108">The warning option can be one of the following: disable, enable, default.</span></span>

</dd> <dt>

<span data-ttu-id="6f315-109">*lista de mensajes \_*</span><span class="sxs-lookup"><span data-stu-id="6f315-109">*message\_list*</span></span> 
</dt> <dd>

<span data-ttu-id="6f315-110">Una lista de números de mensaje separados por espacios.</span><span class="sxs-lookup"><span data-stu-id="6f315-110">A list of message numbers separated by spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f315-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f315-111">Remarks</span></span>

<span data-ttu-id="6f315-112">La Directiva pragma se puede usar como una directiva pragma del compilador de C.</span><span class="sxs-lookup"><span data-stu-id="6f315-112">The pragma can be used like a C-compiler pragma.</span></span> <span data-ttu-id="6f315-113">Es decir, deshabilita, habilita o vuelve al comportamiento predeterminado de una advertencia de MIDL determinada.</span><span class="sxs-lookup"><span data-stu-id="6f315-113">That is, it disables, enables, or returns to the default behavior for a given MIDL warning.</span></span>

## <a name="examples"></a><span data-ttu-id="6f315-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6f315-114">Examples</span></span>

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a><span data-ttu-id="6f315-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f315-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f315-116">**pragma**</span><span class="sxs-lookup"><span data-stu-id="6f315-116">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




