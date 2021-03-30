---
title: modificador/msc_ver
description: El \_ modificador/MSC ver se usa para permitir que MIDL genere código que incluye optimizaciones para diferentes versiones de los compiladores de C/C++ de Microsoft.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver modificador MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904174"
---
# <a name="msc_ver-switch"></a><span data-ttu-id="d6c42-104">\_modificador de/MSC ver</span><span class="sxs-lookup"><span data-stu-id="d6c42-104">/msc\_ver switch</span></span>

<span data-ttu-id="d6c42-105">El modificador **/MSC \_ Ver** se usa para permitir que MIDL genere código que incluye optimizaciones para diferentes versiones de los compiladores de C/C++ de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d6c42-105">The **/msc\_ver** switch is used to allow MIDL to generate code that includes optimizations for different versions of Microsoft C/C++ compilers.</span></span>

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a><span data-ttu-id="d6c42-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="d6c42-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="d6c42-107">*número de versión \_*</span><span class="sxs-lookup"><span data-stu-id="d6c42-107">*version\_number*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c42-108">Especifica un número de versión entero del compilador Microsoft Visual C++ que se utilizará para compilar el cliente y el código auxiliar del servidor de la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="d6c42-108">Specifies an integer version number of the Microsoft Visual C++ compiler that will be used to compile the client and server stubs of the distributed application.</span></span> <span data-ttu-id="d6c42-109">El número de versión predeterminado es 1100, que corresponde a Visual C++ versión 5,0.</span><span class="sxs-lookup"><span data-stu-id="d6c42-109">The default version number is 1100, which corresponds to Visual C++ version 5.0.</span></span> <span data-ttu-id="d6c42-110">El número de versión 1200 corresponde a Visual C++ versión 6,0, etc.</span><span class="sxs-lookup"><span data-stu-id="d6c42-110">The version number 1200 corresponds to Visual C++ version 6.0, and so on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6c42-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6c42-111">Remarks</span></span>

<span data-ttu-id="d6c42-112">En concreto, los valores de versión de 1100 o superior hacen que el compilador de MIDL genere código mediante la directiva **\_ \_ declspec (UUID ())** .</span><span class="sxs-lookup"><span data-stu-id="d6c42-112">In particular, version values of 1100 or greater cause the MIDL compiler to generate code utilizing the **\_\_declspec(uuid())** directive.</span></span> <span data-ttu-id="d6c42-113">También activa macros que usan las directivas **\_ \_ declspec (selectany)** y **\_ \_ declspec (novtable)** .</span><span class="sxs-lookup"><span data-stu-id="d6c42-113">It also activates macros that use the **\_\_declspec(selectany)** and **\_\_declspec(novtable)** directives.</span></span>

 

 




