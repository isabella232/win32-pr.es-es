---
title: coclass (atributo)
description: La instrucción coclass proporciona una lista de las interfaces admitidas para un objeto de componente.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- atributo de coclase MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420649"
---
# <a name="coclass-attribute"></a><span data-ttu-id="5dc7a-104">coclass (atributo)</span><span class="sxs-lookup"><span data-stu-id="5dc7a-104">coclass attribute</span></span>

<span data-ttu-id="5dc7a-105">La instrucción **CoClass** proporciona una lista de las interfaces admitidas para un objeto de componente.</span><span class="sxs-lookup"><span data-stu-id="5dc7a-105">The **coclass** statement provides a listing of the supported interfaces for a component object.</span></span>

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a><span data-ttu-id="5dc7a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5dc7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dc7a-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5dc7a-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc7a-108">El **\[** atributo [**UUID**](uuid.md) **\]** es necesario en una **coclase**.</span><span class="sxs-lookup"><span data-stu-id="5dc7a-108">The **\[**[**uuid**](uuid.md)**\]** attribute is required on a **coclass**.</span></span> <span data-ttu-id="5dc7a-109">Es el mismo **\[ UUID \]** que se registra como CLSID en la base de datos de registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="5dc7a-109">This is the same **\[uuid\]** that is registered as a CLSID in the system registration database.</span></span> <span data-ttu-id="5dc7a-110">Los **\[** atributos [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**licensed**](licensed.md) **\]** , **\[** [**version**](version.md) **\]** , **\[** [**control**](control.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** y **\[** [**appobject**](appobject.md) **\]** se aceptan, pero no es necesario, antes de una definición de **coclase** .</span><span class="sxs-lookup"><span data-stu-id="5dc7a-110">The **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**licensed**](licensed.md)**\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, and **\[**[**appobject**](appobject.md)**\]** attributes are accepted, but not required, before a **coclass** definition.</span></span>

</dd> <dt>

<span data-ttu-id="5dc7a-111">*classname*</span><span class="sxs-lookup"><span data-stu-id="5dc7a-111">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc7a-112">Nombre por el que se conoce el objeto común en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="5dc7a-112">Name by which the common object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="5dc7a-113">*interfaz: atributos*</span><span class="sxs-lookup"><span data-stu-id="5dc7a-113">*interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc7a-114">Atributos opcionales para la interfaz o dispinterface.</span><span class="sxs-lookup"><span data-stu-id="5dc7a-114">Optional attributes for the interface or dispinterface.</span></span> <span data-ttu-id="5dc7a-115">Los **\[** atributos [**source**](source.md) **\]** , **\[** [**default**](default.md) **\]** y **\[** [**Restricted**](restricted.md) **\]** se aceptan en una interfaz o dispinterface dentro de una **coclase**.</span><span class="sxs-lookup"><span data-stu-id="5dc7a-115">The **\[**[**source**](source.md)**\]**, **\[**[**default**](default.md)**\]**, and **\[**[**restricted**](restricted.md)**\]** attributes are accepted on an interface or dispinterface within a **coclass**.</span></span>

</dd> <dt>

<span data-ttu-id="5dc7a-116">*interfaz*</span><span class="sxs-lookup"><span data-stu-id="5dc7a-116">*interfacename*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc7a-117">Una interfaz declarada con la palabra clave [**interface**](interface.md) o una dispinterface declarada con la palabra clave [**dispinterface**](dispinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="5dc7a-117">Either an interface declared with the [**interface**](interface.md) keyword, or a dispinterface declared with the [**dispinterface**](dispinterface.md) keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dc7a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5dc7a-118">Remarks</span></span>

<span data-ttu-id="5dc7a-119">El modelo de objetos componentes de Microsoft define una clase como una implementación de que permite **QueryInterface** entre un conjunto de interfaces.</span><span class="sxs-lookup"><span data-stu-id="5dc7a-119">The Microsoft Component Object Model defines a class as an implementation that allows **QueryInterface** between a set of interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="5dc7a-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5dc7a-120">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a><span data-ttu-id="5dc7a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5dc7a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc7a-122">**appobject**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-122">**appobject**</span></span>](appobject.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-123">**control**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-123">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-124">**predeterminada**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-124">**default**</span></span>](default.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-126">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="5dc7a-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-127">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="5dc7a-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="5dc7a-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-129">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-129">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-130">**plusvalía**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-130">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-131">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-132">**bajo**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-132">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-133">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="5dc7a-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="5dc7a-134">**Restrict**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-134">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-135">**fuentes**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-135">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-136">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="5dc7a-136">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="5dc7a-137">**uuid**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-137">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="5dc7a-138">**Versión**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-138">**version**</span></span>](version.md)
</dt> </dl>

 

 