---
title: atributo proxy
description: El atributo \ proxy \ impide que la automatización se registre como un controlador de proxy o código auxiliar para una interfaz dual.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- atributo de proxy MIDL
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487542"
---
# <a name="proxy-attribute"></a><span data-ttu-id="03f98-104">atributo proxy</span><span class="sxs-lookup"><span data-stu-id="03f98-104">proxy attribute</span></span>

<span data-ttu-id="03f98-105">El atributo **\[ proxy \]** impide que la automatización se registre como un controlador de proxy o código auxiliar para una interfaz dual.</span><span class="sxs-lookup"><span data-stu-id="03f98-105">The **\[proxy\]** attribute prevents Automation from registering as a proxy/stub handler for a dual interface.</span></span>

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="03f98-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03f98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03f98-107">*cadena: UUID*</span><span class="sxs-lookup"><span data-stu-id="03f98-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="03f98-108">Especifica una cadena que consta de 8 dígitos hexadecimales seguidos de un guion y, a continuación, tres grupos de 4 dígitos hexadecimales, seguidos de un guion y 12 dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="03f98-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="03f98-109">Puede incluir la cadena UUID entre comillas, excepto cuando se usa el modificador de compilador MIDL [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="03f98-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f98-110">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="03f98-110">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="03f98-111">Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="03f98-111">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="03f98-112">Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="03f98-112">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="03f98-113">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="03f98-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="03f98-114">Nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="03f98-114">Name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="03f98-115">*interfaz base*</span><span class="sxs-lookup"><span data-stu-id="03f98-115">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="03f98-116">Especifica el nombre de una interfaz de la que esta interfaz derivada hereda las funciones miembro, los códigos de estado y los atributos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="03f98-116">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="03f98-117">La interfaz derivada no hereda las definiciones de tipo.</span><span class="sxs-lookup"><span data-stu-id="03f98-117">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="03f98-118">Para ello, use la palabra clave [**Import**](import.md) para importar el archivo IDL de la interfaz base.</span><span class="sxs-lookup"><span data-stu-id="03f98-118">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03f98-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03f98-119">Remarks</span></span>

<span data-ttu-id="03f98-120">El uso del \[ atributo **proxy** \] para una interfaz dual impide que el TLB tome el código auxiliar generado.</span><span class="sxs-lookup"><span data-stu-id="03f98-120">Using the \[ **proxy**\] attribute for a dual interface prevents the TLB from taking over generated stubs.</span></span> <span data-ttu-id="03f98-121">Si se especifica este atributo, no se debe anular el registro del proxy typelib cuando se anula el registro de typelib.</span><span class="sxs-lookup"><span data-stu-id="03f98-121">If this attribute is specified, the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

### <a name="flags"></a><span data-ttu-id="03f98-122">Marcas</span><span class="sxs-lookup"><span data-stu-id="03f98-122">Flags</span></span>

<dl> <dt>

<span data-ttu-id="03f98-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>\_proxy TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="03f98-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="03f98-124">Las interfaces se pueden marcar con la \_ marca del proxy TYPEFLAG para indicar que van a usar una biblioteca de vínculos dinámicos de proxy/código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="03f98-124">Interfaces can be marked with the TYPEFLAG\_PROXY flag to indicate they will be using a proxy/stub dynamic link library.</span></span> <span data-ttu-id="03f98-125">Esta marca especifica que no se debe anular el registro del proxy de la biblioteca de bibliotecas cuando se anula el registro de la biblioteca de bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="03f98-125">This flag specifies the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="03f98-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="03f98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f98-127">**Generar una biblioteca de tipos con MIDL**</span><span class="sxs-lookup"><span data-stu-id="03f98-127">**Generating a Type Library with MIDL**</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="03f98-128">**BI**</span><span class="sxs-lookup"><span data-stu-id="03f98-128">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="03f98-129">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="03f98-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 