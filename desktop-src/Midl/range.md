---
title: range (atributo)
description: El atributo \ Range \ permite especificar un intervalo de valores permitidos para los argumentos o campos cuyos valores se establecen en tiempo de ejecución. Cuando se usa con un tipo de canalización, el atributo especifica el intervalo permitido para el recuento de elementos de los fragmentos de la canalización.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- atributo de intervalo MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665785"
---
# <a name="range-attribute"></a><span data-ttu-id="856d6-105">range (atributo)</span><span class="sxs-lookup"><span data-stu-id="856d6-105">range attribute</span></span>

<span data-ttu-id="856d6-106">El atributo **\[ Range \]** permite especificar un intervalo de valores permitidos para los argumentos o campos cuyos valores se establecen en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="856d6-106">The **\[range\]** attribute lets you specify a range of allowable values for arguments or fields whose values are set at run time.</span></span> <span data-ttu-id="856d6-107">Cuando se usa con un tipo de canalización, el atributo especifica el intervalo permitido para el recuento de elementos de los fragmentos de la canalización.</span><span class="sxs-lookup"><span data-stu-id="856d6-107">When used with a pipe type, the attribute specifies the allowable range for the count of elements in the pipe chunks.</span></span>

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a><span data-ttu-id="856d6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="856d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="856d6-109">*bajo-Val*</span><span class="sxs-lookup"><span data-stu-id="856d6-109">*low-val*</span></span> 
</dt> <dd>

<span data-ttu-id="856d6-110">El valor mínimo permitido que puede contener el parámetro o el campo.</span><span class="sxs-lookup"><span data-stu-id="856d6-110">The lowest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="856d6-111">*alto-Val*</span><span class="sxs-lookup"><span data-stu-id="856d6-111">*high-val*</span></span> 
</dt> <dd>

<span data-ttu-id="856d6-112">Valor máximo permitido que puede contener el parámetro o el campo.</span><span class="sxs-lookup"><span data-stu-id="856d6-112">The highest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="856d6-113">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="856d6-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="856d6-114">Un tipo entero distinto de [**Hyper**](hyper.md) o [**\_ \_ Int64**](--int64.md), un identificador de tipo de un tipo entero, un tipo de [**enumeración**](enum.md) o un nombre de tipo de canalización.</span><span class="sxs-lookup"><span data-stu-id="856d6-114">An integral type other than [**hyper**](hyper.md) or [**\_\_int64**](--int64.md), a type identifier to an integral type, an [**enum**](enum.md) type, or a pipe type name.</span></span>

</dd> <dt>

<span data-ttu-id="856d6-115">*clara*</span><span class="sxs-lookup"><span data-stu-id="856d6-115">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="856d6-116">Un declarador estándar de C, como un identificador.</span><span class="sxs-lookup"><span data-stu-id="856d6-116">A standard C declarator, such as an identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="856d6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="856d6-117">Remarks</span></span>

<span data-ttu-id="856d6-118">Use el atributo **\[ Range \]** para modificar el significado de los parámetros o campos confidenciales, como los que se usan para el tamaño o la longitud, con matrices compatibles o variables, o siempre que desee comprobar un valor de parámetro o campo con respecto a un intervalo de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="856d6-118">Use the **\[range\]** attribute to modify the meaning of sensitive parameters or fields, such as those used for size or length, with conformant or varying arrays; or whenever you want to check a parameter or field value against a range of valid values.</span></span> <span data-ttu-id="856d6-119">El atributo se aplica a los parámetros de nivel superior, así como a los campos y parámetros de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="856d6-119">The attribute is applicable to top-level parameters as well as lower-level parameters and fields.</span></span> <span data-ttu-id="856d6-120">Agregar el atributo de **\[ intervalo \]** a un tipo no cambia su formato de conexión, por lo que no afecta a la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="856d6-120">Adding the **\[range\]** attribute to a type does not change its wire format, thus does not affect backward compatibility.</span></span>

<span data-ttu-id="856d6-121">El atributo **\[ Range \]** también se puede utilizar en datos compatibles, como búferes o matrices con un atributo de conformidad.</span><span class="sxs-lookup"><span data-stu-id="856d6-121">The **\[range\]** attribute can also be used on conformant data such as buffers or arrays with a conformance attribute.</span></span> <span data-ttu-id="856d6-122">El efecto es limitar todos los tamaños de conformidad para los datos compatibles con el intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="856d6-122">The effect is to limit all conformance sizes for the conformant data to the specified range.</span></span> <span data-ttu-id="856d6-123">Si los datos conformes son una matriz multidimensional, cada dimensión de la matriz se limita al intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="856d6-123">If the conformant data is a multi-dimensional array, each array dimension is limited to the specified range.</span></span>

<span data-ttu-id="856d6-124">El uso del **\[ intervalo \]** en los datos conformes requiere que el destino de compilación sea â € "Target NT60 o superior.</span><span class="sxs-lookup"><span data-stu-id="856d6-124">Use of **\[range\]** on conformant data requires that the compilation target be â€“target NT60 or higher.</span></span>

<span data-ttu-id="856d6-125">Tenga en cuenta que debe utilizar la opción del compilador [**/Robust**](-robust.md) al compilar el archivo IDL para generar el código auxiliar que realizará estas comprobaciones.</span><span class="sxs-lookup"><span data-stu-id="856d6-125">Note that you must use the [**/robust**](-robust.md) compiler option when you compile your IDL file in order to generate the stub code that will perform these checks.</span></span> <span data-ttu-id="856d6-126">Sin el modificador **/Robust** , el compilador MIDL omite este atributo.</span><span class="sxs-lookup"><span data-stu-id="856d6-126">Without the **/robust** switch, the MIDL compiler ignores this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="856d6-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="856d6-127">Examples</span></span>

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a><span data-ttu-id="856d6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="856d6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="856d6-129">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="856d6-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="856d6-130">matrices</span><span class="sxs-lookup"><span data-stu-id="856d6-130">arrays</span></span>](/windows/desktop/Rpc/arrays)
</dt> <dt>

[<span data-ttu-id="856d6-131">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="856d6-131">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="856d6-132">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="856d6-132">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="856d6-133">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="856d6-133">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="856d6-134">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="856d6-134">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="856d6-135">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="856d6-135">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="856d6-136">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="856d6-136">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="856d6-137">**el modificador \_ es**</span><span class="sxs-lookup"><span data-stu-id="856d6-137">**switch\_is**</span></span>](switch-is.md)
</dt> </dl>

 

 