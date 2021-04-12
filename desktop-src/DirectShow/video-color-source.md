---
description: Origen de color de vídeo
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Origen de color de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c751d74a78b027d50f033acb3709d18fe8f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277583"
---
# <a name="video-color-source"></a><span data-ttu-id="38bf6-103">Origen de color de vídeo</span><span class="sxs-lookup"><span data-stu-id="38bf6-103">Video Color Source</span></span>

> [!Note]  
> <span data-ttu-id="38bf6-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="38bf6-104">\[Deprecated.</span></span> <span data-ttu-id="38bf6-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38bf6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="38bf6-106">El origen de color de vídeo crea una imagen de vídeo continua de un color sólido.</span><span class="sxs-lookup"><span data-stu-id="38bf6-106">The Video Color Source creates a continuous video image of a solid color.</span></span>

<span data-ttu-id="38bf6-107">IDENTIFICADOR de clase (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span><span class="sxs-lookup"><span data-stu-id="38bf6-107">Class ID (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span></span>

<span data-ttu-id="38bf6-108">Nombre de la variable CLSID: **CLSID \_ ColorSource**</span><span class="sxs-lookup"><span data-stu-id="38bf6-108">CLSID Variable Name: **CLSID\_ColorSource**</span></span>

<span data-ttu-id="38bf6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38bf6-109">Properties</span></span>



| <span data-ttu-id="38bf6-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38bf6-110">Property</span></span> | <span data-ttu-id="38bf6-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="38bf6-111">Type</span></span>      | <span data-ttu-id="38bf6-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="38bf6-112">Default</span></span> | <span data-ttu-id="38bf6-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="38bf6-113">Description</span></span>                                   |
|----------|-----------|---------|-----------------------------------------------|
| <span data-ttu-id="38bf6-114">Color</span><span class="sxs-lookup"><span data-stu-id="38bf6-114">"Color"</span></span>  | <span data-ttu-id="38bf6-115">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="38bf6-115">**DWORD**</span></span> | <span data-ttu-id="38bf6-116">0</span><span class="sxs-lookup"><span data-stu-id="38bf6-116">0</span></span>       | <span data-ttu-id="38bf6-117">Especifica el color que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="38bf6-117">Specifies the color to generate.</span></span> <span data-ttu-id="38bf6-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="38bf6-118">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="38bf6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38bf6-119">Remarks</span></span>

<span data-ttu-id="38bf6-120">El origen de color de vídeo se usa con los objetos de origen.</span><span class="sxs-lookup"><span data-stu-id="38bf6-120">The Video Color Source is used with source objects.</span></span> <span data-ttu-id="38bf6-121">En primer lugar, cree un nuevo objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="38bf6-121">First, create a new source object.</span></span> <span data-ttu-id="38bf6-122">A continuación, establezca el GUID del subobjeto del objeto de origen en CLSID \_ ColorSource llamando al método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="38bf6-122">Then set the source object's subobject GUID to CLSID\_ColorSource, by calling the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="38bf6-123">Para establecer el color, cree un objeto [setter de propiedad](property-setter.md) y aplique la propiedad "color" en el tiempo cero.</span><span class="sxs-lookup"><span data-stu-id="38bf6-123">To set the color, create a [Property Setter](property-setter.md) object and apply the "Color" property at time zero.</span></span> <span data-ttu-id="38bf6-124">El valor de esta propiedad es un número hexadecimal con el formato *0xAARRGGBB*, donde *AA* es el valor alfa, *RR* es el valor rojo, *GG* es el valor verde y *BB* es el valor azul.</span><span class="sxs-lookup"><span data-stu-id="38bf6-124">The value of this property is a hexadecimal number with the format *0xAARRGGBB*, where *AA* is the alpha value, *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="38bf6-125">Los valores alfa van de 0x00 (transparente) a 0xFF (opaco).</span><span class="sxs-lookup"><span data-stu-id="38bf6-125">Alpha values range from 0x00 (transparent) to 0xFF (opaque).</span></span> <span data-ttu-id="38bf6-126">La propiedad es estática y debe aplicarse en el tiempo cero.</span><span class="sxs-lookup"><span data-stu-id="38bf6-126">The property is static and must be applied at time zero.</span></span>

<span data-ttu-id="38bf6-127">Si no especifica el valor alfa, el valor predeterminado es cero (transparente).</span><span class="sxs-lookup"><span data-stu-id="38bf6-127">If you do not specify the alpha value, it defaults to zero (transparent).</span></span> <span data-ttu-id="38bf6-128">En un proyecto de vídeo de color de 32 bits, esto hará que las transiciones o los efectos que usan alfa representen el origen de color de vídeo como completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="38bf6-128">In a 32-bit-color video project, this will cause transitions or effects that use alpha to render the Video Color Source as completely transparent.</span></span> <span data-ttu-id="38bf6-129">Para que sea segura, especifique siempre el alfa.</span><span class="sxs-lookup"><span data-stu-id="38bf6-129">To be safe, always specify the alpha.</span></span> <span data-ttu-id="38bf6-130">Por ejemplo, el negro opaco es **0xFF000000**.</span><span class="sxs-lookup"><span data-stu-id="38bf6-130">For example, opaque black is **0xFF000000**.</span></span>

<span data-ttu-id="38bf6-131">En el ejemplo de código siguiente se muestra cómo utilizar este objeto.</span><span class="sxs-lookup"><span data-stu-id="38bf6-131">The following code example shows how to use this object.</span></span> <span data-ttu-id="38bf6-132">Para obtener más información sobre el uso de [**IPropertySetter**](ipropertysetter.md), vea [establecer propiedades en efectos y transiciones](setting-properties-on-effects-and-transitions.md):</span><span class="sxs-lookup"><span data-stu-id="38bf6-132">For more information about using [**IPropertySetter**](ipropertysetter.md), see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md):</span></span>


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



<span data-ttu-id="38bf6-133">En el ejemplo siguiente se muestra la representación XML del objeto creado en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="38bf6-133">The following example shows the XML representation of the object created in the previous example.</span></span> <span data-ttu-id="38bf6-134">En este caso, el elemento [**param**](param-element.md) no admite elementos [**en**](at-element.md) o [**lineales**](linear-element.md) , porque el objeto no admite propiedades dinámicas:</span><span class="sxs-lookup"><span data-stu-id="38bf6-134">In this case the [**param**](param-element.md) element does not support [**at**](at-element.md) or [**linear**](linear-element.md) elements, because the object does not support dynamic properties:</span></span>


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



