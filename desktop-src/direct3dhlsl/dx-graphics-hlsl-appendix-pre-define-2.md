---
title: '\#define (directiva) (macro)'
description: Directiva de preprocesador que crea una macro de tipo función.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d0c54c0c433c91522c8a72c5955a419eb72f9eee
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387521"
---
# <a name="define-directive-macro"></a><span data-ttu-id="71658-103">\#define (directiva) (macro)</span><span class="sxs-lookup"><span data-stu-id="71658-103">\#define directive (macro)</span></span>

<span data-ttu-id="71658-104">Directiva de preprocesador que crea una macro de tipo función.</span><span class="sxs-lookup"><span data-stu-id="71658-104">Preprocessor directive that creates a function-like macro.</span></span>



| <span data-ttu-id="71658-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span><span class="sxs-lookup"><span data-stu-id="71658-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span></span> |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="71658-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71658-106">Parameters</span></span>



| <span data-ttu-id="71658-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="71658-107">Item</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="71658-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="71658-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71658-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*Identificador*</span><span class="sxs-lookup"><span data-stu-id="71658-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                                                                                                                                                             | <span data-ttu-id="71658-110">Identificador de la macro.</span><span class="sxs-lookup"><span data-stu-id="71658-110">Identifier of the macro.</span></span> <br/> <span data-ttu-id="71658-111">Una segunda [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) para una macro con un identificador que ya existe en el contexto actual genera un error a menos que la segunda secuencia de token sea idéntica a la primera.</span><span class="sxs-lookup"><span data-stu-id="71658-111">A second [\#define](dx-graphics-hlsl-appendix-pre-define.md) for a macro with an identifier that already exists in the current context generates an error unless the second token sequence is identical to the first.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="71658-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span><span class="sxs-lookup"><span data-stu-id="71658-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span></span> <br/> | <span data-ttu-id="71658-113">Lista de argumentos de la macro.</span><span class="sxs-lookup"><span data-stu-id="71658-113">List of arguments to the macro.</span></span> <span data-ttu-id="71658-114">La lista de argumentos está delimitada por comas, puede ser de cualquier longitud y debe incluirse entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="71658-114">The argument list is comma-delimited, can be of any length, and must be enclosed in parentheses.</span></span> <span data-ttu-id="71658-115">Cada nombre de argumento de la lista debe ser único.</span><span class="sxs-lookup"><span data-stu-id="71658-115">Each argument name in the list must be unique.</span></span> <span data-ttu-id="71658-116">Ningún espacio en blanco puede separar *el parámetro de* identificador y el paréntesis de apertura.</span><span class="sxs-lookup"><span data-stu-id="71658-116">No white space can separate the *identifier* parameter and the opening parenthesis.</span></span> <br/> <span data-ttu-id="71658-117">Use la concatenación de líneas colocando una barra diagonal inversa ( ) inmediatamente antes del carácter de nueva línea para dividir directivas \\ largas en varias líneas de origen.</span><span class="sxs-lookup"><span data-stu-id="71658-117">Use line concatenation place a backslash (\\) immediately before the newline character to split long directives onto multiple source lines.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="71658-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="71658-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[optional\]</span></span> <br/>                                                                                                                     | <span data-ttu-id="71658-119">Valor de la macro.</span><span class="sxs-lookup"><span data-stu-id="71658-119">Value of the macro.</span></span> <span data-ttu-id="71658-120">Este parámetro consta de una serie de tokens, como palabras clave, constantes o instrucciones completas.</span><span class="sxs-lookup"><span data-stu-id="71658-120">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="71658-121">Uno o varios caracteres de espacio en blanco deben separar este parámetro del *parámetro identifier;* este espacio en blanco no se considera parte del texto sustituido, ni tampoco ningún espacio en blanco después del último token del texto.</span><span class="sxs-lookup"><span data-stu-id="71658-121">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <span data-ttu-id="71658-122">Use paréntesis para asegurarse de que los argumentos complicados se interpretan correctamente.</span><span class="sxs-lookup"><span data-stu-id="71658-122">Make liberal use of parentheses to ensure that complicated arguments are interpreted correctly.</span></span> <br/> <span data-ttu-id="71658-123">Si el valor del parámetro *identifier* se produce dentro del parámetro *token-string* (incluso como resultado de otra expansión de macro), no se expande.</span><span class="sxs-lookup"><span data-stu-id="71658-123">If the value of the *identifier* parameter occurs within the *token-string* parameter (even as a result of another macro expansion), it is not expanded.</span></span> <br/> <span data-ttu-id="71658-124">Si excluye este parámetro, todas las instancias del parámetro *identifier* se quitan del archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="71658-124">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="71658-125">El identificador permanece definido y se puede probar mediante las directivas [ \# ifdefined](dx-graphics-hlsl-appendix-pre-ifdef.md) \# , ifdef \# e ifndef.</span><span class="sxs-lookup"><span data-stu-id="71658-125">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="71658-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71658-126">Remarks</span></span>

<span data-ttu-id="71658-127">Todas las instancias  del parámetro identifier que se producen después de la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) en el archivo de origen constituyen una llamada macro y el identificador se reemplazará por una versión del parámetro *token-string* que tenga argumentos reales sustituidos por parámetros formales.</span><span class="sxs-lookup"><span data-stu-id="71658-127">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file constitute a macro call, and the identifier will be replaced by a version of the *token-string* parameter that has actual arguments substituted for formal parameters.</span></span> <span data-ttu-id="71658-128">El número de parámetros de la llamada debe coincidir con el número de parámetros de la definición de macro.</span><span class="sxs-lookup"><span data-stu-id="71658-128">The number of parameters in the call must match the number of parameters in the macro definition.</span></span> <span data-ttu-id="71658-129">El identificador solo se reemplaza cuando forma un token; Por ejemplo, el identificador no se reemplaza si aparece en un comentario, dentro de una cadena o como parte de un identificador más largo.</span><span class="sxs-lookup"><span data-stu-id="71658-129">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="71658-130">La [ \# directiva undef](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocesador que olvide la definición de un identificador; para obtener más información, vea \# undef Directive (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="71658-130">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="71658-131">Definir constantes con la opción del compilador /D tiene el mismo efecto que usar la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) al principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="71658-131">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="71658-132">Se pueden definir hasta 30 macros con la opción /D.</span><span class="sxs-lookup"><span data-stu-id="71658-132">Up to 30 macros can be defined with the /D option.</span></span>

<span data-ttu-id="71658-133">Los argumentos reales de la llamada macro coinciden con los argumentos formales correspondientes en la definición de macro.</span><span class="sxs-lookup"><span data-stu-id="71658-133">The actual arguments in the macro call are matched to the corresponding formal arguments in the macro definition.</span></span> <span data-ttu-id="71658-134">Cada argumento formal de la cadena de token se reemplaza por el argumento real correspondiente, a menos que el argumento esté precedido de un operador stringizing ( \# ), charizing ( @) o \# token-pasting ( \# \# ), \# o va seguido de un \# operador .</span><span class="sxs-lookup"><span data-stu-id="71658-134">Each formal argument in the token string is replaced by the corresponding actual argument, unless the argument is preceded by a stringizing (\#), charizing (\#@), or token-pasting (\#\#) operator, or is followed by a \#\# operator.</span></span> <span data-ttu-id="71658-135">Cualquier macro en el argumento real se expande antes de que la directiva reemplace el parámetro formal.</span><span class="sxs-lookup"><span data-stu-id="71658-135">Any macros in the actual argument are expanded before the directive replaces the formal parameter.</span></span>

<span data-ttu-id="71658-136">La pegada de tokens en el compilador HLSL es ligeramente diferente de la pegada de tokens en el compilador de C, ya que los tokens pegados deben ser tokens válidos por sí mismos.</span><span class="sxs-lookup"><span data-stu-id="71658-136">Token pasting in the HLSL compiler is slightly different from token pasting in the C compiler, in that the pasted tokens must be valid tokens on their own.</span></span> <span data-ttu-id="71658-137">Por ejemplo, considere la siguiente definición de macro:</span><span class="sxs-lookup"><span data-stu-id="71658-137">For example, consider the following macro definition:</span></span>


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



<span data-ttu-id="71658-138">En el compilador de C, esto da como resultado lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="71658-138">In the C compiler, this results in the following:</span></span>


```
float4x4 test
```



<span data-ttu-id="71658-139">Sin embargo, en el compilador HLSL, esto da como resultado lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="71658-139">In the HLSL compiler however, this results in the following:</span></span>


```
float4 x4 test
```



<span data-ttu-id="71658-140">Puede evitar este comportamiento mediante la siguiente definición de macro en su lugar.</span><span class="sxs-lookup"><span data-stu-id="71658-140">You can work around this behavior by using the following macro definition instead.</span></span>


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a><span data-ttu-id="71658-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="71658-141">Examples</span></span>

<span data-ttu-id="71658-142">En el ejemplo siguiente se usa una macro para definir líneas de cursor.</span><span class="sxs-lookup"><span data-stu-id="71658-142">The following example uses a macro to define cursor lines.</span></span>


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



<span data-ttu-id="71658-143">En el ejemplo siguiente se define una macro que recupera un entero pseudoaleativo en el intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="71658-143">The following example defines a macro that retrieves a pseudorandom integer in the specified range.</span></span>


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a><span data-ttu-id="71658-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71658-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71658-145">Directivas de preprocesador (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="71658-145">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="71658-146">\#definir sobrecargas</span><span class="sxs-lookup"><span data-stu-id="71658-146">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="71658-147">\#directiva undef (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="71658-147">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





