---
title: atributo con licencia
description: El atributo \ licensed \ indica que la coclase a la que se aplica tiene licencia y se debe crear una instancia de con IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- MIDL de atributo con licencia
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077621"
---
# <a name="licensed-attribute"></a><span data-ttu-id="631f8-104">atributo con licencia</span><span class="sxs-lookup"><span data-stu-id="631f8-104">licensed attribute</span></span>

<span data-ttu-id="631f8-105">El atributo con **\[ licencia \]** indica que la [**coclase**](coclass.md) a la que se aplica tiene licencia y se debe crear una instancia de ella mediante [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span><span class="sxs-lookup"><span data-stu-id="631f8-105">The **\[licensed\]** attribute indicates that the [**coclass**](coclass.md) to which it applies is licensed, and must be instantiated using [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span></span>

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a><span data-ttu-id="631f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="631f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="631f8-107">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="631f8-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="631f8-108">Especifica cero o más atributos que se aplican a la instrucción [**CoClass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="631f8-108">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="631f8-109">Los atributos de **coclase** permitidos son **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , con **\[ licencia \]**, **\[** [**versión**](version.md) **\]** , **\[** [**control**](control.md) **\]** y **\[** [**oculto**](hidden.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="631f8-109">Allowable **coclass** attributes are **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[licensed\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, and **\[**[**hidden**](hidden.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="631f8-110">*classname*</span><span class="sxs-lookup"><span data-stu-id="631f8-110">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="631f8-111">Especifica el nombre por el que se conoce el objeto de componente en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="631f8-111">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="631f8-112">*definición de coclases*</span><span class="sxs-lookup"><span data-stu-id="631f8-112">*coclass-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="631f8-113">Especifica las instrucciones que componen la definición de [**coclase**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="631f8-113">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="631f8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="631f8-114">Remarks</span></span>

<span data-ttu-id="631f8-115">La concesión de licencias es una característica de COM que proporciona control sobre la creación de objetos.</span><span class="sxs-lookup"><span data-stu-id="631f8-115">Licensing is a feature of COM that provides control over object creation.</span></span> <span data-ttu-id="631f8-116">Los objetos con licencia solo los pueden crear los clientes que tienen autorización para usarlos.</span><span class="sxs-lookup"><span data-stu-id="631f8-116">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="631f8-117">Las licencias se implementan en COM a través de la interfaz [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) y admiten una clave de licencia que se puede pasar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="631f8-117">Licensing is implemented in COM through the [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

### <a name="flags"></a><span data-ttu-id="631f8-118">Marcas</span><span class="sxs-lookup"><span data-stu-id="631f8-118">Flags</span></span>

<span data-ttu-id="631f8-119">TYPEFLAG \_ FLICENSED</span><span class="sxs-lookup"><span data-stu-id="631f8-119">TYPEFLAG\_FLICENSED</span></span>

## <a name="examples"></a><span data-ttu-id="631f8-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="631f8-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a><span data-ttu-id="631f8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="631f8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="631f8-122">**coclase**</span><span class="sxs-lookup"><span data-stu-id="631f8-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="631f8-123">Contenido de una biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="631f8-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="631f8-124">**control**</span><span class="sxs-lookup"><span data-stu-id="631f8-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="631f8-125">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="631f8-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="631f8-126">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="631f8-126">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="631f8-127">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="631f8-127">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="631f8-128">**plusvalía**</span><span class="sxs-lookup"><span data-stu-id="631f8-128">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="631f8-129">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="631f8-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="631f8-130">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="631f8-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="631f8-131">**Versión**</span><span class="sxs-lookup"><span data-stu-id="631f8-131">**version**</span></span>](version.md)
</dt> </dl>

 

 