---
description: La interfaz IScanProfile representa un único Perfil de examen y permite a las aplicaciones establecer y obtener las propiedades del perfil.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Interfaz IScanProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706320"
---
# <a name="iscanprofile-interface"></a><span data-ttu-id="c5e4b-103">Interfaz IScanProfile</span><span class="sxs-lookup"><span data-stu-id="c5e4b-103">IScanProfile interface</span></span>

<span data-ttu-id="c5e4b-104">La interfaz **IScanProfile** representa un único Perfil de examen y permite a las aplicaciones establecer y obtener las propiedades del perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-104">The **IScanProfile** interface represents a single scan profile and enables applications to set and get the properties of the profile.</span></span>

## <a name="members"></a><span data-ttu-id="c5e4b-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="c5e4b-105">Members</span></span>

<span data-ttu-id="c5e4b-106">La interfaz **IScanProfile** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c5e4b-106">The **IScanProfile** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c5e4b-107">**IScanProfile** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c5e4b-107">**IScanProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="c5e4b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5e4b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c5e4b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5e4b-109">Methods</span></span>

<span data-ttu-id="c5e4b-110">La interfaz **IScanProfile** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-110">The **IScanProfile** interface has these methods.</span></span>



| <span data-ttu-id="c5e4b-111">Método</span><span class="sxs-lookup"><span data-stu-id="c5e4b-111">Method</span></span>                                                     | <span data-ttu-id="c5e4b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5e4b-112">Description</span></span>                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5e4b-113">**GetAllPropIDs**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-113">**GetAllPropIDs**</span></span>](-wia-iscanprofile-getallpropids.md)   | <span data-ttu-id="c5e4b-114">Obtiene todos los identificadores de propiedad disponibles en un perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-114">Gets all available property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="c5e4b-115">**GetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-115">**GetDeviceID**</span></span>](-wia-iscanprofile-getdeviceid.md)       | <span data-ttu-id="c5e4b-116">Devuelve el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-116">Returns the ID of the device.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="c5e4b-117">**GetGUID**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-117">**GetGUID**</span></span>](-wia-iscanprofile-getguid.md)               | <span data-ttu-id="c5e4b-118">Devuelve el GUID del perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-118">Returns the GUID of the profile.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="c5e4b-119">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-119">**GetItem**</span></span>](-wia-iscanprofile-getitem.md)               | <span data-ttu-id="c5e4b-120">Obtiene el GUID de la categoría del elemento de WIA 2,0 con el que está asociado el perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-120">Gets the GUID of the category of the WIA 2.0 item that the profile is associated with.</span></span><br/>                                                   |
| [<span data-ttu-id="c5e4b-121">**GetName**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-121">**GetName**</span></span>](-wia-iscanprofile-getname.md)               | <span data-ttu-id="c5e4b-122">Obtiene el nombre descriptivo del perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-122">Gets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="c5e4b-123">**GetNumPropIDS**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-123">**GetNumPropIDS**</span></span>](-wia-iscanprofile-getnumpropids.md)   | <span data-ttu-id="c5e4b-124">Obtiene el número de identificadores de propiedad de un perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-124">Gets the number of property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="c5e4b-125">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-125">**GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)       | <span data-ttu-id="c5e4b-126">Obtiene el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de digitalización.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-126">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="c5e4b-127">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-127">**IsDefault**</span></span>](-wia-iscanprofile-isdefault.md)           | <span data-ttu-id="c5e4b-128">Obtiene un valor que indica si el perfil es el perfil de detección predeterminado de un dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) asociado.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-128">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span><br/> |
| [<span data-ttu-id="c5e4b-129">**RemoveProperty**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-129">**RemoveProperty**</span></span>](-wia-iscanprofile-removeproperty.md) | <span data-ttu-id="c5e4b-130">Quita una lista especificada de propiedades secundarias en el `<Properties>` elemento de un perfil de digitalización.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-130">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="c5e4b-131">**Guardar**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-131">**Save**</span></span>](-wia-iscanprofile-save.md)                     | <span data-ttu-id="c5e4b-132">Guarda los cambios en un perfil en el disco.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-132">Saves changes to a profile to disk.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="c5e4b-133">**SetItem**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-133">**SetItem**</span></span>](-wia-iscanprofile-setitem.md)               | <span data-ttu-id="c5e4b-134">Establece el GUID de la categoría del elemento de WIA 2,0 al que está asociado el perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-134">Sets the GUID of the category of WIA 2.0 item that the profile is associated with.</span></span><br/>                                                       |
| [<span data-ttu-id="c5e4b-135">**SetName**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-135">**SetName**</span></span>](-wia-iscanprofile-setname.md)               | <span data-ttu-id="c5e4b-136">Establece el nombre descriptivo del perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-136">Sets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="c5e4b-137">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-137">**SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)       | <span data-ttu-id="c5e4b-138">Establece el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de digitalización.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-138">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="c5e4b-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5e4b-139">Remarks</span></span>

<span data-ttu-id="c5e4b-140">Cualquier dispositivo de [**IWiaItem2**](-wia-iwiaitem2.md) puede tener un perfil de digitalización.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-140">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="c5e4b-141">Sin embargo, los elementos de **IWiaItem2** de tipos de la \_ categoría WIA \_ Finished \_ File y WIA \_ Category \_ root no pueden tener perfiles.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-141">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="c5e4b-142">Si un perfil de digitalización se guarda con el método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) , se almacena como un archivo XML en% userprofile% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-142">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="c5e4b-143">Para crear una instancia de un objeto **IScanProfile** , use el método [**IScanProfileMgr:: CreateProfile**](-wia-iscanprofilemgr-createprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e4b-143">To create an instance of an **IScanProfile** object, use the [**IScanProfileMgr::CreateProfile**](-wia-iscanprofilemgr-createprofile.md) method.</span></span> <span data-ttu-id="c5e4b-144">Para obtener una referencia a un perfil de digitalización que ya se ha guardado en el disco, use el método [**IScanProfileMgr:: OpenProfile**](-wia-iscanprofilemgr-openprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e4b-144">To get a reference to a scan profile that has already been saved to disk, use the [**IScanProfileMgr::OpenProfile**](-wia-iscanprofilemgr-openprofile.md) method.</span></span>

<span data-ttu-id="c5e4b-145">Todos los perfiles de examen tienen los siguientes elementos: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , y `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="c5e4b-145">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="c5e4b-146">El perfil predeterminado de un dispositivo también tiene un `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-146">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="c5e4b-147">Los `<ProfileGUID>` `<DeviceID>` elementos y no se pueden cambiar una vez creado el perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-147">The `<ProfileGUID>` and `<DeviceID>` elements cannot be changed after the profile is created.</span></span> <span data-ttu-id="c5e4b-148">Los valores del `<ProfileName>` elemento y el `<WiaItem>` elemento se pueden cambiar una vez creado el perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-148">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed after the profile is created.</span></span> <span data-ttu-id="c5e4b-149">`<Default>`Se puede Agregar o eliminar el elemento.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-149">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="c5e4b-150">Esto se puede hacer mediante programación con los métodos [**IScanProfile:: setName**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)y [**IScanProfileMgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e4b-150">This can be done programatically with the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="c5e4b-151">Los usuarios también pueden cambiar estas propiedades a través del método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e4b-151">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="c5e4b-152">El `<Properties>` elemento contiene `<Property>` elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-152">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="c5e4b-153">Úselos para agregar cualquier propiedad de dispositivo o elemento de WIA 2,0 al perfil.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-153">Use these to add any WIA 2.0 item or device property to the profile.</span></span> <span data-ttu-id="c5e4b-154">También puede desarrollar su propia imagen adquisiciones `<Property>` elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-154">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="c5e4b-155">Esto hace que el esquema de Perfil de análisis sea extensible.</span><span class="sxs-lookup"><span data-stu-id="c5e4b-155">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="c5e4b-156">(Para obtener más información sobre cómo extender el esquema, vea [definir propiedades personalizadas](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)y [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="c5e4b-156">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e4b-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5e4b-157">Requirements</span></span>



| <span data-ttu-id="c5e4b-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e4b-158">Requirement</span></span> | <span data-ttu-id="c5e4b-159">Value</span><span class="sxs-lookup"><span data-stu-id="c5e4b-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e4b-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5e4b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e4b-161">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c5e4b-161">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c5e4b-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5e4b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e4b-163">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5e4b-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5e4b-164">IDL</span><span class="sxs-lookup"><span data-stu-id="c5e4b-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5e4b-165"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5e4b-165"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5e4b-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5e4b-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e4b-167">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c5e4b-167">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="c5e4b-168">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="c5e4b-168">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
