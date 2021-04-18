---
title: /conmutador del sistema
description: El modificador/System indica al compilador de MIDL que genere una biblioteca de tipos para el sistema especificado. El valor predeterminado es el sistema operativo actual.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /modificador del sistema MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358145"
---
# <a name="system-switch"></a><span data-ttu-id="17f9b-105">/<system> conmutador</span><span class="sxs-lookup"><span data-stu-id="17f9b-105">/<system> switch</span></span>

<span data-ttu-id="17f9b-106">El **/<system>** modificador indica al compilador de MIDL que genere una biblioteca de tipos para el sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="17f9b-106">The **/<system>** switch directs the MIDL compiler to generate a type library for the specified system.</span></span> <span data-ttu-id="17f9b-107">El valor predeterminado es el sistema operativo actual.</span><span class="sxs-lookup"><span data-stu-id="17f9b-107">The default is the current operating system.</span></span>

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a><span data-ttu-id="17f9b-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="17f9b-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="17f9b-109"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="17f9b-109"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="17f9b-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="17f9b-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="17f9b-111"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="17f9b-111"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="17f9b-112">Un entorno Windows de 64 de 64 bits basado en Intel, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="17f9b-112">An Intel-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="17f9b-113"><span id="amd64"></span><span id="AMD64"></span>AMD64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="17f9b-113"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="17f9b-114">Un entorno de Windows de 64 bits basado en dispositivos de American micro, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="17f9b-114">An American Micro Devices-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17f9b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17f9b-115">Remarks</span></span>

<span data-ttu-id="17f9b-116">El **/<system>** modificador es funcionalmente igual que la opción de MIDL [**/env**](-env.md) y el COMpilador MIDL lo reconoce únicamente para mantener la compatibilidad con MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="17f9b-116">The **/<system>** switch is functionally the same as the MIDL [**/env**](-env.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span> <span data-ttu-id="17f9b-117">Si va a generar un nuevo archivo make, use el modificador **/env** .</span><span class="sxs-lookup"><span data-stu-id="17f9b-117">If you are generating a new makefile, use the **/env** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="17f9b-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="17f9b-118">Examples</span></span>

<span data-ttu-id="17f9b-119">**MIDL/Win32 nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="17f9b-119">**midl /win32 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="17f9b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="17f9b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f9b-121">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="17f9b-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="17f9b-122">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="17f9b-122">**/env**</span></span>](-env.md)
</dt> </dl>

 

 




