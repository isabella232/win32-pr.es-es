---
title: defaultvtable (atributo)
description: El atributo \ defaultvtable \ define una interfaz como la interfaz vtable predeterminada.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- defaultvtable (atributo) MIDL
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904574"
---
# <a name="defaultvtable-attribute"></a><span data-ttu-id="bfa80-104">defaultvtable (atributo)</span><span class="sxs-lookup"><span data-stu-id="bfa80-104">defaultvtable attribute</span></span>

<span data-ttu-id="bfa80-105">El atributo **\[ defaultvtable \]** define una interfaz como la interfaz vtable predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bfa80-105">The **\[defaultvtable\]** attribute defines an interface as the default Vtable interface.</span></span>

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="bfa80-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfa80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa80-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="bfa80-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bfa80-108">Otros atributos que se aplican a la clase.</span><span class="sxs-lookup"><span data-stu-id="bfa80-108">Other attributes that apply to the class.</span></span> <span data-ttu-id="bfa80-109">Los **\[** atributos [**source**](source.md) **\]** y **\[** [**UUID**](uuid.md) **\]** son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="bfa80-109">The **\[**[**source**](source.md)**\]** and **\[**[**uuid**](uuid.md)**\]** attributes are required.</span></span>

</dd> <dt>

<span data-ttu-id="bfa80-110">*nombre de coclase*</span><span class="sxs-lookup"><span data-stu-id="bfa80-110">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bfa80-111">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="bfa80-111">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="bfa80-112">*coclass-interface-List*</span><span class="sxs-lookup"><span data-stu-id="bfa80-112">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bfa80-113">Una lista de interfaces para la clase.</span><span class="sxs-lookup"><span data-stu-id="bfa80-113">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfa80-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfa80-114">Remarks</span></span>

<span data-ttu-id="bfa80-115">Una interfaz vtable predeterminada no puede ser una dispinterface; debe ser una interfaz dual o vtable o una interfaz.</span><span class="sxs-lookup"><span data-stu-id="bfa80-115">A default Vtable interface cannot be a dispinterface—it must be a dual or Vtable or interface.</span></span> <span data-ttu-id="bfa80-116">Si la interfaz es una interfaz dual, los receptores pueden suponer que recibirán eventos a través de vtable.</span><span class="sxs-lookup"><span data-stu-id="bfa80-116">If the interface is a dual interface, then sinks can assume that they will receive events through Vtable.</span></span>

<span data-ttu-id="bfa80-117">Una clase puede ser tanto una interfaz de origen predeterminada como una interfaz de origen vtable predeterminada, como se muestra en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bfa80-117">A class can be both a default source interface and a default Vtable source interface as shown in the example.</span></span> <span data-ttu-id="bfa80-118">En este caso, un receptor de notificaciones debe utilizar IID \_ IDISPATCH para recibir los eventos de envío y usar el identificador de interfaz para recibir los eventos de vtable.</span><span class="sxs-lookup"><span data-stu-id="bfa80-118">In this case an advise sink should use IID\_IDISPATCH to receive dispatch events and use the interface identifier to receive Vtable events.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="bfa80-119">Representación Typeflag</span><span class="sxs-lookup"><span data-stu-id="bfa80-119">Typeflag Representation</span></span>

<span data-ttu-id="bfa80-120">La presencia de IMPLTYPEFLAG \_ FDEFAULTVTABLE.</span><span class="sxs-lookup"><span data-stu-id="bfa80-120">The presence of IMPLTYPEFLAG\_FDEFAULTVTABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="bfa80-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bfa80-121">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="bfa80-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfa80-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa80-123">**coclase**</span><span class="sxs-lookup"><span data-stu-id="bfa80-123">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="bfa80-124">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="bfa80-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="bfa80-125">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="bfa80-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="bfa80-126">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="bfa80-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="bfa80-127">**fuentes**</span><span class="sxs-lookup"><span data-stu-id="bfa80-127">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="bfa80-128">**uuid**</span><span class="sxs-lookup"><span data-stu-id="bfa80-128">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 