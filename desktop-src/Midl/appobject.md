---
title: appobject (atributo)
description: El atributo \ appobject \ identifica la coclase como un objeto de aplicación, que está asociado a una aplicación EXE completa.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- appobject (atributo) MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420598"
---
# <a name="appobject-attribute"></a><span data-ttu-id="adf5b-104">appobject (atributo)</span><span class="sxs-lookup"><span data-stu-id="adf5b-104">appobject attribute</span></span>

<span data-ttu-id="adf5b-105">El atributo **\[ appobject \]** identifica la [**coclase**](coclass.md) como un objeto de aplicación, que está asociado a una aplicación exe completa.</span><span class="sxs-lookup"><span data-stu-id="adf5b-105">The **\[appobject\]** attribute identifies the [**coclass**](coclass.md) as an application object, which is associated with a full EXE application.</span></span>

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a><span data-ttu-id="adf5b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="adf5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf5b-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="adf5b-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="adf5b-108">Especifica un número de identificación único universal para la [**coclase**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="adf5b-108">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="adf5b-109">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="adf5b-109">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="adf5b-110">Especifica cero o más atributos que se aplican a la instrucción [**CoClass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="adf5b-110">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="adf5b-111">Los atributos **de coclase** permitidos son [**\[ HelpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), con [**\[ licencia \]**](licensed.md), [**\[ versión \]**](version.md), [**\[ control \]**](control.md)y [**\[ oculto \]**](hidden.md).</span><span class="sxs-lookup"><span data-stu-id="adf5b-111">Allowable **coclass** attributes are [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[licensed\]**](licensed.md), [**\[version\]**](version.md), [**\[control\]**](control.md), and [**\[hidden\]**](hidden.md).</span></span>

</dd> <dt>

<span data-ttu-id="adf5b-112">*classname*</span><span class="sxs-lookup"><span data-stu-id="adf5b-112">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="adf5b-113">Especifica el nombre por el que se conoce el objeto de componente en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="adf5b-113">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="adf5b-114">*definición de coclase*</span><span class="sxs-lookup"><span data-stu-id="adf5b-114">*coclass definition*</span></span> 
</dt> <dd>

<span data-ttu-id="adf5b-115">Especifica las instrucciones que componen la definición de [**coclase**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="adf5b-115">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adf5b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="adf5b-116">Remarks</span></span>

<span data-ttu-id="adf5b-117">El atributo **\[ appobject \]** también indica que las funciones y propiedades de la [**coclase**](coclass.md) están disponibles globalmente en la biblioteca de tipos actual.</span><span class="sxs-lookup"><span data-stu-id="adf5b-117">The **\[appobject\]** attribute also indicates that the functions and properties of the [**coclass**](coclass.md) are globally available in the current type library.</span></span>

<span data-ttu-id="adf5b-118">La representación typeflag para este atributo es TYPEFLAG \_ FAPPOBJECT</span><span class="sxs-lookup"><span data-stu-id="adf5b-118">The typeflag representation for this attribute is TYPEFLAG\_FAPPOBJECT</span></span>

## <a name="examples"></a><span data-ttu-id="adf5b-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="adf5b-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="adf5b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="adf5b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf5b-121">**coclase**</span><span class="sxs-lookup"><span data-stu-id="adf5b-121">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="adf5b-122">**control**</span><span class="sxs-lookup"><span data-stu-id="adf5b-122">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="adf5b-123">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="adf5b-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="adf5b-124">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="adf5b-124">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="adf5b-125">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="adf5b-125">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="adf5b-126">**plusvalía**</span><span class="sxs-lookup"><span data-stu-id="adf5b-126">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="adf5b-127">**bajo**</span><span class="sxs-lookup"><span data-stu-id="adf5b-127">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="adf5b-128">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="adf5b-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="adf5b-129">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="adf5b-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="adf5b-130">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="adf5b-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="adf5b-131">**Versión**</span><span class="sxs-lookup"><span data-stu-id="adf5b-131">**version**</span></span>](version.md)
</dt> </dl>

 

 