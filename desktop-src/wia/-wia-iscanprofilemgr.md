---
description: La interfaz IScanProfileMgr proporciona métodos para crear, abrir, eliminar y administrar perfiles de digitalización.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Interfaz IScanProfileMgr (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666681"
---
# <a name="iscanprofilemgr-interface"></a><span data-ttu-id="eac43-103">Interfaz IScanProfileMgr</span><span class="sxs-lookup"><span data-stu-id="eac43-103">IScanProfileMgr interface</span></span>

<span data-ttu-id="eac43-104">La interfaz **IScanProfileMgr** proporciona métodos para crear, abrir, eliminar y administrar perfiles de digitalización.</span><span class="sxs-lookup"><span data-stu-id="eac43-104">The **IScanProfileMgr** interface provides methods for creating, opening, deleting, and managing scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="eac43-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="eac43-105">Members</span></span>

<span data-ttu-id="eac43-106">La interfaz **IScanProfileMgr** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="eac43-106">The **IScanProfileMgr** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="eac43-107">**IScanProfileMgr** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eac43-107">**IScanProfileMgr** also has these types of members:</span></span>

-   [<span data-ttu-id="eac43-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="eac43-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eac43-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="eac43-109">Methods</span></span>

<span data-ttu-id="eac43-110">La interfaz **IScanProfileMgr** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="eac43-110">The **IScanProfileMgr** interface has these methods.</span></span>



| <span data-ttu-id="eac43-111">Método</span><span class="sxs-lookup"><span data-stu-id="eac43-111">Method</span></span>                                                                              | <span data-ttu-id="eac43-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="eac43-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eac43-113">**CreateProfile**</span><span class="sxs-lookup"><span data-stu-id="eac43-113">**CreateProfile**</span></span>](-wia-iscanprofilemgr-createprofile.md)                         | <span data-ttu-id="eac43-114">Crea un perfil de digitalización vacío y lo asocia a un escáner u otro elemento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="eac43-114">Creates an empty scan profile and associates it with a scanner or other WIA 2.0 item.</span></span><br/>                       |
| [<span data-ttu-id="eac43-115">**DeleteAllProfiles**</span><span class="sxs-lookup"><span data-stu-id="eac43-115">**DeleteAllProfiles**</span></span>](-wia-iscanprofilemgr-deleteallprofiles.md)                 | <span data-ttu-id="eac43-116">Elimina todos los perfiles de análisis asociados con el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="eac43-116">Deletes all the scan profiles associated with the specified device.</span></span><br/>                                         |
| [<span data-ttu-id="eac43-117">**DeleteAllProfilesForUser**</span><span class="sxs-lookup"><span data-stu-id="eac43-117">**DeleteAllProfilesForUser**</span></span>](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | <span data-ttu-id="eac43-118">Elimina todos los perfiles de digitalización disponibles para el usuario en el sistema en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eac43-118">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span> <br/> |
| [<span data-ttu-id="eac43-119">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="eac43-119">**DeleteProfile**</span></span>](-wia-iscanprofilemgr-deleteprofile.md)                         | <span data-ttu-id="eac43-120">Elimina el perfil de digitalización especificado.</span><span class="sxs-lookup"><span data-stu-id="eac43-120">Deletes the specified scan profile.</span></span><br/>                                                                         |
| [<span data-ttu-id="eac43-121">**GetDefaultProfile**</span><span class="sxs-lookup"><span data-stu-id="eac43-121">**GetDefaultProfile**</span></span>](-wia-iscanprofilemgr-getdefaultprofile.md)                 | <span data-ttu-id="eac43-122">Obtiene el perfil de detección predeterminado.</span><span class="sxs-lookup"><span data-stu-id="eac43-122">Gets the default scan profile.</span></span><br/>                                                                              |
| [<span data-ttu-id="eac43-123">**GetNumProfiles**</span><span class="sxs-lookup"><span data-stu-id="eac43-123">**GetNumProfiles**</span></span>](-wia-iscanprofilemgr-getnumprofiles.md)                       | <span data-ttu-id="eac43-124">Obtiene el número de perfiles de examen creados para el usuario en el sistema en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eac43-124">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span><br/> |
| [<span data-ttu-id="eac43-125">**GetNumProfilesforDeviceID**</span><span class="sxs-lookup"><span data-stu-id="eac43-125">**GetNumProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | <span data-ttu-id="eac43-126">Obtiene el número de perfiles de examen para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eac43-126">Gets the number of scan profiles for the device.</span></span><br/>                                                            |
| [<span data-ttu-id="eac43-127">**GetProfiles**</span><span class="sxs-lookup"><span data-stu-id="eac43-127">**GetProfiles**</span></span>](-wia-iscanprofilemgr-getprofiles.md)                             | <span data-ttu-id="eac43-128">Obtiene todos los perfiles de digitalización disponibles para el usuario en el sistema en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eac43-128">Gets all the scan profiles available for the user in the system that your application is running under.</span></span><br/>     |
| [<span data-ttu-id="eac43-129">**GetProfilesforDeviceID**</span><span class="sxs-lookup"><span data-stu-id="eac43-129">**GetProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | <span data-ttu-id="eac43-130">Obtiene todos los perfiles de análisis asociados a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eac43-130">Gets all the scan profiles associated with a device.</span></span><br/>                                                        |
| [<span data-ttu-id="eac43-131">**OpenProfile**</span><span class="sxs-lookup"><span data-stu-id="eac43-131">**OpenProfile**</span></span>](-wia-iscanprofilemgr-openprofile.md)                             | <span data-ttu-id="eac43-132">Abre un perfil de digitalización que se ha guardado en el disco como archivo XML.</span><span class="sxs-lookup"><span data-stu-id="eac43-132">Opens a scan profile that has been saved to disk as an XML file.</span></span><br/>                                            |
| [<span data-ttu-id="eac43-133">**Actualizaciones**</span><span class="sxs-lookup"><span data-stu-id="eac43-133">**Refresh**</span></span>](-wia-iscanprofilemgr-refresh.md)                                     | <span data-ttu-id="eac43-134">Vuelve a enumerar todos los perfiles de digitalización en el sistema.</span><span class="sxs-lookup"><span data-stu-id="eac43-134">Re-enumerates all the scan profiles in the system.</span></span><br/>                                                          |
| [<span data-ttu-id="eac43-135">**SetDefault**</span><span class="sxs-lookup"><span data-stu-id="eac43-135">**SetDefault**</span></span>](-wia-iscanprofilemgr-setdefault.md)                               | <span data-ttu-id="eac43-136">Establece el perfil de digitalización especificado como perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="eac43-136">Sets the specified scan profile as the default profile.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="eac43-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eac43-137">Remarks</span></span>

<span data-ttu-id="eac43-138">Para crear un objeto **IScanProfileMgr** , use el método [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="eac43-138">To create an **IScanProfileMgr** object, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method with the following parameters:</span></span>

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

<span data-ttu-id="eac43-139">Si un perfil de digitalización se guarda con el método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) , se almacena como un archivo XML en% userprofile% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="eac43-139">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="eac43-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eac43-140">Requirements</span></span>



| <span data-ttu-id="eac43-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="eac43-141">Requirement</span></span> | <span data-ttu-id="eac43-142">Value</span><span class="sxs-lookup"><span data-stu-id="eac43-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eac43-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eac43-143">Minimum supported client</span></span><br/> | <span data-ttu-id="eac43-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eac43-144">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="eac43-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eac43-145">Minimum supported server</span></span><br/> | <span data-ttu-id="eac43-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="eac43-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eac43-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eac43-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="eac43-148"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="eac43-148"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="eac43-149">IDL</span><span class="sxs-lookup"><span data-stu-id="eac43-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eac43-150"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eac43-150"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac43-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="eac43-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac43-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="eac43-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="eac43-153">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="eac43-153">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
