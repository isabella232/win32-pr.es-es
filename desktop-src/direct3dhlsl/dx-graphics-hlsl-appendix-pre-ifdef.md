---
title: " ifdef y ifndef (directivas)"
description: Directivas de preprocesador que determinan si se define una constante o una macro de preprocesador específica.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef y ifndef (directivas) HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076750"
---
# <a name="ifdef-and-ifndef-directives"></a><span data-ttu-id="7c543-104">\#ifdef y \# ifndef (directivas)</span><span class="sxs-lookup"><span data-stu-id="7c543-104">\#ifdef and \#ifndef Directives</span></span>

<span data-ttu-id="7c543-105">Directivas de preprocesador que determinan si se define una constante o una macro de preprocesador específica.</span><span class="sxs-lookup"><span data-stu-id="7c543-105">Preprocessor directives that determine whether a specific preprocessor constant or macro is defined.</span></span>



| <span data-ttu-id="7c543-106">\#ifdef ( *identificador* )...</span><span class="sxs-lookup"><span data-stu-id="7c543-106">\#ifdef *identifier* ...</span></span>  |
|---------------------------|
| <span data-ttu-id="7c543-107">\#endif</span><span class="sxs-lookup"><span data-stu-id="7c543-107">\#endif</span></span>                   |
| <span data-ttu-id="7c543-108">\#ifndef ( *identificador* )...</span><span class="sxs-lookup"><span data-stu-id="7c543-108">\#ifndef *identifier* ...</span></span> |
| <span data-ttu-id="7c543-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="7c543-109">\#endif</span></span>                   |



 

## <a name="parameters"></a><span data-ttu-id="7c543-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c543-110">Parameters</span></span>



| <span data-ttu-id="7c543-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="7c543-111">Item</span></span>                                                                              | <span data-ttu-id="7c543-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c543-112">Description</span></span>                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="7c543-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="7c543-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="7c543-114">Identificador de la constante o macro que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="7c543-114">Identifier of the constant or macro to check.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c543-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c543-115">Remarks</span></span>

<span data-ttu-id="7c543-116">Puede usar las \# directivas ifdef y \# ifndef en cualquier lugar donde [ \# ](dx-graphics-hlsl-appendix-pre-if.md) se pueda utilizar.</span><span class="sxs-lookup"><span data-stu-id="7c543-116">You can use the \#ifdef and \#ifndef directives anywhere that the [\#if](dx-graphics-hlsl-appendix-pre-if.md) can be used.</span></span> <span data-ttu-id="7c543-117">La \# instrucción ifdef es equivalente a) Directive.</span><span class="sxs-lookup"><span data-stu-id="7c543-117">The \#ifdef statement is equivalent to ) directive.</span></span> <span data-ttu-id="7c543-118">Estas directivas solo comprueban la presencia o ausencia de identificadores definidos mediante la Directiva de [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) , no para los identificadores declarados en el código fuente de C o C++.</span><span class="sxs-lookup"><span data-stu-id="7c543-118">These directives check only for the presence or absence of identifiers defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive, not for identifiers declared in the C or C++ source code.</span></span>

<span data-ttu-id="7c543-119">Estas directivas se proporcionan únicamente por compatibilidad con las versiones anteriores del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="7c543-119">These directives are provided only for compatibility with previous versions of the language.</span></span> <span data-ttu-id="7c543-120">Se prefiere el uso del operador [definido](dx-graphics-hlsl-appendix-pre-if.md) con la \# Directiva if.</span><span class="sxs-lookup"><span data-stu-id="7c543-120">The use of the [defined](dx-graphics-hlsl-appendix-pre-if.md) operator with the \#if directive is preferred.</span></span>

<span data-ttu-id="7c543-121">La \# Directiva ifndef comprueba el opuesto de la condición comprobada por \# ifdef.</span><span class="sxs-lookup"><span data-stu-id="7c543-121">The \#ifndef directive checks for the opposite of the condition checked by \#ifdef.</span></span> <span data-ttu-id="7c543-122">Si no se define el identificador, la condición es true (distinto de cero). de lo contrario, la condición es false (cero).</span><span class="sxs-lookup"><span data-stu-id="7c543-122">If the identifier is not defined, the condition is true (nonzero); otherwise, the condition is false (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="7c543-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7c543-123">Examples</span></span>

<span data-ttu-id="7c543-124">El elemento identifier se puede pasar desde la línea de comandos con la opción /D.</span><span class="sxs-lookup"><span data-stu-id="7c543-124">The identifier can be passed from the command line using the /D option.</span></span> <span data-ttu-id="7c543-125">Se pueden especificar hasta 30 macros con /D.</span><span class="sxs-lookup"><span data-stu-id="7c543-125">Up to 30 macros can be specified with /D.</span></span> <span data-ttu-id="7c543-126">Es útil para comprobar si existe una definición, porque una definición se puede pasar desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="7c543-126">This is useful for checking whether a definition exists, because a definition can be passed from the command line.</span></span> <span data-ttu-id="7c543-127">En el ejemplo siguiente se usa este comportamiento para determinar si se debe ejecutar una aplicación en modo de prueba.</span><span class="sxs-lookup"><span data-stu-id="7c543-127">The following example uses this behavior to determine whether to run an application in test mode.</span></span>


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



<span data-ttu-id="7c543-128">Cuando se compila con el siguiente comando, PROG. cpp se compilará en modo de prueba; de lo contrario, se compilará en el modo final.</span><span class="sxs-lookup"><span data-stu-id="7c543-128">When compiled using the following command, prog.cpp will compile in test mode; otherwise, it will compile in final mode.</span></span>


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a><span data-ttu-id="7c543-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c543-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c543-130">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7c543-130">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="7c543-131">\#Si,)</span><span class="sxs-lookup"><span data-stu-id="7c543-131">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





