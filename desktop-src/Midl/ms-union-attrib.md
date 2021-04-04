---
title: ms_union (atributo)
description: La palabra clave \ MS \_ Union \ se utiliza para controlar la alineación del NDR de las uniones no encapsuladas.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union el atributo MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076576"
---
# <a name="ms_union-attribute"></a><span data-ttu-id="7e155-104">atributo de unión de MS \_</span><span class="sxs-lookup"><span data-stu-id="7e155-104">ms\_union attribute</span></span>

<span data-ttu-id="7e155-105">La palabra clave \[ **MS \_ Union** \] se utiliza para controlar la alineación del NDR de las uniones no encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="7e155-105">The keyword \[**ms\_union**\] is used to control the NDR alignment of nonencapsulated unions.</span></span>

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a><span data-ttu-id="7e155-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e155-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e155-107">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="7e155-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7e155-108">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7e155-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="7e155-109">*tipo de procedimiento*</span><span class="sxs-lookup"><span data-stu-id="7e155-109">*procedure-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7e155-110">Especifica el tipo de valor devuelto del procedimiento al que se aplica el atributo.</span><span class="sxs-lookup"><span data-stu-id="7e155-110">Specifies the return type of the procedure to which the attribute is being applied.</span></span>

</dd> <dt>

<span data-ttu-id="7e155-111">*procedimiento: nombre*</span><span class="sxs-lookup"><span data-stu-id="7e155-111">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7e155-112">Especifica el nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="7e155-112">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="7e155-113">*lista de parámetros*</span><span class="sxs-lookup"><span data-stu-id="7e155-113">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7e155-114">Especifica la lista de parámetros del procedimiento, que puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="7e155-114">Specifies the procedure's parameter list, which may be empty.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e155-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e155-115">Remarks</span></span>

<span data-ttu-id="7e155-116">No utilice nunca este modificador o atributo con nuevas interfaces.</span><span class="sxs-lookup"><span data-stu-id="7e155-116">Never use this switch or attribute with new interfaces.</span></span> <span data-ttu-id="7e155-117">Esta es solo una característica de compatibilidad con versiones anteriores. El compilador MIDL en esta versión de Microsoft RPC refleja el comportamiento del compilador de OSF DCE IDL para uniones no encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="7e155-117">This is a backward compatibility feature only.The MIDL compiler in this version of Microsoft RPC mirrors the behavior of the OSF DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="7e155-118">Sin embargo, dado que las versiones anteriores del compilador de MIDL no lo hacían, el modificador [**/MS \_ Union**](-ms-union.md) proporciona compatibilidad con las interfaces creadas en versiones anteriores del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="7e155-118">However, because earlier versions of the MIDL compiler did not do so, the [**/ms\_union**](-ms-union.md) switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="7e155-119">La característica **MS \_ Union** se puede usar como un atributo de interfaz IDL, un atributo de tipo IDL o como un modificador de la línea de comandos ( [**/MS \_ Union**](-ms-union.md)).</span><span class="sxs-lookup"><span data-stu-id="7e155-119">The **ms\_union** feature can be used as an IDL interface attribute, an IDL type attribute, or as a command-line switch ( [**/ms\_union**](-ms-union.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="7e155-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7e155-120">Examples</span></span>

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a><span data-ttu-id="7e155-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e155-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e155-122">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="7e155-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7e155-123">**\_Unión/MS**</span><span class="sxs-lookup"><span data-stu-id="7e155-123">**/ms\_union**</span></span>](-ms-union.md)
</dt> </dl>

 

 




