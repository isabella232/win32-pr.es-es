---
title: '\#define (Directiva, Constant)'
description: Directiva de preprocesador que asigna un nombre descriptivo a una constante de la aplicación.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104077140"
---
# <a name="define-directive-constant"></a><span data-ttu-id="68345-103">\#define (Directiva, Constant)</span><span class="sxs-lookup"><span data-stu-id="68345-103">\#define directive (constant)</span></span>

<span data-ttu-id="68345-104">Directiva de preprocesador que asigna un nombre descriptivo a una constante de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68345-104">Preprocessor directive that assigns a meaningful name to a constant in your application.</span></span>



| <span data-ttu-id="68345-105">\#definición *de identifiertoken: cadena*</span><span class="sxs-lookup"><span data-stu-id="68345-105">\#define *identifiertoken-string*</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="68345-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68345-106">Parameters</span></span>



| <span data-ttu-id="68345-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="68345-107">Item</span></span>                                                                                                                       | <span data-ttu-id="68345-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="68345-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68345-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="68345-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                          | <span data-ttu-id="68345-110">Identificador de la constante.</span><span class="sxs-lookup"><span data-stu-id="68345-110">Identifier of the constant.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="68345-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-cadena* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="68345-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-string* \[optional\]</span></span><br/> | <span data-ttu-id="68345-112">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="68345-112">Value of the constant.</span></span> <span data-ttu-id="68345-113">Este parámetro se compone de una serie de tokens, como palabras clave, constantes o instrucciones completas.</span><span class="sxs-lookup"><span data-stu-id="68345-113">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="68345-114">Uno o más caracteres de espacio en blanco deben separar este parámetro del parámetro *Identifier* ; Este espacio en blanco no se considera parte del texto sustituido, ni tampoco ningún espacio en blanco después del último token del texto.</span><span class="sxs-lookup"><span data-stu-id="68345-114">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <br/> <span data-ttu-id="68345-115">Si excluye este parámetro, todas las instancias del parámetro *Identifier* se quitan del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="68345-115">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="68345-116">El identificador permanece definido y se puede probar mediante las directivas [ \# If Defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef y \# ifndef.</span><span class="sxs-lookup"><span data-stu-id="68345-116">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="68345-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68345-117">Remarks</span></span>

<span data-ttu-id="68345-118">Todas las instancias del parámetro de *identificador* que se producen después de la Directiva de [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) en el archivo de código fuente se reemplazarán por el valor del parámetro de *cadena de token* .</span><span class="sxs-lookup"><span data-stu-id="68345-118">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file will be replaced by the value of the *token-string* parameter.</span></span> <span data-ttu-id="68345-119">El identificador solo se reemplaza cuando forma un token. por ejemplo, el identificador no se reemplaza si aparece en un comentario, dentro de una cadena o como parte de un identificador más largo.</span><span class="sxs-lookup"><span data-stu-id="68345-119">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="68345-120">La directiva [ \# UNDEF](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocesador que olvide la definición de un identificador; para obtener más información, vea \# UNDEF (Directiva) (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="68345-120">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="68345-121">La definición de constantes con la opción/D del compilador tiene el mismo efecto que el uso de la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) al principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="68345-121">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="68345-122">Se pueden definir hasta 30 constantes con la opción/D.</span><span class="sxs-lookup"><span data-stu-id="68345-122">Up to 30 constants can be defined with the /D option.</span></span> <span data-ttu-id="68345-123">Para obtener un ejemplo de cómo se puede usar, vea la sección ejemplos de [ \# ifdef y)](dx-graphics-hlsl-appendix-pre-ifdef.md).</span><span class="sxs-lookup"><span data-stu-id="68345-123">For an example of how this can be used, see the Examples section of [\#ifdef and )](dx-graphics-hlsl-appendix-pre-ifdef.md).</span></span>

## <a name="examples"></a><span data-ttu-id="68345-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="68345-124">Examples</span></span>

<span data-ttu-id="68345-125">En el ejemplo siguiente se define el ancho del identificador como la constante entera 80 y, a continuación, se define la longitud en términos de ancho y la constante de tipo entero 10.</span><span class="sxs-lookup"><span data-stu-id="68345-125">The following example defines the identifier WIDTH as the integer constant 80 and then defines LENGTH in terms of WIDTH and the integer constant 10.</span></span>


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



<span data-ttu-id="68345-126">Cada instancia subsiguiente de LENGTH se reemplaza por (WIDTH + 10) y cada instancia subsiguiente de WIDTH + 10 se reemplaza por la expresión (80 + 10).</span><span class="sxs-lookup"><span data-stu-id="68345-126">Every subsequent instance of LENGTH is replaced by (WIDTH + 10), and every subsequent instance of WIDTH + 10 is replaced by the expression (80 + 10).</span></span> <span data-ttu-id="68345-127">Los paréntesis alrededor del ancho + 10 son importantes porque controlan la interpretación en instrucciones como las siguientes.</span><span class="sxs-lookup"><span data-stu-id="68345-127">The parentheses around WIDTH + 10 are important because they control the interpretation in statements such as the following.</span></span>


```
var = LENGTH * 20;
```



<span data-ttu-id="68345-128">Después de la fase de preprocesamiento, la instrucción pasa a ser la siguiente, que se evalúa como 1.800.</span><span class="sxs-lookup"><span data-stu-id="68345-128">After the preprocessing stage the statement becomes the following, which evaluates to 1,800.</span></span>


```
var = ( 80 + 10 ) * 20;
```



<span data-ttu-id="68345-129">Sin paréntesis, el resultado sería el siguiente, que se evalúa como 280.</span><span class="sxs-lookup"><span data-stu-id="68345-129">Without parentheses, the result would be the following, which evaluates to 280.</span></span>


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a><span data-ttu-id="68345-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68345-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68345-131">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68345-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="68345-132">\#definir sobrecargas</span><span class="sxs-lookup"><span data-stu-id="68345-132">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="68345-133">\#UNDEF (Directiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68345-133">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





