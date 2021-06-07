---
title: Atributo const
description: La palabra clave const modifica el tipo de una declaración de tipo o el tipo de un parámetro de función, lo que impide que el valor varíe.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- atributo const MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7095e29daf18dc111caf37038b06b0beff5245a8
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387064"
---
# <a name="const-attribute"></a><span data-ttu-id="a273c-104">Atributo const</span><span class="sxs-lookup"><span data-stu-id="a273c-104">const attribute</span></span>

<span data-ttu-id="a273c-105">La **palabra clave const** modifica el tipo de una declaración de tipo o el tipo de un parámetro de función, lo que impide que el valor varíe.</span><span class="sxs-lookup"><span data-stu-id="a273c-105">The **const** keyword modifies the type of a type declaration or the type of a function parameter, preventing the value from varying.</span></span>

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a><span data-ttu-id="a273c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a273c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a273c-107">*const-type*</span><span class="sxs-lookup"><span data-stu-id="a273c-107">*const-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-108">Especifica un entero MIDL válido, un carácter, una cadena o un tipo booleano.</span><span class="sxs-lookup"><span data-stu-id="a273c-108">Specifies a valid MIDL integer, character, string, or Boolean type.</span></span> <span data-ttu-id="a273c-109">Los tipos MIDL válidos incluyen small [**,**](small.md) [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), \**\* charÂ*, __ [*wchar \_ t* \*](wchar-t.md), \**wchar \_ \* tÂ*_, _ [*byte* \*](byte.md), \**byteÂ \** _, y [_*voidÂ \**_](void.md).</span><span class="sxs-lookup"><span data-stu-id="a273c-109">Valid MIDL types include [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), \**charÂ \**_, [_ *wchar\_t*\*](wchar-t.md), \**wchar\_tÂ \**_, [_ *byte*\*](byte.md), \**byteÂ \** _, and [_*voidÂ \**_](void.md).</span></span> <span data-ttu-id="a273c-110">Los tipos enteros y de caracteres pueden [ser _ *signed* \*](signed.md) [**o unsigned**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="a273c-110">The integer and character types can be [_ *signed*\*](signed.md) or [**unsigned**](unsigned.md).</span></span>

</dd> <dt>

<span data-ttu-id="a273c-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="a273c-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-112">Especifica un identificador MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="a273c-112">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="a273c-113">Los identificadores MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado y deben comenzar con un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="a273c-113">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="a273c-114">*const-expression*</span><span class="sxs-lookup"><span data-stu-id="a273c-114">*const-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-115">Especifica una expresión, un identificador o una constante numérica o de caracteres adecuada para el tipo especificado: literales enteros constantes o expresiones de entero constante para constantes enteras; Expresiones booleanas que se pueden calcular durante la compilación para tipos [**booleanos;**](boolean.md) constantes de un solo carácter para [**tipos char;**](char-idl.md) y constantes de cadena para tipos **\[** [**de**](string.md) **\]** cadena.</span><span class="sxs-lookup"><span data-stu-id="a273c-115">Specifies an expression, identifier, or numeric or character constant appropriate for the specified type: constant integer literals or constant integer expressions for integer constants; Boolean expressions that can be computed at compilation for [**Boolean**](boolean.md) types; single-character constants for [**char**](char-idl.md) types; and string constants for **\[**[**string**](string.md)**\]** types.</span></span> <span data-ttu-id="a273c-116">El [ \* *tipo \* voidÂ* _](void.md) solo se puede inicializar en _\*NULL\*\*.</span><span class="sxs-lookup"><span data-stu-id="a273c-116">The [\**voidÂ \** _](void.md) type can be initialized only to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="a273c-117">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="a273c-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-118">Especifica uno o varios atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="a273c-118">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="a273c-119">*pointer-type*</span><span class="sxs-lookup"><span data-stu-id="a273c-119">*pointer-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-120">Especifica un tipo de puntero MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="a273c-120">Specifies a valid MIDL pointer type.</span></span>

</dd> <dt>

<span data-ttu-id="a273c-121">*declarator y declarator-list*</span><span class="sxs-lookup"><span data-stu-id="a273c-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-122">Especifica declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="a273c-122">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="a273c-123">Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="a273c-123">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="a273c-124">La *lista de declaradores* consta de uno o varios declaradores, separados por comas.</span><span class="sxs-lookup"><span data-stu-id="a273c-124">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="a273c-125">El identificador de nombre de parámetro en el declarador de función es opcional.</span><span class="sxs-lookup"><span data-stu-id="a273c-125">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a273c-126">*function-attr-list*</span><span class="sxs-lookup"><span data-stu-id="a273c-126">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-127">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="a273c-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="a273c-128">Los atributos de función válidos son la devolución de llamada , local; el atributo de puntero **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** y la cadena de atributos de uso , ignore y el identificador de contexto .</span><span class="sxs-lookup"><span data-stu-id="a273c-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="a273c-129">*type-specifier*</span><span class="sxs-lookup"><span data-stu-id="a273c-129">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-130">Especifica un tipo base , [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type o un identificador de tipo. [ \_](midl-base-types.md)</span><span class="sxs-lookup"><span data-stu-id="a273c-130">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="a273c-131">Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="a273c-131">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="a273c-132">*ptr-decl*</span><span class="sxs-lookup"><span data-stu-id="a273c-132">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-133">Especifica cero o más declaradores de puntero.</span><span class="sxs-lookup"><span data-stu-id="a273c-133">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="a273c-134">Un declarador de puntero es el mismo que el declarador de puntero usado en C. Se construye a partir del **\* *designador _ , modificadores como _* far** y el calificador **const**.</span><span class="sxs-lookup"><span data-stu-id="a273c-134">A pointer declarator is the same as the pointer declarator used in C. It is constructed from the \**\**_ designator, modifiers such as _\* far\*\*, and the qualifier **const**.</span></span>

</dd> <dt>

<span data-ttu-id="a273c-135">*function-name*</span><span class="sxs-lookup"><span data-stu-id="a273c-135">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-136">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="a273c-136">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a273c-137">*parameter-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="a273c-137">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a273c-138">Especifica cero o más atributos direccionales, atributos de campo, atributos de uso y atributos de puntero adecuados para el tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="a273c-138">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="a273c-139">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="a273c-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a273c-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a273c-140">Remarks</span></span>

<span data-ttu-id="a273c-141">MIDL permite declarar tipos enteros, caracteres, cadenas y booleanos constantes en el cuerpo de la interfaz del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="a273c-141">MIDL allows you to declare constant integer, character, string, and Boolean types in the interface body of the IDL file.</span></span> <span data-ttu-id="a273c-142">**Las declaraciones** de tipo Const se reproducen en el archivo de encabezado generado como **\# directivas define.**</span><span class="sxs-lookup"><span data-stu-id="a273c-142">**Const** type declarations are reproduced in the generated header file as **\#define** directives.</span></span>

<span data-ttu-id="a273c-143">Los compiladores IDL de DCE no admiten expresiones constantes.</span><span class="sxs-lookup"><span data-stu-id="a273c-143">DCE IDL compilers do not support constant expressions.</span></span> <span data-ttu-id="a273c-144">Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/osf**](-osf.md) del compilador midL.</span><span class="sxs-lookup"><span data-stu-id="a273c-144">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="a273c-145">Una constante definida previamente se puede usar como el valor asignado de una constante subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="a273c-145">A previously defined constant can be used as the assigned value of a subsequent constant.</span></span> <span data-ttu-id="a273c-146">El valor de una expresión entera constante se convierte automáticamente al tipo entero correspondiente de acuerdo con las reglas de conversión de C.</span><span class="sxs-lookup"><span data-stu-id="a273c-146">The value of a constant integral expression is automatically converted to the respective integer type in accordance with C conversion rules.</span></span>

<span data-ttu-id="a273c-147">El valor de una constante de caracteres debe ser un carácter ASCII entre comillas simples.</span><span class="sxs-lookup"><span data-stu-id="a273c-147">The value of a character constant must be a single-quoted ASCII character.</span></span> <span data-ttu-id="a273c-148">Cuando la constante de caracteres es el propio carácter de comilla simple ('), el carácter de barra diagonal inversa ( ) debe preceder al carácter de comilla \\ simple, como en \\ '.</span><span class="sxs-lookup"><span data-stu-id="a273c-148">When the character constant is the single-quote character itself ('), the backslash character (\\) must precede the single-quote character, as in \\'.</span></span>

<span data-ttu-id="a273c-149">El valor de una constante de cadena de caracteres debe ser una cadena entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="a273c-149">The value of a character-string constant must be a double-quoted string.</span></span> <span data-ttu-id="a273c-150">Dentro de una cadena, el carácter de barra diagonal inversa ( ) debe preceder a un carácter literal de comilla **\\** doble ( **"** ), como en **\\ "**.</span><span class="sxs-lookup"><span data-stu-id="a273c-150">Within a string, the backslash (**\\**) character must precede a literal double-quote character ( **"** ), as in **\\"**.</span></span> <span data-ttu-id="a273c-151">Dentro de una cadena, el carácter de barra diagonal inversa ( **\\** ) representa un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="a273c-151">Within a string, the backslash character (**\\**) represents an escape character.</span></span> <span data-ttu-id="a273c-152">Las constantes de cadena pueden constar de hasta 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a273c-152">String constants can consist of up to 255 characters.</span></span>

<span data-ttu-id="a273c-153">El valor **NULL** es el único valor válido para las constantes de tipo [ \* *voidÂ \** _](void.md).</span><span class="sxs-lookup"><span data-stu-id="a273c-153">The value **NULL** is the only valid value for constants of type [\**voidÂ \** _](void.md).</span></span> <span data-ttu-id="a273c-154">Se omiten todos los atributos asociados a la declaración _ \*const\*\*.</span><span class="sxs-lookup"><span data-stu-id="a273c-154">Any attributes associated with the _ *const*\* declaration are ignored.</span></span>

<span data-ttu-id="a273c-155">El compilador MIDL no comprueba si hay errores de intervalo en **la inicialización const.**</span><span class="sxs-lookup"><span data-stu-id="a273c-155">The MIDL compiler does not check for range errors in **const** initialization.</span></span> <span data-ttu-id="a273c-156">Por ejemplo, cuando se especifica "const short x = 0xFFFFFFFF;", el compilador MIDL no informa de un error y el inicializador se reproduce en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="a273c-156">For example, when you specify "const short x = 0xFFFFFFFF;" the MIDL compiler does not report an error and the initializer is reproduced in the generated header file.</span></span>

## <a name="examples"></a><span data-ttu-id="a273c-157">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a273c-157">Examples</span></span>

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a><span data-ttu-id="a273c-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="a273c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a273c-159">**Matrices**</span><span class="sxs-lookup"><span data-stu-id="a273c-159">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="a273c-160">Tipos base midl</span><span class="sxs-lookup"><span data-stu-id="a273c-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a273c-161">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a273c-161">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="a273c-162">**Byte**</span><span class="sxs-lookup"><span data-stu-id="a273c-162">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="a273c-163">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="a273c-163">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="a273c-164">**Char**</span><span class="sxs-lookup"><span data-stu-id="a273c-164">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="a273c-165">**identificador de \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="a273c-165">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="a273c-166">**Enum**</span><span class="sxs-lookup"><span data-stu-id="a273c-166">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="a273c-167">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="a273c-167">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a273c-168">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="a273c-168">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="a273c-169">**Local**</span><span class="sxs-lookup"><span data-stu-id="a273c-169">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="a273c-170">**Largo**</span><span class="sxs-lookup"><span data-stu-id="a273c-170">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="a273c-171">**/osf**</span><span class="sxs-lookup"><span data-stu-id="a273c-171">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="a273c-172">**Ptr**</span><span class="sxs-lookup"><span data-stu-id="a273c-172">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="a273c-173">**ref**</span><span class="sxs-lookup"><span data-stu-id="a273c-173">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="a273c-174">**Corto**</span><span class="sxs-lookup"><span data-stu-id="a273c-174">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="a273c-175">**Firmado**</span><span class="sxs-lookup"><span data-stu-id="a273c-175">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="a273c-176">**Pequeño**</span><span class="sxs-lookup"><span data-stu-id="a273c-176">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="a273c-177">**Cadena**</span><span class="sxs-lookup"><span data-stu-id="a273c-177">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="a273c-178">**Estructura**</span><span class="sxs-lookup"><span data-stu-id="a273c-178">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="a273c-179">**Unión**</span><span class="sxs-lookup"><span data-stu-id="a273c-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="a273c-180">**Único**</span><span class="sxs-lookup"><span data-stu-id="a273c-180">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="a273c-181">**Unsigned**</span><span class="sxs-lookup"><span data-stu-id="a273c-181">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="a273c-182">**void**</span><span class="sxs-lookup"><span data-stu-id="a273c-182">**void**</span></span>](void.md)
</dt> <dt>

[<span data-ttu-id="a273c-183">**wchar \_ t**</span><span class="sxs-lookup"><span data-stu-id="a273c-183">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 