---
description: Establecer propiedades en efectos y transiciones
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Establecer propiedades en efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677029"
---
# <a name="setting-properties-on-effects-and-transitions"></a><span data-ttu-id="8b5fe-103">Establecer propiedades en efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="8b5fe-103">Setting Properties on Effects and Transitions</span></span>

<span data-ttu-id="8b5fe-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="8b5fe-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8b5fe-105">Muchos efectos y transiciones de los [servicios de edición de DirectShow](directshow-editing-services.md) admiten propiedades que controlan su comportamiento.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-105">Many [DirectShow Editing Services](directshow-editing-services.md) effects and transitions support properties that control their behavior.</span></span> <span data-ttu-id="8b5fe-106">Una aplicación puede establecer el valor de una propiedad mediante la interfaz [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5fe-106">An application can set the value of a property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="8b5fe-107">El objeto de efecto o transición subyacente debe admitir **IDispatch** para establecer las propiedades.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-107">The underlying effect or transition object must support **IDispatch** for setting the properties.</span></span> <span data-ttu-id="8b5fe-108">Con las transiciones y los efectos de vídeo, la aplicación puede establecer un intervalo de valores que cambian con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-108">With video effects and transitions, the application can set a range of values that change over time.</span></span> <span data-ttu-id="8b5fe-109">(Por ejemplo, puede establecer una transición de borrado para retroceder y avanzar por el marco). Con los efectos de audio, el valor de la propiedad es estático y no puede cambiar con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-109">(For example, you can set a wipe transition to move back and forth across the frame.) With audio effects, the value of the property is static and cannot change over time.</span></span> <span data-ttu-id="8b5fe-110">La única excepción es el efecto de [sobre de volumen](volume-envelope-effect.md) , que admite una propiedad dinámica para el nivel de volumen.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-110">The only exception is the [Volume Envelope](volume-envelope-effect.md) effect, which supports a dynamic property for the volume level.</span></span>

<span data-ttu-id="8b5fe-111">Para establecer una propiedad, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-111">To set a property, perform the following steps.</span></span>

1.  <span data-ttu-id="8b5fe-112">Cree una instancia del establecedor de propiedad (CLSID \_ PropertySetter).</span><span class="sxs-lookup"><span data-stu-id="8b5fe-112">Create an instance of the property setter (CLSID\_PropertySetter).</span></span>
2.  <span data-ttu-id="8b5fe-113">Rellene las estructuras [**de \_ valor**](dexter-value.md) de [**Dexterity \_**](dexter-param.md) y Dexterity con los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-113">Fill [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures with the property data.</span></span> <span data-ttu-id="8b5fe-114">Estas estructuras se describen a continuación.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-114">These structures are discussed below.</span></span>
3.  <span data-ttu-id="8b5fe-115">Pase las estructuras de valor [**Dexterity \_**](dexter-param.md) y [**Dexterity \_**](dexter-value.md) al método [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5fe-115">Pass the [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures to the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method.</span></span>
4.  <span data-ttu-id="8b5fe-116">Repita los pasos 2 y 3 para cada propiedad que desee establecer.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-116">Repeat steps 2 and 3 for each property you want to set.</span></span>
5.  <span data-ttu-id="8b5fe-117">Pase el puntero de la interfaz [**IPropertySetter**](ipropertysetter.md) al método [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5fe-117">Pass the [**IPropertySetter**](ipropertysetter.md) interface pointer to the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span>

<span data-ttu-id="8b5fe-118">La estructura del [**\_ parámetro dexterss**](dexter-param.md) especifica qué propiedad se establece.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-118">The [**DEXTER\_PARAM**](dexter-param.md) structure specifies which property is being set.</span></span> <span data-ttu-id="8b5fe-119">Contiene los miembros siguientes.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-119">It contains the following members.</span></span>

-   <span data-ttu-id="8b5fe-120">**Nombre**: nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="8b5fe-120">**Name**: Name of the property</span></span>
-   <span data-ttu-id="8b5fe-121">**DISPID**: Reserved, debe ser cero</span><span class="sxs-lookup"><span data-stu-id="8b5fe-121">**dispID**: Reserved, must be zero</span></span>
-   <span data-ttu-id="8b5fe-122">**nvalores**: número de valores</span><span class="sxs-lookup"><span data-stu-id="8b5fe-122">**nValues**: Number of values</span></span>

<span data-ttu-id="8b5fe-123">La \_ estructura de valores de Dexterity especifica el valor de una propiedad en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-123">The DEXTER\_VALUE structure specifies the value of a property at a given time.</span></span> <span data-ttu-id="8b5fe-124">Contiene los miembros siguientes.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-124">It contains the following members.</span></span>

-   <span data-ttu-id="8b5fe-125">**v**: tipo Variant que especifica un nuevo valor para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-125">**v**: VARIANT type that specifies a new value for the property.</span></span> <span data-ttu-id="8b5fe-126">El miembro **VT** de esta variante define el tipo de datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-126">The **vt** member of this VARIANT defines the data type of the property.</span></span> <span data-ttu-id="8b5fe-127">Para obtener más información sobre el tipo **Variant** , vea el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-127">For more information on the **VARIANT** type, see the Windows SDK.</span></span>
-   <span data-ttu-id="8b5fe-128">**RT**: tiempo de referencia cuando la propiedad asume este valor, en relación con la hora de inicio del efecto o la transición.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-128">**rt**: Reference time when the property assumes this value, relative to the starting time of the effect or transition.</span></span> <span data-ttu-id="8b5fe-129">La hora de inicio del efecto o la transición es relativa a la hora de inicio de su objeto primario.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-129">The start time of the effect or transition is relative to the start time of its parent object.</span></span>
-   <span data-ttu-id="8b5fe-130">**dwInterp**: marca que especifica cómo cambia la propiedad del valor anterior al nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-130">**dwInterp**: Flag that specifies how the property changes from the previous value to the new value.</span></span> <span data-ttu-id="8b5fe-131">Con la \_ marca de salto DEXTERF, la propiedad salta inmediatamente al nuevo valor en el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-131">With the DEXTERF\_JUMP flag, the property jumps instantly to the new value at the specified time.</span></span> <span data-ttu-id="8b5fe-132">Con la \_ marca DEXTERF Interpolate, la propiedad se interpola linealmente desde el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-132">With the DEXTERF\_INTERPOLATE flag, the property is interpolated linearly from the previous value.</span></span>

<span data-ttu-id="8b5fe-133">Si establece el miembro **VT** en VT \_ BSTR, el establecedor de propiedad realiza las conversiones necesarias.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-133">If you set the **vt** member to VT\_BSTR, the property setter makes any necessary conversions.</span></span> <span data-ttu-id="8b5fe-134">En el caso de valores de punto flotante, incluya el cero a la izquierda delante de la posición decimal.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-134">For floating-point values, include the leading zero before the decimal place.</span></span> <span data-ttu-id="8b5fe-135">Por ejemplo, 0,3, no. 3.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-135">For example, 0.3, not .3.</span></span>

> [!Note]  
> <span data-ttu-id="8b5fe-136">Las aplicaciones deben evitar depender de la conversión de **BSTR** s a valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-136">Applications should avoid relying on the conversion from **BSTR** s to numeric values.</span></span> <span data-ttu-id="8b5fe-137">Si la propiedad tiene un valor numérico, puede usar el tipo de **variante** numérica adecuado.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-137">If the property has a numeric value, use the appropriate numeric **VARIANT** type is possible.</span></span>

 

<span data-ttu-id="8b5fe-138">El valor de una propiedad puede cambiar con el tiempo, por lo que el método [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) toma una única estructura de [**\_ parámetros de Dexterity**](dexter-param.md) y un puntero a una matriz de estructuras de [**\_ valor de Dexterity**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5fe-138">The value of a property can change over time, so the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method takes a single [**DEXTER\_PARAM**](dexter-param.md) structure and a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span> <span data-ttu-id="8b5fe-139">La matriz define un conjunto de valores basados en el tiempo para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-139">The array defines a set of time-based values for the property.</span></span> <span data-ttu-id="8b5fe-140">Los miembros de la matriz deben estar en orden de tiempo ascendente y el miembro **nvalores** de la estructura del \_ parámetro Dexterity debe ser igual a la longitud de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-140">The members of the array must be in ascending time order, and the **nValues** member of the DEXTER\_PARAM structure must equal the length of the array.</span></span>

<span data-ttu-id="8b5fe-141">En el ejemplo de código siguiente se crean datos de propiedades para la transición de [borrado de SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5fe-141">The following code example creates property data for the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span> <span data-ttu-id="8b5fe-142">Establece el código de borrado en 120, que crea un barrido de óvalo.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-142">It sets the wipe code to 120, which creates an oval wipe.</span></span> <span data-ttu-id="8b5fe-143">Establece el tiempo de referencia en cero, lo que indica el inicio de la transición.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-143">It sets the reference time to zero, indicating the start of the transition.</span></span>


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



<span data-ttu-id="8b5fe-144">**Cambiar propiedades dinámicamente**</span><span class="sxs-lookup"><span data-stu-id="8b5fe-144">**Dynamically Changing Properties**</span></span>

<span data-ttu-id="8b5fe-145">Después de representar un proyecto de edición de vídeo, es posible modificar las propiedades de un objeto de efecto o transición mientras el gráfico se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-145">After you render a video editing project, it is possible to modify an effect or transition object's properties while the graph is running.</span></span> <span data-ttu-id="8b5fe-146">Sin embargo, esto solo es posible si establece propiedades en ese objeto antes de que la aplicación llame a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="8b5fe-146">However, this is possible only if you set properties on that object before the application called [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="8b5fe-147">Si es así, puede llamar a [**IAMTimelineObj:: GetPropertySetter**](iamtimelineobj-getpropertysetter.md) en el efecto o la transición, borrar o modificar las propiedades y los cambios se realizarán de forma dinámica a medida que el gráfico se esté ejecutando.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-147">If so, you can call [**IAMTimelineObj::GetPropertySetter**](iamtimelineobj-getpropertysetter.md) on the effect or transition, clear or modify the properties, and the changes will happen dynamically as the graph is running.</span></span> <span data-ttu-id="8b5fe-148">Puede haber anomalías visuales mientras se produce el cambio, por lo que solo se recomienda para la vista previa.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-148">There may be visual anomalies while the change occurs, so this is recommended only for preview.</span></span> <span data-ttu-id="8b5fe-149">No cambie las propiedades mientras escribe el proyecto en un archivo.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-149">Do not change the properties while you are writing the project to a file.</span></span>

<span data-ttu-id="8b5fe-150">Si no ha establecido ninguna propiedad en el objeto de efecto o transición antes de llamar a **ConnectFrontEnd**, no podrá agregarle propiedades mientras se esté ejecutando el gráfico.</span><span class="sxs-lookup"><span data-stu-id="8b5fe-150">If you did not set any properties on the effect or transition object before you called **ConnectFrontEnd**, you cannot add properties to it while the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b5fe-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b5fe-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b5fe-152">Trabajar con efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="8b5fe-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



