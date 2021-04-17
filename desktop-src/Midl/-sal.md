---
title: modificador/sal
description: El modificador/sal indica a MIDL que genere anotaciones SAL en los archivos de código auxiliar generados.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- /sal modificador MIDL
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651334"
---
# <a name="sal-switch"></a><span data-ttu-id="7fca8-104">modificador/sal</span><span class="sxs-lookup"><span data-stu-id="7fca8-104">/sal switch</span></span>

<span data-ttu-id="7fca8-105">El modificador **/sal** indica a MIDL que genere anotaciones sal en los archivos de código auxiliar generados.</span><span class="sxs-lookup"><span data-stu-id="7fca8-105">The **/sal** switch directs MIDL to generate SAL annotations in the generated stub files.</span></span>

``` syntax
midl /sal
```

## <a name="switch-options"></a><span data-ttu-id="7fca8-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="7fca8-106">Switch Options</span></span>

<span data-ttu-id="7fca8-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7fca8-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fca8-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fca8-108">Remarks</span></span>

<span data-ttu-id="7fca8-109">MIDL marcará los parámetros de puntero y matriz con anotaciones que reflejen la descripción del parámetro en el archivo IDL tal y como se aplica mediante RPC y el motor de serialización de NDR.</span><span class="sxs-lookup"><span data-stu-id="7fca8-109">MIDL will mark pointer and array parameters with annotations that reflect the parameter description in the IDL file as enforced by RPC and the NDR marshaling engine.</span></span> <span data-ttu-id="7fca8-110">MIDL no crea anotaciones para los parámetros de los métodos de interfaz marcados con el atributo [**\[ local \]**](local.md)a menos que [**/sal \_ local**](-sal-local.md) también esté presente en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="7fca8-110">MIDL does not create annotations for parameters in interface methods marked with the [**\[local\]**](local.md)attribute unless [**/sal\_local**](-sal-local.md) is also present on the command line.</span></span> <span data-ttu-id="7fca8-111">Para reemplazar la anotación generada por MIDL, utilice el atributo [**\[ Anotate \]**](annotate.md) .</span><span class="sxs-lookup"><span data-stu-id="7fca8-111">To override the MIDL-generated annotation, use the [**\[annotate\]**](annotate.md) attribute.</span></span>

<span data-ttu-id="7fca8-112">Las anotaciones generadas por MIDL siempre tienen el prefijo \_ \_ RPC \_ y requieren el uso del encabezado **rpcsal. h** para traducir la anotación en anotaciones de sal estándar.</span><span class="sxs-lookup"><span data-stu-id="7fca8-112">MIDL-generated annotations are always prefixed with \_\_RPC\_, and require use of the **rpcsal.h** header to translate the annotation into standard SAL annotations.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fca8-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fca8-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fca8-114">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="7fca8-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="7fca8-115">**/sal \_ local**</span><span class="sxs-lookup"><span data-stu-id="7fca8-115">**/sal\_local**</span></span>](-sal-local.md)
</dt> <dt>

<span data-ttu-id="7fca8-116">[**\[anotar\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="7fca8-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




