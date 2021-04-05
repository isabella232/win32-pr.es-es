---
title: modificador/Pack
description: El modificador/Pack es el mismo que el de la opción/ZP.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- /Pack modificador MIDL
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076868"
---
# <a name="pack-switch"></a><span data-ttu-id="bf3dc-104">modificador/Pack</span><span class="sxs-lookup"><span data-stu-id="bf3dc-104">/pack switch</span></span>

<span data-ttu-id="bf3dc-105">El modificador **/Pack** es el mismo que el de la opción [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="bf3dc-105">The **/pack** switch is the same as the [**/Zp**](-zp.md) option.</span></span>

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a><span data-ttu-id="bf3dc-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="bf3dc-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="bf3dc-107">*nivel de empaquetado \_*</span><span class="sxs-lookup"><span data-stu-id="bf3dc-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="bf3dc-108">Especifica el nivel de empaquetado de las estructuras en el sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="bf3dc-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="bf3dc-109">El valor de nivel de empaquetado se puede establecer en 1, 2, 4 u 8.</span><span class="sxs-lookup"><span data-stu-id="bf3dc-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf3dc-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf3dc-110">Remarks</span></span>

<span data-ttu-id="bf3dc-111">El modificador **/Pack** designa el nivel de empaquetado de las estructuras en el sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="bf3dc-111">The **/pack** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="bf3dc-112">El valor de nivel de empaquetado corresponde al valor de la opción [**/ZP**](-zp.md) usado por el compilador de Microsoft C/C++ versión 7,0.</span><span class="sxs-lookup"><span data-stu-id="bf3dc-112">The packing-level value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ version 7.0 compiler.</span></span> <span data-ttu-id="bf3dc-113">Para obtener más información, vea la documentación de programación de Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="bf3dc-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="bf3dc-114">Especifique el mismo nivel de empaquetado al invocar el compilador de MIDL y el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="bf3dc-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span> <span data-ttu-id="bf3dc-115">El nivel de empaquetado predeterminado que se usa cuando no se especifica el modificador [**/ZP**](-zp.md) ni **/Pack** es 8, en todos los entornos de compilación.</span><span class="sxs-lookup"><span data-stu-id="bf3dc-115">The default packing level used when neither the [**/Zp**](-zp.md) nor **/pack** switch is specified is 8, in both all build environments.</span></span>

<span data-ttu-id="bf3dc-116">Para obtener una explicación de los posibles peligros en el uso de niveles de empaquetado no estándar, vea el tema de ayuda de [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="bf3dc-116">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="bf3dc-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bf3dc-117">Examples</span></span>

<span data-ttu-id="bf3dc-118">**MIDL/Pack 2 nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="bf3dc-118">**midl /pack 2 filename.idl**</span></span>

<span data-ttu-id="bf3dc-119">**MIDL/Pack 8 bar. idl**</span><span class="sxs-lookup"><span data-stu-id="bf3dc-119">**midl /pack 8 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="bf3dc-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf3dc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf3dc-121">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="bf3dc-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="bf3dc-122">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="bf3dc-122">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="bf3dc-123">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="bf3dc-123">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




