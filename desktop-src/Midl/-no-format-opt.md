---
title: modificador/no_format_opt
description: El \_ modificador de formato/no \_ cambia la manera en que MIDL optimiza el tipo y los descriptores de procedimiento.
ms.assetid: 721ac828-7b47-4991-8bce-f9babf6c77a8
keywords:
- /no_format_opt modificador MIDL
topic_type:
- apiref
api_name:
- /no_format_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d6e54b963c9637c4f5a583fc9d8f44a0f2880e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685658"
---
# <a name="no_format_opt-switch"></a><span data-ttu-id="824ba-104">\_modificador de formato/no \_</span><span class="sxs-lookup"><span data-stu-id="824ba-104">/no\_format\_opt switch</span></span>

<span data-ttu-id="824ba-105">El modificador de **\_ formato \_ /no** cambia la manera en que MIDL optimiza el tipo y los descriptores de procedimiento.</span><span class="sxs-lookup"><span data-stu-id="824ba-105">The **/no\_format\_opt** switch changes the way MIDL optimizes type and procedure descriptors.</span></span>

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a><span data-ttu-id="824ba-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="824ba-106">Switch Options</span></span>

<span data-ttu-id="824ba-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="824ba-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="824ba-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="824ba-108">Remarks</span></span>

<span data-ttu-id="824ba-109">De forma predeterminada, MIDL elimina los descriptores de tipos y procedimientos duplicados con el fin de reducir el tamaño del código auxiliar generado.</span><span class="sxs-lookup"><span data-stu-id="824ba-109">By default, MIDL eliminates duplicate type and procedure descriptors in order to reduce the size of the generated stub code.</span></span> <span data-ttu-id="824ba-110">El uso del modificador del **\_ \_ formato/no** desactiva este comportamiento de optimización.</span><span class="sxs-lookup"><span data-stu-id="824ba-110">Using the **/no\_format\_opt** switch turns off this optimizing behavior.</span></span>

## <a name="examples"></a><span data-ttu-id="824ba-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="824ba-111">Examples</span></span>

<span data-ttu-id="824ba-112">**formato MIDL \_ /no \_ OPT. idl**</span><span class="sxs-lookup"><span data-stu-id="824ba-112">**midl /no\_format\_opt mylean.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="824ba-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="824ba-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824ba-114">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="824ba-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="824ba-115">**/OI**</span><span class="sxs-lookup"><span data-stu-id="824ba-115">**/Oi**</span></span>](-oi.md)
</dt> </dl>

 

 




