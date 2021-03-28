---
title: " line (Directiva)"
description: Directiva de preprocesador que establece el número de línea y el nombre de archivo almacenados internamente del compilador en los valores especificados.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- HLSL de la Directiva de línea
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419544"
---
# <a name="line-directive"></a><span data-ttu-id="d1173-104">\#line (Directiva)</span><span class="sxs-lookup"><span data-stu-id="d1173-104">\#line Directive</span></span>

<span data-ttu-id="d1173-105">Directiva de preprocesador que establece el número de línea y el nombre de archivo almacenados internamente del compilador en los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="d1173-105">Preprocessor directive that sets the compiler's internally-stored line number and filename to the specified values.</span></span>



| <span data-ttu-id="d1173-106">\#línea *lineNumber* "*nombreDeArchivo*"</span><span class="sxs-lookup"><span data-stu-id="d1173-106">\#line *lineNumber* "*filename*"</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d1173-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1173-107">Parameters</span></span>



| <span data-ttu-id="d1173-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d1173-108">Item</span></span>                                                                                                                              | <span data-ttu-id="d1173-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1173-109">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1173-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span><span class="sxs-lookup"><span data-stu-id="d1173-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span></span><br/>                    | <span data-ttu-id="d1173-111">Número de línea que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="d1173-111">Line number to set.</span></span> <span data-ttu-id="d1173-112">Puede ser cualquier constante entera.</span><span class="sxs-lookup"><span data-stu-id="d1173-112">This can be any integer constant.</span></span> <span data-ttu-id="d1173-113">El reemplazo de macros se puede realizar en los tokens de preprocesamiento, siempre que el resultado se evalúe como la sintaxis correcta.</span><span class="sxs-lookup"><span data-stu-id="d1173-113">Macro replacement can be performed on the preprocessing tokens, as long as the result evaluates to the correct syntax.</span></span> <br/>                     |
| <span data-ttu-id="d1173-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*nombre de archivo* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="d1173-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*filename* \[optional\]</span></span> <br/> | <span data-ttu-id="d1173-115">Nombre de archivo que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="d1173-115">Filename to set.</span></span> <span data-ttu-id="d1173-116">El nombre de archivo puede ser cualquier combinación de caracteres y debe incluirse entre comillas dobles ("").</span><span class="sxs-lookup"><span data-stu-id="d1173-116">The filename can be any combination of characters, and must be enclosed in double quotation marks (" ").</span></span> <span data-ttu-id="d1173-117">Si se omite este parámetro, el nombre de archivo anterior permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="d1173-117">If this parameter is omitted, the previous filename remains unchanged.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="d1173-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1173-118">Remarks</span></span>

<span data-ttu-id="d1173-119">El compilador usa el número de línea y el nombre de archivo para hacer referencia a los errores que encuentra durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="d1173-119">The compiler uses the line number and filename to refer to errors that it finds during compilation.</span></span> <span data-ttu-id="d1173-120">El número de línea suele referirse a la línea de entrada actual, y el nombre de archivo hace referencia al archivo de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="d1173-120">The line number usually refers to the current input line, and the filename refers to the current input file.</span></span> <span data-ttu-id="d1173-121">El número de línea se incrementa una vez que se procesa cada línea.</span><span class="sxs-lookup"><span data-stu-id="d1173-121">The line number is incremented after each line is processed.</span></span> <span data-ttu-id="d1173-122">Si se cambia el número de línea y el nombre de archivo, el compilador omite los valores anteriores y continúa el procesamiento con los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="d1173-122">If you change the line number and filename, the compiler ignores the previous values and continues processing with the new values.</span></span> <span data-ttu-id="d1173-123">Los \# generadores de programas suelen usar la directiva line para hacer que los mensajes de error hagan referencia al archivo de código fuente original en lugar de al programa generado.</span><span class="sxs-lookup"><span data-stu-id="d1173-123">The \#line directive is typically used by program generators to cause error messages to refer to the original source file instead of to the generated program.</span></span>

<span data-ttu-id="d1173-124">El traductor usa el número de línea y el nombre de archivo para determinar los valores de la \_ \_ \_ \_ línea y el archivo \_ \_ de \_ macros \_ predefinidos.</span><span class="sxs-lookup"><span data-stu-id="d1173-124">The translator uses the line number and filename to determine the values of the predefined macros \_\_FILE\_\_ and \_\_LINE\_\_.</span></span> <span data-ttu-id="d1173-125">Estas macros se pueden utilizar para insertar mensajes de error autodescriptivos en el texto del programa.</span><span class="sxs-lookup"><span data-stu-id="d1173-125">You can use these macros to insert self-descriptive error messages into the program text.</span></span> <span data-ttu-id="d1173-126">La \_ \_ \_ \_ macro File se expande a una cadena cuyo contenido es el nombre de archivo, entre comillas dobles ("").</span><span class="sxs-lookup"><span data-stu-id="d1173-126">The \_\_FILE\_\_ macro expands to a string whose contents are the filename, surrounded by double quotation marks (" ").</span></span>

## <a name="examples"></a><span data-ttu-id="d1173-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d1173-127">Examples</span></span>

<span data-ttu-id="d1173-128">En el ejemplo siguiente se establece el número de línea en 151 y el nombre de archivo en "Copy. c".</span><span class="sxs-lookup"><span data-stu-id="d1173-128">The following example sets the line number to 151 and the filename to "copy.c".</span></span>


```
#line 151 "copy.c"
```



<span data-ttu-id="d1173-129">En el ejemplo siguiente, la macro Assert usa la línea de macros predefinidas \_ \_ \_ \_ y el \_ \_ archivo \_ \_ para imprimir un mensaje de error sobre el archivo de código fuente si la aserción especificada no es true.</span><span class="sxs-lookup"><span data-stu-id="d1173-129">In the following example, the macro ASSERT uses the predefined macros \_\_LINE\_\_ and \_\_FILE\_\_ to print an error message about the source file if the specified assertion is not true.</span></span>


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a><span data-ttu-id="d1173-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1173-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1173-131">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d1173-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





