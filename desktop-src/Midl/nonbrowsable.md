---
title: nonbrowsable (atributo)
description: Utilice el atributo \ nonbrowsableable \ para etiquetar un miembro de interfaz o dispinterface que no se debe mostrar en un explorador de propiedades.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- MIDL de atributo no explorable
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995153"
---
# <a name="nonbrowsable-attribute"></a><span data-ttu-id="a7cb0-104">nonbrowsable (atributo)</span><span class="sxs-lookup"><span data-stu-id="a7cb0-104">nonbrowsable attribute</span></span>

<span data-ttu-id="a7cb0-105">Use el atributo **\[ nonbrowsable \]** para etiquetar un miembro de interfaz o dispinterface que no se debe mostrar en un explorador de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-105">Use the **\[nonbrowsable\]** attribute to tag an interface or dispinterface member that should not be displayed in a properties browser.</span></span>

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="a7cb0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7cb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7cb0-107">*Property-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="a7cb0-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a7cb0-108">Otros atributos que se aplican a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="a7cb0-109">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="a7cb0-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a7cb0-110">Tipo de los datos devueltos por el método.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-110">The type of the data returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="a7cb0-111">*nombre de propiedad*</span><span class="sxs-lookup"><span data-stu-id="a7cb0-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a7cb0-112">Nombre de la propiedad o del método.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-112">The name of the property or method.</span></span>

</dd> <dt>

<span data-ttu-id="a7cb0-113">*prop-param-List*</span><span class="sxs-lookup"><span data-stu-id="a7cb0-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a7cb0-114">Cero o más parámetros que se van a pasar al método.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-114">Zero or more parameters to be passed to the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7cb0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7cb0-115">Remarks</span></span>

<span data-ttu-id="a7cb0-116">Algunas propiedades no deben mostrarse en un explorador de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-116">Certain properties should not be displayed in a properties browser.</span></span> <span data-ttu-id="a7cb0-117">Esto puede deberse a que la recuperación del valor tardaría mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-117">This may be because retrieving the value would take a very long time.</span></span> <span data-ttu-id="a7cb0-118">En el ejemplo se impide que el usuario intente recuperar la propiedad *Count* , que devuelve el número de filas del conjunto de registros dinámico. Este número puede representar los resultados de una consulta muy grande.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-118">The example prevents the user from attempting to retrieve the *Count* property, which returns the number of rows in the dynaset.This number may represent the results of a very large query.</span></span>

<span data-ttu-id="a7cb0-119">Otras propiedades pueden tener efectos inesperados en el explorador.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-119">Other properties may have unexpected effects on the browser.</span></span> <span data-ttu-id="a7cb0-120">Por ejemplo, considere un control con la propiedad "IsSelected" para saber si el control está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-120">For example, consider a control with the property "IsSelected" to tell whether the control is selected.</span></span> <span data-ttu-id="a7cb0-121">Si "IsSelected" está establecido en false, un explorador de propiedades basado en la selección examinará un objeto diferente.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-121">If "IsSelected" is set to false, a selection-based properties browser will browse a different object.</span></span>

<span data-ttu-id="a7cb0-122">Tenga en cuenta que una propiedad etiquetada como **\[ nonbrowsable \]** seguirá apareciendo en un examinador de objetos, que no muestra los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-122">Note that a property tagged as **\[nonbrowsable\]** will still appear in an object browser, which does not show property values.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="a7cb0-123">Representación Typeflag</span><span class="sxs-lookup"><span data-stu-id="a7cb0-123">Typeflag Representation</span></span>

<span data-ttu-id="a7cb0-124">La presencia de FUNCFLAG \_ FNONBROWSABLE o VARFLAG \_ FNONBROWSABLE.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-124">The presence of FUNCFLAG\_FNONBROWSABLE or VARFLAG\_FNONBROWSABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="a7cb0-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a7cb0-125">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a><span data-ttu-id="a7cb0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7cb0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7cb0-127">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="a7cb0-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="a7cb0-128">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="a7cb0-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="a7cb0-129">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="a7cb0-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 