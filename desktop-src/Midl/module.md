---
title: Module (atributo)
description: La instrucción Module define un grupo de funciones, normalmente un conjunto de puntos de entrada de DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- atributo de módulo MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358888"
---
# <a name="module-attribute"></a><span data-ttu-id="b529a-104">Module (atributo)</span><span class="sxs-lookup"><span data-stu-id="b529a-104">module attribute</span></span>

<span data-ttu-id="b529a-105">La instrucción **Module** define un grupo de funciones, normalmente un conjunto de puntos de entrada de dll.</span><span class="sxs-lookup"><span data-stu-id="b529a-105">The **module** statement defines a group of functions, typically a set of DLL entry points.</span></span>

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="b529a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b529a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b529a-107">*attributes*</span><span class="sxs-lookup"><span data-stu-id="b529a-107">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="b529a-108">Los \[ atributos [**UUID**](uuid.md) \] , \[ [**version**](version.md) \] , \[ [**HelpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] y \[ [**DllName**](dllname-str-.md) \] se aceptan antes de una instrucción **Module** .</span><span class="sxs-lookup"><span data-stu-id="b529a-108">The \[[**uuid**](uuid.md)\], \[[**version**](version.md)\], \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**hidden**](hidden.md)\], and \[[**dllname**](dllname-str-.md)\] attributes are accepted before a **module** statement.</span></span> <span data-ttu-id="b529a-109">Vea [descripciones de atributos](/previous-versions/windows/desktop/automat/attribute-descriptions), en el libro de automatización OLE, para obtener más información sobre los atributos aceptados antes de la definición de un módulo.</span><span class="sxs-lookup"><span data-stu-id="b529a-109">See [Attribute Descriptions](/previous-versions/windows/desktop/automat/attribute-descriptions), in the OLE Automation book, for more information on the attributes accepted before a module definition.</span></span> <span data-ttu-id="b529a-110">El \[ atributo **DllName** \] es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b529a-110">The \[**dllname**\] attribute is required.</span></span> <span data-ttu-id="b529a-111">Si \[  \] se omite el atributo UUID, el módulo no se especifica de forma única en el sistema.</span><span class="sxs-lookup"><span data-stu-id="b529a-111">If the \[**uuid**\] attribute is omitted, the module is not uniquely specified in the system.</span></span>

</dd> <dt>

<span data-ttu-id="b529a-112">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="b529a-112">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="b529a-113">El nombre del módulo.</span><span class="sxs-lookup"><span data-stu-id="b529a-113">The name of the module.</span></span>

</dd> <dt>

<span data-ttu-id="b529a-114">*elementlist*</span><span class="sxs-lookup"><span data-stu-id="b529a-114">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="b529a-115">Lista de definiciones constantes y prototipos de función para cada función del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="b529a-115">List of constant definitions and function prototypes for each function in the DLL.</span></span> <span data-ttu-id="b529a-116">Puede aparecer cualquier número de definiciones de función en la lista de funciones.</span><span class="sxs-lookup"><span data-stu-id="b529a-116">Any number of function definitions can appear in the function list.</span></span> <span data-ttu-id="b529a-117">Una función de la lista de funciones tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="b529a-117">A function in the function list has the following form:</span></span>

<span data-ttu-id="b529a-118">\[*atributos* \] de *ReturnType* \[ *Convención de llamada funcName* \] (*params*);</span><span class="sxs-lookup"><span data-stu-id="b529a-118">\[*attributes*\] *returntype* \[*calling convention funcname*\](*params*);</span></span>

<span data-ttu-id="b529a-119">\[*atributos* \] de [**const**](const.md) constantType *constname*  =  *constval*;</span><span class="sxs-lookup"><span data-stu-id="b529a-119">\[*attributes*\] [**const**](const.md) constanttype *constname* = *constval*;</span></span>

<span data-ttu-id="b529a-120">Solo \[ [](helpstring.md) \] se aceptan los atributos HelpString y \[ [**HelpContext**](helpcontext.md) \] para [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="b529a-120">Only the \[[**helpstring**](helpstring.md)\] and \[[**helpcontext**](helpcontext.md)\] attributes are accepted for a [**const**](const.md).</span></span>

<span data-ttu-id="b529a-121">Los siguientes atributos se aceptan en una función de un módulo: \[ [**HelpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**PROPPUT**](propput.md) \] , \[ [**PROPPUTREF**](propputref.md) \] y \[ [**vararg**](vararg.md) \] .</span><span class="sxs-lookup"><span data-stu-id="b529a-121">The following attributes are accepted on a function in a module: \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**string**](string.md)\], \[[**entry**](entry.md)\], \[[**propget**](propget.md)\], \[[**propput**](propput.md)\], \[[**propputref**](propputref.md)\], and \[[**vararg**](vararg.md)\].</span></span> <span data-ttu-id="b529a-122">Si \[  \] se especifica vararg, el último parámetro debe ser una matriz segura de tipo **Variant** .</span><span class="sxs-lookup"><span data-stu-id="b529a-122">If \[**vararg**\] is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="b529a-123">La Convención de llamada opcional puede ser una de \_ \_ Pascal/ \_ Pascal/Pascal, \_ \_ Cdecl/ \_ Cdecl/Cdecl o \_ \_ Stdcall/ \_ Stdcall/Stdcall.</span><span class="sxs-lookup"><span data-stu-id="b529a-123">The optional calling convention can be one of \_\_pascal/\_pascal/pascal, \_\_cdecl/\_cdecl/cdecl, or \_\_stdcall/\_stdcall/stdcall.</span></span> <span data-ttu-id="b529a-124">El *tipo de Convención de llamada paramName* puede incluir hasta dos subrayados iniciales.</span><span class="sxs-lookup"><span data-stu-id="b529a-124">The *calling convention type paramname* can include up to two leading underscores.</span></span>

<span data-ttu-id="b529a-125">La lista de parámetros es una lista delimitada por comas de:</span><span class="sxs-lookup"><span data-stu-id="b529a-125">The parameter list is a comma-delimited list of:</span></span>

<span data-ttu-id="b529a-126">\[*sus*\]</span><span class="sxs-lookup"><span data-stu-id="b529a-126">\[*attributes*\]</span></span>

<span data-ttu-id="b529a-127">El tipo puede ser cualquier tipo declarado previamente o tipo integrado, un puntero a cualquier tipo o un puntero a un tipo integrado.</span><span class="sxs-lookup"><span data-stu-id="b529a-127">The type can be any previously declared type or built-in type, a pointer to any type, or a pointer to a built-in type.</span></span> <span data-ttu-id="b529a-128">Los atributos de los parámetros son:</span><span class="sxs-lookup"><span data-stu-id="b529a-128">Attributes on parameters are:</span></span>

<span data-ttu-id="b529a-129">\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**opcional**](optional.md) \] .</span><span class="sxs-lookup"><span data-stu-id="b529a-129">\[[**in**](in.md)\], \[[**out**](out-idl.md)\], \[[**optional**](optional.md)\].</span></span>

<span data-ttu-id="b529a-130">Si \[ [](optional.md) \] se utiliza opcional, los tipos de esos parámetros deben ser **variantes** o **variantes** \* .</span><span class="sxs-lookup"><span data-stu-id="b529a-130">If \[[**optional**](optional.md)\] is used, the types of those parameters must be **VARIANT** or **VARIANT**\*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b529a-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b529a-131">Remarks</span></span>

<span data-ttu-id="b529a-132">La salida del archivo de encabezado (. h) para los módulos es una serie de prototipos de función.</span><span class="sxs-lookup"><span data-stu-id="b529a-132">The header file (.h) output for modules is a series of function prototypes.</span></span> <span data-ttu-id="b529a-133">La palabra clave **Module** y los corchetes adyacentes se quitan de la salida del archivo de encabezado (. h), pero se inserta un Comentario (// **módulo** *ModuleName*) antes que los prototipos.</span><span class="sxs-lookup"><span data-stu-id="b529a-133">The **module** keyword and surrounding brackets are stripped from the header (.h) file output, but a comment (// **module** *modulename*) is inserted before the prototypes.</span></span> <span data-ttu-id="b529a-134">La palabra clave **extern** se inserta antes que las declaraciones.</span><span class="sxs-lookup"><span data-stu-id="b529a-134">The keyword **extern** is inserted before the declarations.</span></span>

## <a name="examples"></a><span data-ttu-id="b529a-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b529a-135">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a><span data-ttu-id="b529a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b529a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b529a-137">**const**</span><span class="sxs-lookup"><span data-stu-id="b529a-137">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="b529a-138">Contenido de una biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b529a-138">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="b529a-139">**DllName**</span><span class="sxs-lookup"><span data-stu-id="b529a-139">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="b529a-140">**movimientos**</span><span class="sxs-lookup"><span data-stu-id="b529a-140">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="b529a-141">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="b529a-141">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="b529a-142">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="b529a-142">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="b529a-143">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="b529a-143">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="b529a-144">**plusvalía**</span><span class="sxs-lookup"><span data-stu-id="b529a-144">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="b529a-145">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="b529a-145">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b529a-146">**propget**</span><span class="sxs-lookup"><span data-stu-id="b529a-146">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="b529a-147">**PROPPUT**</span><span class="sxs-lookup"><span data-stu-id="b529a-147">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="b529a-148">**PROPPUTREF**</span><span class="sxs-lookup"><span data-stu-id="b529a-148">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="b529a-149">**string**</span><span class="sxs-lookup"><span data-stu-id="b529a-149">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="b529a-150">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="b529a-150">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="b529a-151">**uuid**</span><span class="sxs-lookup"><span data-stu-id="b529a-151">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="b529a-152">**vararg**</span><span class="sxs-lookup"><span data-stu-id="b529a-152">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="b529a-153">**Versión**</span><span class="sxs-lookup"><span data-stu-id="b529a-153">**version**</span></span>](version.md)
</dt> </dl>

 

 