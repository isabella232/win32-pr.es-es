---
description: 'La interfaz IPropertySetter establece propiedades en un efecto o transición en los servicios de edición de DirectShow (DES). Para usar esta interfaz, cree una instancia de un objeto setter de propiedad (CLSID \_ PropertySetter) y asóciela con un efecto o transición llamando al método IAMTimelineObj:: SetPropertySetter. Para obtener más información, vea trabajar con efectos y transiciones. normalmente, una aplicación solo necesita llamar al método IPropertySetter:: ClearProps para borrar las propiedades existentes y el método IPropertySetter:: AddProp para agregar nuevas propiedades. Otros componentes DES llaman a los otros métodos de esta interfaz.'
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interfaz IPropertySetter (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680508"
---
# <a name="ipropertysetter-interface"></a><span data-ttu-id="fb870-105">Interfaz IPropertySetter</span><span class="sxs-lookup"><span data-stu-id="fb870-105">IPropertySetter interface</span></span>

> [!Note]  
> <span data-ttu-id="fb870-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="fb870-106">\[Deprecated.</span></span> <span data-ttu-id="fb870-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fb870-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fb870-108">La `IPropertySetter` interfaz establece las propiedades de un efecto o una transición en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="fb870-108">The `IPropertySetter` interface sets properties on an effect or transition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="fb870-109">Para usar esta interfaz, cree una instancia de un objeto setter de propiedad (CLSID \_ PropertySetter) y asóciela con un efecto o transición llamando al método [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="fb870-109">To use this interface, create an instance of a property setter object (CLSID\_PropertySetter), and associate it with an effect or transition by calling the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span> <span data-ttu-id="fb870-110">Para obtener más información, vea [trabajar con efectos y transiciones](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="fb870-110">For more information, see [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

<span data-ttu-id="fb870-111">Normalmente, una aplicación solo necesita llamar al método [**IPropertySetter:: ClearProps**](ipropertysetter-clearprops.md) para borrar las propiedades existentes y el método [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) para agregar nuevas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fb870-111">Usually an application needs to call only the [**IPropertySetter::ClearProps**](ipropertysetter-clearprops.md) method to clear existing properties, and the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method to add new properties.</span></span> <span data-ttu-id="fb870-112">Otros componentes DES llaman a los otros métodos de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="fb870-112">The other methods on this interface are called by other DES components.</span></span>

## <a name="members"></a><span data-ttu-id="fb870-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb870-113">Members</span></span>

<span data-ttu-id="fb870-114">La interfaz **IPropertySetter** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fb870-114">The **IPropertySetter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fb870-115">**IPropertySetter** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fb870-115">**IPropertySetter** also has these types of members:</span></span>

-   [<span data-ttu-id="fb870-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb870-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fb870-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb870-117">Methods</span></span>

<span data-ttu-id="fb870-118">La interfaz **IPropertySetter** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fb870-118">The **IPropertySetter** interface has these methods.</span></span>



| <span data-ttu-id="fb870-119">Método</span><span class="sxs-lookup"><span data-stu-id="fb870-119">Method</span></span>                                               | <span data-ttu-id="fb870-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb870-120">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb870-121">**AddProp**</span><span class="sxs-lookup"><span data-stu-id="fb870-121">**AddProp**</span></span>](ipropertysetter-addprop.md)           | <span data-ttu-id="fb870-122">Agrega una propiedad al establecedor de propiedad, con una matriz de pares de valor de tiempo que definen el valor de la propiedad en un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fb870-122">Adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span><br/> |
| [<span data-ttu-id="fb870-123">**ClearProps**</span><span class="sxs-lookup"><span data-stu-id="fb870-123">**ClearProps**</span></span>](ipropertysetter-clearprops.md)     | <span data-ttu-id="fb870-124">Borra todos los datos de propiedad del establecedor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="fb870-124">Clears all property data from the property setter.</span></span><br/>                                                                                 |
| [<span data-ttu-id="fb870-125">**CloneProps**</span><span class="sxs-lookup"><span data-stu-id="fb870-125">**CloneProps**</span></span>](ipropertysetter-cloneprops.md)     | <span data-ttu-id="fb870-126">Clona un conjunto de propiedades de este establecedor de propiedad y los agrega a un nuevo establecedor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="fb870-126">Clones a set of properties from this property setter and adds them to a new property setter.</span></span><br/>                                       |
| [<span data-ttu-id="fb870-127">**FreeProps**</span><span class="sxs-lookup"><span data-stu-id="fb870-127">**FreeProps**</span></span>](ipropertysetter-freeprops.md)       | <span data-ttu-id="fb870-128">Libera los recursos asignados por el método [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="fb870-128">Frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span><br/>                             |
| [<span data-ttu-id="fb870-129">**GetProps**</span><span class="sxs-lookup"><span data-stu-id="fb870-129">**GetProps**</span></span>](ipropertysetter-getprops.md)         | <span data-ttu-id="fb870-130">Recupera las propiedades establecidas en este objeto, con sus valores correspondientes.</span><span class="sxs-lookup"><span data-stu-id="fb870-130">Retrieves the properties set on this object, with their corresponding values.</span></span><br/>                                                      |
| [<span data-ttu-id="fb870-131">**LoadFromBlob**</span><span class="sxs-lookup"><span data-stu-id="fb870-131">**LoadFromBlob**</span></span>](ipropertysetter-loadfromblob.md) | <span data-ttu-id="fb870-132">Carga los datos de propiedad desde un formato de persistencia.</span><span class="sxs-lookup"><span data-stu-id="fb870-132">Loads property data from a persistence format.</span></span><br/>                                                                                     |
| [<span data-ttu-id="fb870-133">**LoadXML**</span><span class="sxs-lookup"><span data-stu-id="fb870-133">**LoadXML**</span></span>](ipropertysetter-loadxml.md)           | <span data-ttu-id="fb870-134">Carga los datos de propiedad expresados en lenguaje de marcado extensible (XML).</span><span class="sxs-lookup"><span data-stu-id="fb870-134">Loads property data expressed in Extensible Markup Language (XML).</span></span><br/>                                                                 |
| [<span data-ttu-id="fb870-135">**PrintXML**</span><span class="sxs-lookup"><span data-stu-id="fb870-135">**PrintXML**</span></span>](ipropertysetter-printxml.md)         | <span data-ttu-id="fb870-136">Convierte los datos de propiedad en una cadena XML.</span><span class="sxs-lookup"><span data-stu-id="fb870-136">Converts property data into an XML string.</span></span><br/>                                                                                         |
| [<span data-ttu-id="fb870-137">**SaveToBlob**</span><span class="sxs-lookup"><span data-stu-id="fb870-137">**SaveToBlob**</span></span>](ipropertysetter-savetoblob.md)     | <span data-ttu-id="fb870-138">Guarda los datos de propiedad en un formato de persistencia.</span><span class="sxs-lookup"><span data-stu-id="fb870-138">Saves the property data to a persistence format.</span></span><br/>                                                                                   |
| [<span data-ttu-id="fb870-139">**SetProps**</span><span class="sxs-lookup"><span data-stu-id="fb870-139">**SetProps**</span></span>](ipropertysetter-setprops.md)         | <span data-ttu-id="fb870-140">Establece las propiedades del objeto de destino en el estado adecuado para el tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="fb870-140">Sets the properties of the target object to the appropriate state for the specified time.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="fb870-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb870-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fb870-142">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="fb870-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fb870-143">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fb870-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fb870-144">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fb870-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb870-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb870-145">Requirements</span></span>



| <span data-ttu-id="fb870-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb870-146">Requirement</span></span> | <span data-ttu-id="fb870-147">Value</span><span class="sxs-lookup"><span data-stu-id="fb870-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb870-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb870-148">Header</span></span><br/>  | <dl> <span data-ttu-id="fb870-149"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb870-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fb870-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb870-150">Library</span></span><br/> | <dl> <span data-ttu-id="fb870-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb870-151"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
