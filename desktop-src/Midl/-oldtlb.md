---
title: modificador/oldtlb
description: El modificador/oldtlb indica al compilador de MIDL que genere una biblioteca de tipos de formato antiguo.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- /oldtlb modificador MIDL
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420599"
---
# <a name="oldtlb-switch"></a><span data-ttu-id="6db71-104">modificador/oldtlb</span><span class="sxs-lookup"><span data-stu-id="6db71-104">/oldtlb switch</span></span>

<span data-ttu-id="6db71-105">El modificador **/oldtlb** indica al compilador de MIDL que genere una biblioteca de tipos de formato antiguo.</span><span class="sxs-lookup"><span data-stu-id="6db71-105">The **/oldtlb** switch directs the MIDL compiler to generate an old-format type library.</span></span>

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a><span data-ttu-id="6db71-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="6db71-106">Switch Options</span></span>

<span data-ttu-id="6db71-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6db71-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="6db71-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6db71-108">Remarks</span></span>

<span data-ttu-id="6db71-109">El modificador **/oldtlb** invalida el valor predeterminado y dirige el compilador MIDL para generar bibliotecas de tipos de formato antiguo incluso en las versiones actuales de Windows mediante [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) en lugar de [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span><span class="sxs-lookup"><span data-stu-id="6db71-109">The **/oldtlb** switch overrides the default and directs the MIDL compiler to generate old-format type libraries even on current versions of Windows by using [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) instead of [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span></span>

## <a name="examples"></a><span data-ttu-id="6db71-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6db71-110">Examples</span></span>

<span data-ttu-id="6db71-111">**MIDL/oldtlb nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="6db71-111">**midl /oldtlb filename.idl**</span></span>

<span data-ttu-id="6db71-112">**/oldtlb myoldodl. ODL de MIDL**</span><span class="sxs-lookup"><span data-stu-id="6db71-112">**midl /oldtlb myoldodl.odl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6db71-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="6db71-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db71-114">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="6db71-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6db71-115">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="6db71-115">**/newtlb**</span></span>](-newtlb.md)
</dt> </dl>

 

 