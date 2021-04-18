---
description: Produce una excepción de punto de interrupción y registra la cadena especificada mediante la macro DbgLog. Se omite en las compilaciones comerciales.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Macro KDbgBreak (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690019"
---
# <a name="kdbgbreak-macro"></a><span data-ttu-id="08c31-104">KDbgBreak (macro)</span><span class="sxs-lookup"><span data-stu-id="08c31-104">KDbgBreak macro</span></span>

<span data-ttu-id="08c31-105">Produce una excepción de punto de interrupción y registra la cadena especificada mediante la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="08c31-105">Causes a breakpoint exception, and logs the specified string using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="08c31-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="08c31-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c31-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08c31-107">Syntax</span></span>


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="08c31-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08c31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c31-109">*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="08c31-109">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="08c31-110">Cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="08c31-110">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08c31-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08c31-111">Return value</span></span>

<span data-ttu-id="08c31-112">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="08c31-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08c31-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08c31-113">Remarks</span></span>

<span data-ttu-id="08c31-114">A diferencia de la macro [**DbgBreak**](dbgbreak.md) , esta macro no muestra un cuadro de mensaje que pide al usuario.</span><span class="sxs-lookup"><span data-stu-id="08c31-114">Unlike the [**DbgBreak**](dbgbreak.md) macro, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="08c31-115">En las compilaciones de depuración, provoca automáticamente que se produzca una excepción de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="08c31-115">In debug builds, it automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="08c31-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08c31-116">Requirements</span></span>



| <span data-ttu-id="08c31-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="08c31-117">Requirement</span></span> | <span data-ttu-id="08c31-118">Value</span><span class="sxs-lookup"><span data-stu-id="08c31-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08c31-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08c31-119">Header</span></span><br/> | <dl> <span data-ttu-id="08c31-120"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08c31-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08c31-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="08c31-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c31-122">Macros Assert y Breakpoint</span><span class="sxs-lookup"><span data-stu-id="08c31-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




