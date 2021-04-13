---
title: uidefault (atributo)
description: El atributo \ uidefault \ indica que el miembro de información de tipo es el miembro predeterminado que se va a mostrar en la interfaz de usuario.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- uidefault (atributo) MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420568"
---
# <a name="uidefault-attribute"></a><span data-ttu-id="8c0db-104">uidefault (atributo)</span><span class="sxs-lookup"><span data-stu-id="8c0db-104">uidefault attribute</span></span>

<span data-ttu-id="8c0db-105">El atributo **\[ uidefault \]** indica que el miembro de información de tipo es el miembro predeterminado que se va a mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8c0db-105">The **\[uidefault\]** attribute indicates that the type information member is the default member for display in the user interface.</span></span>

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="8c0db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c0db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c0db-107">*lista de atributos de método*</span><span class="sxs-lookup"><span data-stu-id="8c0db-107">*method-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0db-108">Otros atributos que se aplican al método.</span><span class="sxs-lookup"><span data-stu-id="8c0db-108">Other attributes that apply to the method.</span></span>

</dd> <dt>

<span data-ttu-id="8c0db-109">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="8c0db-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0db-110">El tipo de los datos que el método devolverá cuando finalice la ejecución.</span><span class="sxs-lookup"><span data-stu-id="8c0db-110">The type of the data that the method will return when it finishes execution.</span></span>

</dd> <dt>

<span data-ttu-id="8c0db-111">*nombre del método*</span><span class="sxs-lookup"><span data-stu-id="8c0db-111">*method-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0db-112">Nombre del método.</span><span class="sxs-lookup"><span data-stu-id="8c0db-112">The name of the method.</span></span>

</dd> <dt>

<span data-ttu-id="8c0db-113">*lista de parámetros de método*</span><span class="sxs-lookup"><span data-stu-id="8c0db-113">*method-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0db-114">Cero o más parámetros para el método.</span><span class="sxs-lookup"><span data-stu-id="8c0db-114">Zero or more parameters for the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c0db-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c0db-115">Remarks</span></span>

<span data-ttu-id="8c0db-116">Al aplicar el atributo **\[ uidefault \]** a un miembro de una interfaz o una interfaz dispinterface se indica Visual Basic, en tiempo de diseño, para mostrar automáticamente este evento o propiedad al usuario.</span><span class="sxs-lookup"><span data-stu-id="8c0db-116">Applying the **\[uidefault\]** attribute to a member of an interface or a dispinterface tells Visual Basic, at design-time, to automatically display this event or property to the user.</span></span> <span data-ttu-id="8c0db-117">Esto significa que cuando el usuario hace doble clic en un objeto, Visual Basic salta al evento en la interfaz de origen predeterminada que tiene el atributo **\[ uidefault \]** .</span><span class="sxs-lookup"><span data-stu-id="8c0db-117">This means that when the user double-clicks an object, Visual Basic jumps to the event in the default source interface that has the **\[uidefault\]** attribute.</span></span> <span data-ttu-id="8c0db-118">Cuando el usuario selecciona un objeto, el explorador de propiedades de Visual Basic muestra la propiedad en la interfaz de origen predeterminada que tiene este atributo.</span><span class="sxs-lookup"><span data-stu-id="8c0db-118">When the user selects an object, Visual Basic's Properties browser displays the property in the default source interface that has this attribute.</span></span> <span data-ttu-id="8c0db-119">Si ningún evento o propiedad tiene el atributo **\[ uidefault \]** , Visual Basic muestra el primer evento o propiedad enumerados en la interfaz predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8c0db-119">If no event or property has the **\[uidefault\]** attribute, Visual Basic displays the first event or property listed in the default interface.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="8c0db-120">Representación Typeflag</span><span class="sxs-lookup"><span data-stu-id="8c0db-120">Typeflag Representation</span></span>

<span data-ttu-id="8c0db-121">La presencia de FUNCFLAG \_ FUIDEFAULT o VARFLAG \_ FUIDEFAULT</span><span class="sxs-lookup"><span data-stu-id="8c0db-121">The presence of FUNCFLAG\_FUIDEFAULT or VARFLAG\_FUIDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="8c0db-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8c0db-122">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="8c0db-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c0db-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0db-124">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="8c0db-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="8c0db-125">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="8c0db-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="8c0db-126">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="8c0db-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 