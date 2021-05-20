---
title: message pragma (Directiva)
description: Directiva Pragma que genera mensajes en tiempo de compilador.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- message pragma Directive HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 813483efb161a06db5ef7e40da99c391f53565bc
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153488"
---
# <a name="message-pragma-directive"></a><span data-ttu-id="9427c-104">message pragma (Directiva)</span><span class="sxs-lookup"><span data-stu-id="9427c-104">message pragma Directive</span></span>

<span data-ttu-id="9427c-105">Directiva Pragma que genera mensajes en tiempo de compilador.</span><span class="sxs-lookup"><span data-stu-id="9427c-105">Pragma directive that produces compiler-time messages.</span></span>



| <span data-ttu-id="9427c-106">\#pragma message("*token-string*")</span><span class="sxs-lookup"><span data-stu-id="9427c-106">\#pragma message("*token-string*")</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="9427c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9427c-107">Parameters</span></span>



| <span data-ttu-id="9427c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9427c-108">Item</span></span>                                                                                    | <span data-ttu-id="9427c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9427c-109">Description</span></span>                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="9427c-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span><span class="sxs-lookup"><span data-stu-id="9427c-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="9427c-111">Mensaje del compilador.</span><span class="sxs-lookup"><span data-stu-id="9427c-111">Compiler message.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="9427c-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9427c-112">Examples</span></span>

<span data-ttu-id="9427c-113">En el ejemplo siguiente se muestra el procesamiento de mensajes durante el preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="9427c-113">The following example demonstrates message processing during preprocessing.</span></span>


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a><span data-ttu-id="9427c-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9427c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9427c-115">Directivas de preprocesador (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="9427c-115">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="9427c-116">\#Directiva pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9427c-116">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





