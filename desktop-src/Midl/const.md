---
title: const (atributo)
description: La palabra clave const modifica el tipo de una declaración de tipos o el tipo de un parámetro de función, lo que impide variar el valor.
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
ms.openlocfilehash: 8d2980f0f484c838e4f972bbf12fb72173edb3e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789874"
---
# <a name="const-attribute"></a><span data-ttu-id="7f05d-104">const (atributo)</span><span class="sxs-lookup"><span data-stu-id="7f05d-104">const attribute</span></span>

<span data-ttu-id="7f05d-105">La palabra clave **const** modifica el tipo de una declaración de tipos o el tipo de un parámetro de función, lo que impide variar el valor.</span><span class="sxs-lookup"><span data-stu-id="7f05d-105">The **const** keyword modifies the type of a type declaration or the type of a function parameter, preventing the value from varying.</span></span>

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a><span data-ttu-id="7f05d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f05d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f05d-107">*const-Type*</span><span class="sxs-lookup"><span data-stu-id="7f05d-107">*const-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-108">Especifica un entero, un carácter, una cadena o un tipo booleano válidos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="7f05d-108">Specifies a valid MIDL integer, character, string, or Boolean type.</span></span> <span data-ttu-id="7f05d-109">Entre los tipos de MIDL válidos se incluyen [**Small**](small.md), [**Short**](short.md), [**Long**](long.md), [**Char**](char-idl.md), **charÂ \***, [**WCHAR \_ t**](wchar-t.md), **WCHAR \_ tÂ \***, [**byte**](byte.md), **byteÂ \*** y [**voidÂ \***](void.md).</span><span class="sxs-lookup"><span data-stu-id="7f05d-109">Valid MIDL types include [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), **charÂ \***, [**wchar\_t**](wchar-t.md), **wchar\_tÂ \***, [**byte**](byte.md), **byteÂ \***, and [**voidÂ \***](void.md).</span></span> <span data-ttu-id="7f05d-110">Los tipos enteros y de caracteres pueden estar [**firmados**](signed.md) o [**sin firmar**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="7f05d-110">The integer and character types can be [**signed**](signed.md) or [**unsigned**](unsigned.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f05d-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="7f05d-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-112">Especifica un identificador de MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="7f05d-112">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="7f05d-113">Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="7f05d-113">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="7f05d-114">*const-Expression*</span><span class="sxs-lookup"><span data-stu-id="7f05d-114">*const-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-115">Especifica una expresión, un identificador o una constante numérica o de caracteres adecuada para el tipo especificado: literales constantes de tipo entero o expresiones de entero constante para constantes de tipo entero. Expresiones booleanas que se pueden calcular en la compilación para tipos [**booleanos**](boolean.md) ; constantes de un solo carácter para tipos [**Char**](char-idl.md) ; y las constantes de cadena para los tipos de **\[** [**cadena**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7f05d-115">Specifies an expression, identifier, or numeric or character constant appropriate for the specified type: constant integer literals or constant integer expressions for integer constants; Boolean expressions that can be computed at compilation for [**Boolean**](boolean.md) types; single-character constants for [**char**](char-idl.md) types; and string constants for **\[**[**string**](string.md)**\]** types.</span></span> <span data-ttu-id="7f05d-116">El [**tipo \* voidÂ**](void.md) solo se puede inicializar en **null**.</span><span class="sxs-lookup"><span data-stu-id="7f05d-116">The [**voidÂ \***](void.md) type can be initialized only to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7f05d-117">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="7f05d-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-118">Especifica uno o más atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="7f05d-118">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="7f05d-119">*tipo de puntero*</span><span class="sxs-lookup"><span data-stu-id="7f05d-119">*pointer-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-120">Especifica un tipo de puntero MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="7f05d-120">Specifies a valid MIDL pointer type.</span></span>

</dd> <dt>

<span data-ttu-id="7f05d-121">*declarador y lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="7f05d-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-122">Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="7f05d-122">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="7f05d-123">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="7f05d-123">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="7f05d-124">La *lista de declaradores* consta de uno o varios declaradores, separados por comas.</span><span class="sxs-lookup"><span data-stu-id="7f05d-124">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="7f05d-125">El identificador de nombre de parámetro en el declarador de función es opcional.</span><span class="sxs-lookup"><span data-stu-id="7f05d-125">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="7f05d-126">*function-ATTR-List*</span><span class="sxs-lookup"><span data-stu-id="7f05d-126">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-127">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="7f05d-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="7f05d-128">Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7f05d-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="7f05d-129">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="7f05d-129">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-130">Especifica un [ \_ tipo base](midl-base-types.md), [**un struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="7f05d-130">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="7f05d-131">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="7f05d-131">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="7f05d-132">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="7f05d-132">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-133">Especifica cero o más declaradores de puntero.</span><span class="sxs-lookup"><span data-stu-id="7f05d-133">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="7f05d-134">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C. Se construye a partir del **\*** designador, modificadores como **Far** y el calificador **const**.</span><span class="sxs-lookup"><span data-stu-id="7f05d-134">A pointer declarator is the same as the pointer declarator used in C. It is constructed from the **\*** designator, modifiers such as **far**, and the qualifier **const**.</span></span>

</dd> <dt>

<span data-ttu-id="7f05d-135">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="7f05d-135">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-136">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="7f05d-136">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="7f05d-137">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="7f05d-137">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7f05d-138">Especifica cero o más atributos direccionales, atributos de campo, atributos de uso y atributos de puntero adecuados para el tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="7f05d-138">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="7f05d-139">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="7f05d-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f05d-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f05d-140">Remarks</span></span>

<span data-ttu-id="7f05d-141">MIDL permite declarar tipos enteros constantes, de caracteres, de cadena y booleanos en el cuerpo de la interfaz del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7f05d-141">MIDL allows you to declare constant integer, character, string, and Boolean types in the interface body of the IDL file.</span></span> <span data-ttu-id="7f05d-142">Las declaraciones de tipos **const** se reproducen en el archivo de encabezado generado como directivas de **\# definición** .</span><span class="sxs-lookup"><span data-stu-id="7f05d-142">**Const** type declarations are reproduced in the generated header file as **\#define** directives.</span></span>

<span data-ttu-id="7f05d-143">Los compiladores de DCE IDL no admiten expresiones constantes.</span><span class="sxs-lookup"><span data-stu-id="7f05d-143">DCE IDL compilers do not support constant expressions.</span></span> <span data-ttu-id="7f05d-144">Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/OSF**](-osf.md) del compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="7f05d-144">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="7f05d-145">Se puede usar una constante definida previamente como el valor asignado de una constante subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="7f05d-145">A previously defined constant can be used as the assigned value of a subsequent constant.</span></span> <span data-ttu-id="7f05d-146">El valor de una expresión integral constante se convierte automáticamente al tipo de entero correspondiente de acuerdo con las reglas de conversión de C.</span><span class="sxs-lookup"><span data-stu-id="7f05d-146">The value of a constant integral expression is automatically converted to the respective integer type in accordance with C conversion rules.</span></span>

<span data-ttu-id="7f05d-147">El valor de una constante de caracteres debe ser un carácter ASCII entre comillas simples.</span><span class="sxs-lookup"><span data-stu-id="7f05d-147">The value of a character constant must be a single-quoted ASCII character.</span></span> <span data-ttu-id="7f05d-148">Cuando la constante de caracteres es el propio carácter de comilla simple ('), el carácter de barra diagonal inversa ( \) debe preceder al carácter de comilla simple, como en \\ '.</span><span class="sxs-lookup"><span data-stu-id="7f05d-148">When the character constant is the single-quote character itself ('), the backslash character (\) must precede the single-quote character, as in \\'.</span></span>

<span data-ttu-id="7f05d-149">El valor de una constante de cadena de caracteres debe ser una cadena entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="7f05d-149">The value of a character-string constant must be a double-quoted string.</span></span> <span data-ttu-id="7f05d-150">Dentro de una cadena, el carácter de barra diagonal inversa ( **\\** ) debe preceder a un carácter de comilla doble literal ( **"** ), como en **\\ "**.</span><span class="sxs-lookup"><span data-stu-id="7f05d-150">Within a string, the backslash (**\\**) character must precede a literal double-quote character ( **"** ), as in **\\"**.</span></span> <span data-ttu-id="7f05d-151">Dentro de una cadena, el carácter de barra diagonal inversa ( **\\** ) representa un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="7f05d-151">Within a string, the backslash character (**\\**) represents an escape character.</span></span> <span data-ttu-id="7f05d-152">Las constantes de cadena pueden constar de hasta 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7f05d-152">String constants can consist of up to 255 characters.</span></span>

<span data-ttu-id="7f05d-153">El valor **null** es el único valor válido para las constantes de tipo [**voidÂ \***](void.md).</span><span class="sxs-lookup"><span data-stu-id="7f05d-153">The value **NULL** is the only valid value for constants of type [**voidÂ \***](void.md).</span></span> <span data-ttu-id="7f05d-154">Se omiten los atributos asociados a la declaración **const** .</span><span class="sxs-lookup"><span data-stu-id="7f05d-154">Any attributes associated with the **const** declaration are ignored.</span></span>

<span data-ttu-id="7f05d-155">El compilador MIDL no comprueba los errores de intervalo en la inicialización **const** .</span><span class="sxs-lookup"><span data-stu-id="7f05d-155">The MIDL compiler does not check for range errors in **const** initialization.</span></span> <span data-ttu-id="7f05d-156">Por ejemplo, si especifica "const Short x = 0xFFFFFFFF;", el compilador MIDL no notificará un error y el inicializador se reproducirá en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="7f05d-156">For example, when you specify "const short x = 0xFFFFFFFF;" the MIDL compiler does not report an error and the initializer is reproduced in the generated header file.</span></span>

## <a name="examples"></a><span data-ttu-id="7f05d-157">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7f05d-157">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="7f05d-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f05d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f05d-159">**matrices**</span><span class="sxs-lookup"><span data-stu-id="7f05d-159">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="7f05d-160">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="7f05d-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="7f05d-161">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="7f05d-161">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="7f05d-162">**bytes**</span><span class="sxs-lookup"><span data-stu-id="7f05d-162">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="7f05d-163">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="7f05d-163">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="7f05d-164">**char**</span><span class="sxs-lookup"><span data-stu-id="7f05d-164">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="7f05d-165">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="7f05d-165">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="7f05d-166">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="7f05d-166">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="7f05d-167">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="7f05d-167">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7f05d-168">**omitir**</span><span class="sxs-lookup"><span data-stu-id="7f05d-168">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="7f05d-169">**localizar**</span><span class="sxs-lookup"><span data-stu-id="7f05d-169">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="7f05d-170">**tal**</span><span class="sxs-lookup"><span data-stu-id="7f05d-170">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="7f05d-171">**/osf**</span><span class="sxs-lookup"><span data-stu-id="7f05d-171">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="7f05d-172">**ptr**</span><span class="sxs-lookup"><span data-stu-id="7f05d-172">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="7f05d-173">**ref**</span><span class="sxs-lookup"><span data-stu-id="7f05d-173">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="7f05d-174">**short**</span><span class="sxs-lookup"><span data-stu-id="7f05d-174">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="7f05d-175">**conectado**</span><span class="sxs-lookup"><span data-stu-id="7f05d-175">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="7f05d-176">**pequeño**</span><span class="sxs-lookup"><span data-stu-id="7f05d-176">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="7f05d-177">**string**</span><span class="sxs-lookup"><span data-stu-id="7f05d-177">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="7f05d-178">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="7f05d-178">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="7f05d-179">**Unión**</span><span class="sxs-lookup"><span data-stu-id="7f05d-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="7f05d-180">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="7f05d-180">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="7f05d-181">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="7f05d-181">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="7f05d-182">**void**</span><span class="sxs-lookup"><span data-stu-id="7f05d-182">**void**</span></span>](void.md)
</dt> <dt>

[<span data-ttu-id="7f05d-183">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="7f05d-183">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 