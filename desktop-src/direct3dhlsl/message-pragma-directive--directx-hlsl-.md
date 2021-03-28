---
title: Message pragma (Directiva)
description: Directiva pragma que genera mensajes en tiempo de compilación.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- Message pragma Directive HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f342f4a139320e4beb821f32662da72785ab751c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784462"
---
# <a name="message-pragma-directive"></a><span data-ttu-id="0fd74-104">Message pragma (Directiva)</span><span class="sxs-lookup"><span data-stu-id="0fd74-104">message pragma Directive</span></span>

<span data-ttu-id="0fd74-105">Directiva pragma que genera mensajes en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="0fd74-105">Pragma directive that produces compiler-time messages.</span></span>



| <span data-ttu-id="0fd74-106">\#pragma Message "*token-String*"</span><span class="sxs-lookup"><span data-stu-id="0fd74-106">\#pragma message "*token-string*"</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0fd74-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fd74-107">Parameters</span></span>



| <span data-ttu-id="0fd74-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0fd74-108">Item</span></span>                                                                                    | <span data-ttu-id="0fd74-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fd74-109">Description</span></span>                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="0fd74-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-cadena*</span><span class="sxs-lookup"><span data-stu-id="0fd74-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="0fd74-111">Mensaje del compilador.</span><span class="sxs-lookup"><span data-stu-id="0fd74-111">Compiler message.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="0fd74-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0fd74-112">Examples</span></span>

<span data-ttu-id="0fd74-113">En el ejemplo siguiente se muestra el procesamiento de mensajes durante el preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="0fd74-113">The following example demonstrates message processing during preprocessing.</span></span>


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a><span data-ttu-id="0fd74-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fd74-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd74-115">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fd74-115">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="0fd74-116">\#pragma (Directiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fd74-116">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





