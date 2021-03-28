---
title: " error (Directiva)"
description: Directiva de preprocesador que genera mensajes de error en tiempo de compilación.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- HLSL de la Directiva de error
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419546"
---
# <a name="error-directive"></a><span data-ttu-id="5aa2e-104">\#error (Directiva)</span><span class="sxs-lookup"><span data-stu-id="5aa2e-104">\#error Directive</span></span>

<span data-ttu-id="5aa2e-105">Directiva de preprocesador que genera mensajes de error en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="5aa2e-105">Preprocessor directive that produces compiler-time error messages.</span></span>



| <span data-ttu-id="5aa2e-106">\#*token de error: cadena*</span><span class="sxs-lookup"><span data-stu-id="5aa2e-106">\#error *token-string*</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="5aa2e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aa2e-107">Parameters</span></span>



| <span data-ttu-id="5aa2e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5aa2e-108">Item</span></span>                                                                                    | <span data-ttu-id="5aa2e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aa2e-109">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa2e-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-cadena*</span><span class="sxs-lookup"><span data-stu-id="5aa2e-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="5aa2e-111">Mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="5aa2e-111">Error message.</span></span> <span data-ttu-id="5aa2e-112">Este parámetro se compone de una serie de tokens, como palabras clave, constantes o instrucciones completas.</span><span class="sxs-lookup"><span data-stu-id="5aa2e-112">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="5aa2e-113">La cadena de token está sujeta a la expansión de macros.</span><span class="sxs-lookup"><span data-stu-id="5aa2e-113">The token string is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="5aa2e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aa2e-114">Remarks</span></span>

<span data-ttu-id="5aa2e-115">\#las directivas de error son más útiles para detectar incoherencias del programador e infracciones de las restricciones durante el preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="5aa2e-115">\#error directives are most useful for detecting programmer inconsistencies and violation of constraints during preprocessing.</span></span> <span data-ttu-id="5aa2e-116">Cuando \# se encuentra una directiva de error, la compilación finaliza.</span><span class="sxs-lookup"><span data-stu-id="5aa2e-116">When an \#error directive is encountered, compilation terminates.</span></span>

## <a name="examples"></a><span data-ttu-id="5aa2e-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5aa2e-117">Examples</span></span>

<span data-ttu-id="5aa2e-118">En el ejemplo siguiente se muestra el procesamiento de errores durante el preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="5aa2e-118">The following example demonstrates error processing during preprocessing.</span></span>


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a><span data-ttu-id="5aa2e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aa2e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa2e-120">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5aa2e-120">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





