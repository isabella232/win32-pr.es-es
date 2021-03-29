---
title: atributo dual
description: El atributo dual identifica una interfaz que expone propiedades y métodos a través de IDispatch y directamente a través de VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- MIDL de atributo dual
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995236"
---
# <a name="dual-attribute"></a><span data-ttu-id="f5566-104">atributo dual</span><span class="sxs-lookup"><span data-stu-id="f5566-104">dual attribute</span></span>

<span data-ttu-id="f5566-105">El atributo **dual** identifica una interfaz que expone propiedades y métodos a través de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y directamente a través de VTBL.</span><span class="sxs-lookup"><span data-stu-id="f5566-105">The **dual** attribute identifies an interface that exposes properties and methods through [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and directly through the VTBL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="f5566-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5566-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5566-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="f5566-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="f5566-108">Especifica un número de identificación único universal para la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f5566-108">Specifies a universally unique identification number for the interface</span></span>

</dd> <dt>

<span data-ttu-id="f5566-109">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="f5566-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5566-110">Especifica una lista de cero o más atributos MIDL adicionales.</span><span class="sxs-lookup"><span data-stu-id="f5566-110">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f5566-111">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="f5566-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f5566-112">Nombre de la interfaz a la que se aplicará el atributo **dual** .</span><span class="sxs-lookup"><span data-stu-id="f5566-112">The name of the interface to which the **dual** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5566-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5566-113">Remarks</span></span>

<span data-ttu-id="f5566-114">Las interfaces identificadas por el atributo **dual** deben ser compatibles con la automatización y derivarse de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span><span class="sxs-lookup"><span data-stu-id="f5566-114">Interfaces identified by the **dual** attribute must be compatible with Automation and be derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span> <span data-ttu-id="f5566-115">Este atributo no se permite en interfaces dispinterface.</span><span class="sxs-lookup"><span data-stu-id="f5566-115">This attribute is not allowed on dispinterfaces.</span></span>

<span data-ttu-id="f5566-116">El atributo **dual** crea una interfaz que es una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y una interfaz del modelo de objetos componentes (com).</span><span class="sxs-lookup"><span data-stu-id="f5566-116">The **dual** attribute creates an interface that is both an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface and a Component Object Model (COM) interface.</span></span> <span data-ttu-id="f5566-117">Las siete primeras entradas de VTBL para una interfaz dual son los siete miembros de **IDispatch** y las entradas restantes son para el acceso directo a los miembros de la interfaz dual.</span><span class="sxs-lookup"><span data-stu-id="f5566-117">The first seven entries of the VTBL for a dual interface are the seven members of **IDispatch**, and the remaining entries are for direct access to members of the dual interface.</span></span> <span data-ttu-id="f5566-118">Todos los parámetros y tipos devueltos especificados para los miembros de una interfaz dual deben ser tipos compatibles con la automatización.</span><span class="sxs-lookup"><span data-stu-id="f5566-118">All the parameters and return types specified for members of a dual interface must be Automation-compatible types.</span></span>

<span data-ttu-id="f5566-119">Todos los miembros de una interfaz dual deben pasar un HRESULT como el valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="f5566-119">All members of a dual interface must pass an HRESULT as the function return value.</span></span> <span data-ttu-id="f5566-120">Los miembros, como las funciones de descriptor de acceso de propiedades, que necesitan devolver otros valores, deben especificar el último parámetro como [**out**](out-idl.md), [**retval**](retval.md), que indica un parámetro de salida que devuelve el valor de la función.</span><span class="sxs-lookup"><span data-stu-id="f5566-120">Members, such as property accessor functions, that need to return other values, should specify the last parameter as [**out**](out-idl.md), [**retval**](retval.md), indicating an output parameter that returns the value of the function.</span></span> <span data-ttu-id="f5566-121">Además, los miembros que deben admitir varias configuraciones regionales deben pasar un parámetro [**LCID**](lcid.md) .</span><span class="sxs-lookup"><span data-stu-id="f5566-121">In addition, members that need to support multiple locales should pass an [**lcid**](lcid.md) parameter.</span></span>

<span data-ttu-id="f5566-122">Una interfaz dual proporciona tanto la velocidad del enlace VTBL directo como la flexibilidad del enlace [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="f5566-122">A dual interface provides for both the speed of direct VTBL binding and the flexibility of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) binding.</span></span> <span data-ttu-id="f5566-123">Por esta razón, siempre que sea posible, se recomienda usar interfaces duales.</span><span class="sxs-lookup"><span data-stu-id="f5566-123">For this reason, dual interfaces are recommended whenever possible.</span></span>

> [!Note]  
> <span data-ttu-id="f5566-124">Si la aplicación obtiene acceso a los datos de objeto mediante la conversión del puntero *this* dentro de la llamada de interfaz, debe comprobar los punteros VTBL en el objeto con sus propios punteros VTBL para asegurarse de que está conectado al proxy adecuado.</span><span class="sxs-lookup"><span data-stu-id="f5566-124">If your application accesses object data by casting the *this* pointer within the interface call, you should check the VTBL pointers in the object against your own VTBL pointers to ensure that you are connected to the appropriate proxy.</span></span>

 

<span data-ttu-id="f5566-125">Especificar **dual** en una interfaz implica que la interfaz es compatible con la automatización y, por consiguiente, hace que \_ se establezcan las marcas TYPEFLAG FDUAL y TYPEFLAG \_ FOLEAUTOMATION.</span><span class="sxs-lookup"><span data-stu-id="f5566-125">Specifying **dual** on an interface implies that the interface is compatible with Automation, and therefore causes both the TYPEFLAG\_FDUAL and TYPEFLAG\_FOLEAUTOMATION flags to be set.</span></span>

### <a name="flags"></a><span data-ttu-id="f5566-126">Marcas</span><span class="sxs-lookup"><span data-stu-id="f5566-126">Flags</span></span>

<span data-ttu-id="f5566-127">TYPEFLAG \_ FDUAL, TYPEFLAG \_ FOLEAUTOMATION</span><span class="sxs-lookup"><span data-stu-id="f5566-127">TYPEFLAG\_FDUAL, TYPEFLAG\_FOLEAUTOMATION</span></span>

## <a name="examples"></a><span data-ttu-id="f5566-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f5566-128">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a><span data-ttu-id="f5566-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5566-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5566-130">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="f5566-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f5566-131">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="f5566-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="f5566-132">**LCID**</span><span class="sxs-lookup"><span data-stu-id="f5566-132">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="f5566-133">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="f5566-133">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="f5566-134">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="f5566-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f5566-135">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="f5566-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f5566-136">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="f5566-136">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="f5566-137">**retval**</span><span class="sxs-lookup"><span data-stu-id="f5566-137">**retval**</span></span>](retval.md)
</dt> </dl>

 

 