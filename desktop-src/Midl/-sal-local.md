---
title: modificador/sal_local
description: El \_ conmutador local/sal dirige a MIDL para que también genere anotaciones sal para los parámetros de los métodos de interfaz marcados como \ local \. El modificador/sal también debe estar presente.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local modificador MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676291"
---
# <a name="sal_local-switch"></a><span data-ttu-id="a6636-105">\_conmutador local de/sal</span><span class="sxs-lookup"><span data-stu-id="a6636-105">/sal\_local switch</span></span>

<span data-ttu-id="a6636-106">El **conmutador \_ local/sal** dirige a MIDL para que también genere anotaciones sal para los parámetros de los métodos de interfaz marcados como [**\[ locales \]**](local.md).</span><span class="sxs-lookup"><span data-stu-id="a6636-106">The **/sal\_local** switch directs MIDL to also generate SAL annotations for parameters of interface methods marked [**\[local\]**](local.md).</span></span> <span data-ttu-id="a6636-107">El modificador [**/sal**](-sal.md) también debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="a6636-107">The [**/sal**](-sal.md) switch must also be present.</span></span>

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a><span data-ttu-id="a6636-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="a6636-108">Switch Options</span></span>

<span data-ttu-id="a6636-109">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a6636-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6636-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6636-110">Remarks</span></span>

<span data-ttu-id="a6636-111">Modifica el comportamiento del modificador [**/sal**](-sal.md) para proporcionar también anotaciones en los parámetros de los métodos de interfaz marcados con el atributo [**\[ local \]**](local.md) .</span><span class="sxs-lookup"><span data-stu-id="a6636-111">Modifies the behavior of the [**/sal**](-sal.md) switch to also provide annotations on the parameters of interface methods marked with the [**\[local\]**](local.md) attribute.</span></span> <span data-ttu-id="a6636-112">Utilice el atributo [**\[ Anotate \]**](annotate.md)para invalidar la anotación generada por MIDL con una cadena de anotación diferente.</span><span class="sxs-lookup"><span data-stu-id="a6636-112">Use the [**\[annotate\]**](annotate.md)attribute to override the MIDL-generated annotation with a different annotation string.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6636-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6636-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6636-114">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="a6636-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="a6636-115">**/sal**</span><span class="sxs-lookup"><span data-stu-id="a6636-115">**/sal**</span></span>](-sal.md)
</dt> <dt>

<span data-ttu-id="a6636-116">[**\[anotar\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="a6636-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




