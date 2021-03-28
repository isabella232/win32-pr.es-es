---
title: '\#define (Directiva) (macro)'
description: Directiva de preprocesador que crea una macro similar a una función.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8de5a47fc92c02e9f565c80f600359e8e5b32f9
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104997005"
---
# <a name="define-directive-macro"></a><span data-ttu-id="a1d45-103">\#define (Directiva) (macro)</span><span class="sxs-lookup"><span data-stu-id="a1d45-103">\#define directive (macro)</span></span>

<span data-ttu-id="a1d45-104">Directiva de preprocesador que crea una macro similar a una función.</span><span class="sxs-lookup"><span data-stu-id="a1d45-104">Preprocessor directive that creates a function-like macro.</span></span>



| <span data-ttu-id="a1d45-105">\#define el *identificador*( *argument0*,..., *argumentn-1* ) *token-String*</span><span class="sxs-lookup"><span data-stu-id="a1d45-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span></span> |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="a1d45-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1d45-106">Parameters</span></span>



| <span data-ttu-id="a1d45-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a1d45-107">Item</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="a1d45-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1d45-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d45-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="a1d45-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                                                                                                                                                             | <span data-ttu-id="a1d45-110">Identificador de la macro.</span><span class="sxs-lookup"><span data-stu-id="a1d45-110">Identifier of the macro.</span></span> <br/> <span data-ttu-id="a1d45-111">Una segunda [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) para una macro con un identificador que ya existe en el contexto actual genera un error a menos que la segunda secuencia del token sea idéntica a la primera.</span><span class="sxs-lookup"><span data-stu-id="a1d45-111">A second [\#define](dx-graphics-hlsl-appendix-pre-define.md) for a macro with an identifier that already exists in the current context generates an error unless the second token sequence is identical to the first.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a1d45-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*,..., *argumentn-1* )</span><span class="sxs-lookup"><span data-stu-id="a1d45-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span></span> <br/> | <span data-ttu-id="a1d45-113">Lista de argumentos de la macro.</span><span class="sxs-lookup"><span data-stu-id="a1d45-113">List of arguments to the macro.</span></span> <span data-ttu-id="a1d45-114">La lista de argumentos está delimitada por comas, puede tener cualquier longitud y debe incluirse entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="a1d45-114">The argument list is comma-delimited, can be of any length, and must be enclosed in parentheses.</span></span> <span data-ttu-id="a1d45-115">Cada nombre de argumento de la lista debe ser único.</span><span class="sxs-lookup"><span data-stu-id="a1d45-115">Each argument name in the list must be unique.</span></span> <span data-ttu-id="a1d45-116">Ningún espacio en blanco puede separar el parámetro de *identificador* y el paréntesis de apertura.</span><span class="sxs-lookup"><span data-stu-id="a1d45-116">No white space can separate the *identifier* parameter and the opening parenthesis.</span></span> <br/> <span data-ttu-id="a1d45-117">Usar concatenación de línea Coloque una barra diagonal inversa ( \) inmediatamente antes del carácter de nueva línea para dividir las directivas largas en varias líneas de código fuente.</span><span class="sxs-lookup"><span data-stu-id="a1d45-117">Use line concatenation place a backslash (\) immediately before the newline character to split long directives onto multiple source lines.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a1d45-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-cadena* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="a1d45-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[optional\]</span></span> <br/>                                                                                                                     | <span data-ttu-id="a1d45-119">Valor de la macro.</span><span class="sxs-lookup"><span data-stu-id="a1d45-119">Value of the macro.</span></span> <span data-ttu-id="a1d45-120">Este parámetro se compone de una serie de tokens, como palabras clave, constantes o instrucciones completas.</span><span class="sxs-lookup"><span data-stu-id="a1d45-120">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="a1d45-121">Uno o más caracteres de espacio en blanco deben separar este parámetro del parámetro *Identifier* ; Este espacio en blanco no se considera parte del texto sustituido, ni tampoco ningún espacio en blanco después del último token del texto.</span><span class="sxs-lookup"><span data-stu-id="a1d45-121">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <span data-ttu-id="a1d45-122">Haga un uso liberal de los paréntesis para asegurarse de que los argumentos complicados se interpreten correctamente.</span><span class="sxs-lookup"><span data-stu-id="a1d45-122">Make liberal use of parentheses to ensure that complicated arguments are interpreted correctly.</span></span> <br/> <span data-ttu-id="a1d45-123">Si el valor del parámetro *Identifier* aparece dentro del parámetro *token-String* (incluso como resultado de otra expansión de macro), no se expande.</span><span class="sxs-lookup"><span data-stu-id="a1d45-123">If the value of the *identifier* parameter occurs within the *token-string* parameter (even as a result of another macro expansion), it is not expanded.</span></span> <br/> <span data-ttu-id="a1d45-124">Si excluye este parámetro, todas las instancias del parámetro *Identifier* se quitan del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="a1d45-124">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="a1d45-125">El identificador permanece definido y se puede probar mediante las directivas [ \# If Defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef y \# ifndef.</span><span class="sxs-lookup"><span data-stu-id="a1d45-125">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="a1d45-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1d45-126">Remarks</span></span>

<span data-ttu-id="a1d45-127">Todas las instancias del parámetro de *identificador* que se producen después de la Directiva de [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) en el archivo de código fuente constituyen una llamada de macro y el identificador se reemplazará por una versión del parámetro de *cadena de token* que tenga argumentos reales sustituidos por parámetros formales.</span><span class="sxs-lookup"><span data-stu-id="a1d45-127">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file constitute a macro call, and the identifier will be replaced by a version of the *token-string* parameter that has actual arguments substituted for formal parameters.</span></span> <span data-ttu-id="a1d45-128">El número de parámetros de la llamada debe coincidir con el número de parámetros de la definición de macro.</span><span class="sxs-lookup"><span data-stu-id="a1d45-128">The number of parameters in the call must match the number of parameters in the macro definition.</span></span> <span data-ttu-id="a1d45-129">El identificador solo se reemplaza cuando forma un token. por ejemplo, el identificador no se reemplaza si aparece en un comentario, dentro de una cadena o como parte de un identificador más largo.</span><span class="sxs-lookup"><span data-stu-id="a1d45-129">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="a1d45-130">La directiva [ \# UNDEF](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocesador que olvide la definición de un identificador; para obtener más información, vea \# UNDEF (Directiva) (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="a1d45-130">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="a1d45-131">La definición de constantes con la opción/D del compilador tiene el mismo efecto que el uso de la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) al principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="a1d45-131">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="a1d45-132">Se pueden definir hasta 30 macros con la opción/D.</span><span class="sxs-lookup"><span data-stu-id="a1d45-132">Up to 30 macros can be defined with the /D option.</span></span>

<span data-ttu-id="a1d45-133">Los argumentos reales de la llamada de macro coinciden con los argumentos formales correspondientes en la definición de macro.</span><span class="sxs-lookup"><span data-stu-id="a1d45-133">The actual arguments in the macro call are matched to the corresponding formal arguments in the macro definition.</span></span> <span data-ttu-id="a1d45-134">Cada argumento formal de la cadena de token se reemplaza por el argumento real correspondiente, a menos que el argumento esté precedido por un operador de generación de cadenas ( \# ), de carácter ( \# @) o de pegado de token ( \# \# ), o que vaya seguido de un \# \# operador.</span><span class="sxs-lookup"><span data-stu-id="a1d45-134">Each formal argument in the token string is replaced by the corresponding actual argument, unless the argument is preceded by a stringizing (\#), charizing (\#@), or token-pasting (\#\#) operator, or is followed by a \#\# operator.</span></span> <span data-ttu-id="a1d45-135">Cualquier macro en el argumento real se expande antes de que la directiva reemplace el parámetro formal.</span><span class="sxs-lookup"><span data-stu-id="a1d45-135">Any macros in the actual argument are expanded before the directive replaces the formal parameter.</span></span>

<span data-ttu-id="a1d45-136">El pegado de tokens en el compilador de HLSL es ligeramente diferente del pegado de tokens en el compilador de C, en que los tokens pegados deben ser tokens válidos por su cuenta.</span><span class="sxs-lookup"><span data-stu-id="a1d45-136">Token pasting in the HLSL compiler is slightly different from token pasting in the C compiler, in that the pasted tokens must be valid tokens on their own.</span></span> <span data-ttu-id="a1d45-137">Por ejemplo, considere la siguiente definición de macro:</span><span class="sxs-lookup"><span data-stu-id="a1d45-137">For example, consider the following macro definition:</span></span>


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



<span data-ttu-id="a1d45-138">En el compilador de C, esto da como resultado lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a1d45-138">In the C compiler, this results in the following:</span></span>


```
float4x4 test
```



<span data-ttu-id="a1d45-139">Sin embargo, en el compilador HLSL, esto da como resultado lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a1d45-139">In the HLSL compiler however, this results in the following:</span></span>


```
float4 x4 test
```



<span data-ttu-id="a1d45-140">Puede solucionar este comportamiento mediante la siguiente definición de macro.</span><span class="sxs-lookup"><span data-stu-id="a1d45-140">You can work around this behavior by using the following macro definition instead.</span></span>


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a><span data-ttu-id="a1d45-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a1d45-141">Examples</span></span>

<span data-ttu-id="a1d45-142">En el ejemplo siguiente se usa una macro para definir líneas de cursores.</span><span class="sxs-lookup"><span data-stu-id="a1d45-142">The following example uses a macro to define cursor lines.</span></span>


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



<span data-ttu-id="a1d45-143">En el ejemplo siguiente se define una macro que recupera un entero pseudoaleatorio en el intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="a1d45-143">The following example defines a macro that retrieves a pseudorandom integer in the specified range.</span></span>


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a><span data-ttu-id="a1d45-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1d45-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1d45-145">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a1d45-145">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="a1d45-146">\#definir sobrecargas</span><span class="sxs-lookup"><span data-stu-id="a1d45-146">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="a1d45-147">\#UNDEF (Directiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a1d45-147">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





