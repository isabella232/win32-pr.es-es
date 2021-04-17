---
description: Comprueba si un puntero es NULL. Si el puntero es NULL, la función o el método en el que aparece la macro devuelve el valor especificado.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro CheckPointr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660826"
---
# <a name="checkpointer-macro"></a><span data-ttu-id="811e9-104">Macro CheckPointr</span><span class="sxs-lookup"><span data-stu-id="811e9-104">CheckPointer macro</span></span>

<span data-ttu-id="811e9-105">Comprueba si un puntero es **null**.</span><span class="sxs-lookup"><span data-stu-id="811e9-105">Checks whether a pointer is **NULL**.</span></span> <span data-ttu-id="811e9-106">Si el puntero es **null**, la función o el método en el que aparece la macro devuelve el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="811e9-106">If the pointer is **NULL**, the function or method in which the macro appears returns the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="811e9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="811e9-107">Syntax</span></span>


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a><span data-ttu-id="811e9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="811e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="811e9-109">*m*</span><span class="sxs-lookup"><span data-stu-id="811e9-109">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="811e9-110">Puntero que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="811e9-110">Pointer to check.</span></span>

</dd> <dt>

<span data-ttu-id="811e9-111">*direcc*</span><span class="sxs-lookup"><span data-stu-id="811e9-111">*ret*</span></span> 
</dt> <dd>

<span data-ttu-id="811e9-112">Valor que devuelve la función o el método si *p* es **null**.</span><span class="sxs-lookup"><span data-stu-id="811e9-112">Value that the function or method returns if *p* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="811e9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="811e9-113">Return value</span></span>

<span data-ttu-id="811e9-114">La función circundante devuelve *RET* si *p* es **null**.</span><span class="sxs-lookup"><span data-stu-id="811e9-114">The surrounding function returns *ret* if *p* is **NULL**.</span></span> <span data-ttu-id="811e9-115">De lo contrario, la macro no hace que la función circundante devuelva.</span><span class="sxs-lookup"><span data-stu-id="811e9-115">Otherwise, the macro does not cause the surrounding function to return.</span></span>

## <a name="examples"></a><span data-ttu-id="811e9-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="811e9-116">Examples</span></span>


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a><span data-ttu-id="811e9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="811e9-117">Requirements</span></span>



| <span data-ttu-id="811e9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="811e9-118">Requirement</span></span> | <span data-ttu-id="811e9-119">Value</span><span class="sxs-lookup"><span data-stu-id="811e9-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="811e9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="811e9-120">Header</span></span><br/> | <dl> <span data-ttu-id="811e9-121"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="811e9-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="811e9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="811e9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="811e9-123">Macros de validación de puntero</span><span class="sxs-lookup"><span data-stu-id="811e9-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




