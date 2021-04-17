---
description: La propiedad PatchProperty obtiene información acerca de una revisión específica que se aplica a una instancia específica del producto. Esta propiedad llama a MsiGetPatchInfoEx.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Patch. PatchProperty (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653750"
---
# <a name="patchpatchproperty-method"></a><span data-ttu-id="930cf-104">Patch. PatchProperty (método)</span><span class="sxs-lookup"><span data-stu-id="930cf-104">Patch.PatchProperty method</span></span>

<span data-ttu-id="930cf-105">La propiedad **PatchProperty** obtiene información acerca de una revisión específica que se aplica a una instancia específica del producto.</span><span class="sxs-lookup"><span data-stu-id="930cf-105">The **PatchProperty** property gets information about a specific patch applied to a specific instance of the product.</span></span> <span data-ttu-id="930cf-106">Esta propiedad llama a [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span><span class="sxs-lookup"><span data-stu-id="930cf-106">This property calls [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="930cf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="930cf-107">Syntax</span></span>


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a><span data-ttu-id="930cf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="930cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930cf-109">*szProperty*</span><span class="sxs-lookup"><span data-stu-id="930cf-109">*szProperty*</span></span> 
</dt> <dd>

<span data-ttu-id="930cf-110">El parámetro *szProperty* puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="930cf-110">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="930cf-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="930cf-111">Name</span></span>          | <span data-ttu-id="930cf-112">Significado</span><span class="sxs-lookup"><span data-stu-id="930cf-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="930cf-113">LocalPackage</span><span class="sxs-lookup"><span data-stu-id="930cf-113">LocalPackage</span></span>  | <span data-ttu-id="930cf-114">Obtiene el archivo de revisión almacenado en caché que usa el producto.</span><span class="sxs-lookup"><span data-stu-id="930cf-114">Get the cached patch file used by the product.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="930cf-115">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="930cf-115">Transforms</span></span>    | <span data-ttu-id="930cf-116">Obtiene el conjunto de transformaciones de revisión aplicadas al producto en la última instalación de la revisión.</span><span class="sxs-lookup"><span data-stu-id="930cf-116">Get the set of patch transforms applied to the product by the last patch installation.</span></span> <span data-ttu-id="930cf-117">Es posible que este valor no esté disponible para las aplicaciones por usuario no administradas si el usuario no ha iniciado sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="930cf-117">This value may not be available for per-user-unmanaged applications if the user is not logged in to the computer.</span></span>                                                                                                                     |
| <span data-ttu-id="930cf-118">InstallDate</span><span class="sxs-lookup"><span data-stu-id="930cf-118">InstallDate</span></span>   | <span data-ttu-id="930cf-119">Obtiene la fecha en la que se aplicó la revisión al producto.</span><span class="sxs-lookup"><span data-stu-id="930cf-119">Get the date when the patch was applied to the product.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="930cf-120">No instalables</span><span class="sxs-lookup"><span data-stu-id="930cf-120">Uninstallable</span></span> | <span data-ttu-id="930cf-121">Devuelve "1" si la revisión está marcada como posible para la desinstalación del producto.</span><span class="sxs-lookup"><span data-stu-id="930cf-121">Returns "1" if the patch is marked as possible to uninstall from the product.</span></span> <span data-ttu-id="930cf-122">En este caso, el instalador puede seguir bloqueando la desinstalación si esta revisión es necesaria para otra revisión que no se puede desinstalar.</span><span class="sxs-lookup"><span data-stu-id="930cf-122">In this case, the installer can still block the uninstallation if this patch is required by another patch that cannot be uninstalled.</span></span>                                                                                                          |
| <span data-ttu-id="930cf-123">Estado</span><span class="sxs-lookup"><span data-stu-id="930cf-123">State</span></span>         | <span data-ttu-id="930cf-124">Devuelve "1" si esta revisión se aplica actualmente al producto.</span><span class="sxs-lookup"><span data-stu-id="930cf-124">Returns "1" if this patch is currently applied to the product.</span></span> <span data-ttu-id="930cf-125">Devuelve "2" si esta revisión se ha sustituido por otra revisión.</span><span class="sxs-lookup"><span data-stu-id="930cf-125">Returns "2" if this patch has been superseded by another patch.</span></span> <span data-ttu-id="930cf-126">Devuelve "4" si otra revisión ha hecho que esta revisión esté obsoleta.</span><span class="sxs-lookup"><span data-stu-id="930cf-126">Returns "4" if this patch has been made obsolete by another patch.</span></span> <span data-ttu-id="930cf-127">Estos valores corresponden a las constantes utilizadas por el parámetro *dwFilter* de [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span><span class="sxs-lookup"><span data-stu-id="930cf-127">These values correspond to the constants used by the *dwFilter* parameter of [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span> |
| <span data-ttu-id="930cf-128">DisplayName</span><span class="sxs-lookup"><span data-stu-id="930cf-128">DisplayName</span></span>   | <span data-ttu-id="930cf-129">Obtiene el nombre para mostrar registrado de la revisión.</span><span class="sxs-lookup"><span data-stu-id="930cf-129">Get the registered display name for the patch.</span></span> <span data-ttu-id="930cf-130">En el caso de las revisiones que no incluyen la propiedad DisplayName en la tabla [MsiPatchMetadata](msipatchmetadata-table.md) , el nombre para mostrar devuelto es una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="930cf-130">For patches that do not include the DisplayName property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned display name is an empty string ("").</span></span>                                                                                                      |
| <span data-ttu-id="930cf-131">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="930cf-131">MoreInfoURL</span></span>   | <span data-ttu-id="930cf-132">Obtener la dirección URL de la información de soporte registrada para la revisión.</span><span class="sxs-lookup"><span data-stu-id="930cf-132">Get the registered support information URL for the patch.</span></span> <span data-ttu-id="930cf-133">En el caso de las revisiones que no incluyen la propiedad MoreInfoURL en la tabla [MsiPatchMetadata](msipatchmetadata-table.md) , la dirección URL de información de soporte devuelta es una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="930cf-133">For patches that do not include the MoreInfoURL property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned support information URL is an empty string ("").</span></span>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930cf-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="930cf-134">Return value</span></span>

<span data-ttu-id="930cf-135">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="930cf-135">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="930cf-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="930cf-136">Remarks</span></span>

<span data-ttu-id="930cf-137">Este método puede devolver ERROR \_ Unknown \_ patch si el objeto [**patch**](patch-object.md) se inicializa con una cadena vacía para *ProductCode*.</span><span class="sxs-lookup"><span data-stu-id="930cf-137">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="930cf-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="930cf-138">Requirements</span></span>



| <span data-ttu-id="930cf-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="930cf-139">Requirement</span></span> | <span data-ttu-id="930cf-140">Value</span><span class="sxs-lookup"><span data-stu-id="930cf-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="930cf-141">Versión</span><span class="sxs-lookup"><span data-stu-id="930cf-141">Version</span></span><br/> | <span data-ttu-id="930cf-142">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="930cf-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="930cf-143">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="930cf-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="930cf-144">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="930cf-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="930cf-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="930cf-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="930cf-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="930cf-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="930cf-147">IID</span><span class="sxs-lookup"><span data-stu-id="930cf-147">IID</span></span><br/>     | <span data-ttu-id="930cf-148">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="930cf-148">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="930cf-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="930cf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930cf-150">**Distribución**</span><span class="sxs-lookup"><span data-stu-id="930cf-150">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="930cf-151">**MsiEnumPatchesEx**</span><span class="sxs-lookup"><span data-stu-id="930cf-151">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="930cf-152">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="930cf-152">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="930cf-153">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="930cf-153">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




