---
title: /ZP (modificador)
description: El modificador/ZP es el mismo que el de la opción/Pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /ZP-modificador MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783695"
---
# <a name="zp-switch"></a><span data-ttu-id="39c76-104">/ZP (modificador)</span><span class="sxs-lookup"><span data-stu-id="39c76-104">/Zp switch</span></span>

<span data-ttu-id="39c76-105">El modificador **/ZP** es el mismo que el de la opción [**/Pack**](-pack.md) .</span><span class="sxs-lookup"><span data-stu-id="39c76-105">The **/Zp** switch is the same as the [**/pack**](-pack.md) option.</span></span>

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a><span data-ttu-id="39c76-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="39c76-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="39c76-107">*nivel de empaquetado \_*</span><span class="sxs-lookup"><span data-stu-id="39c76-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="39c76-108">Especifica el nivel de empaquetado de las estructuras en el sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="39c76-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="39c76-109">El valor de nivel de empaquetado se puede establecer en 1, 2, 4 u 8.</span><span class="sxs-lookup"><span data-stu-id="39c76-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39c76-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39c76-110">Remarks</span></span>

<span data-ttu-id="39c76-111">El modificador **/ZP** designa el nivel de empaquetado de las estructuras en el sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="39c76-111">The **/Zp** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="39c76-112">El valor de nivel de empaquetado corresponde al valor de la opción **/ZP** usado por el compilador de C/C++ de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39c76-112">The packing-level value corresponds to the **/Zp** option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="39c76-113">Para obtener más información, vea la documentación de programación de Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="39c76-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="39c76-114">Especifique el mismo nivel de empaquetado al invocar el compilador de MIDL y el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="39c76-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="39c76-115">El nivel de empaquetado predeterminado que se usa cuando no se especifica el modificador **/ZP** ni [**/Pack**](-pack.md) es 8 en todos los entornos de compilación.</span><span class="sxs-lookup"><span data-stu-id="39c76-115">The default packing level used when neither the **/Zp** nor [**/pack**](-pack.md) switch is specified is 8 in all build environments.</span></span>

> [!Note]  
> <span data-ttu-id="39c76-116">No use **/Zp1** o **/ZP2** en plataformas MIPS o Alpha y no use **/Zp4** o **/Zp8** en plataformas de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="39c76-116">Do not use **/Zp1** or **/Zp2** on MIPS or Alpha platforms and do not use **/Zp4** or **/Zp8** on 16-bit platforms.</span></span> <span data-ttu-id="39c76-117">En función del tipo de datos y la ubicación de memoria asignada por el compilador de C en tiempo de ejecución, esto puede dar lugar a una excepción de errores de alineación de datos en las plataformas de MIPS y Alpha.</span><span class="sxs-lookup"><span data-stu-id="39c76-117">Depending on the data type and memory location assigned by the C compiler at run time, this can result in a data misalignment exception on MIPS and Alpha platforms.</span></span> <span data-ttu-id="39c76-118">En las plataformas de MS-DOS, el compilador de C no garantizará la alineación en 4 u 8, por lo que la aplicación puede finalizar.</span><span class="sxs-lookup"><span data-stu-id="39c76-118">On MS-DOS platforms, the C compiler will not ensure the alignment at 4 or 8, and so the application may terminate.</span></span>

 

## <a name="examples"></a><span data-ttu-id="39c76-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="39c76-119">Examples</span></span>

<span data-ttu-id="39c76-120">**MIDL/Zp4 nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="39c76-120">**midl /Zp4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="39c76-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="39c76-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c76-122">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="39c76-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="39c76-123">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="39c76-123">**/pack**</span></span>](-pack.md)
</dt> </dl>

 

 




