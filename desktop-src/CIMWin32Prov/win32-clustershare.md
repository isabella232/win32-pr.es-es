---
description: La \_ clase ClusterShare de Win32 representa un recurso compartido en un clúster.
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Win32_ClusterShare (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccff6ad8d99692d066728c99dd74ab07640af4fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153364"
---
# <a name="win32_clustershare-class"></a><span data-ttu-id="7c83d-103">\_Clase Win32 ClusterShare</span><span class="sxs-lookup"><span data-stu-id="7c83d-103">Win32\_ClusterShare class</span></span>

<span data-ttu-id="7c83d-104">\[La **clase \_ ClusterShare de Win32** está en desuso.</span><span class="sxs-lookup"><span data-stu-id="7c83d-104">\[The **Win32\_ClusterShare** class is deprecated.</span></span> <span data-ttu-id="7c83d-105">En su lugar, use las clases del [**\_ recurso compartido de msft**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) y [**msft \_ SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) .\]</span><span class="sxs-lookup"><span data-stu-id="7c83d-105">Please use the [**MSFT\_FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) and [**MSFT\_SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) classes instead.\]</span></span>

<span data-ttu-id="7c83d-106">La \_ clase ClusterShare de Win32 representa un recurso compartido en un clúster.</span><span class="sxs-lookup"><span data-stu-id="7c83d-106">The Win32\_ClusterShare class represents a shared resource on a cluster.</span></span>

<span data-ttu-id="7c83d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7c83d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c83d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c83d-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
  string   ServerName;
};
```

## <a name="members"></a><span data-ttu-id="7c83d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7c83d-109">Members</span></span>

<span data-ttu-id="7c83d-110">La **clase \_ ClusterShare de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7c83d-110">The **Win32\_ClusterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="7c83d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7c83d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7c83d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c83d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7c83d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="7c83d-113">Methods</span></span>

<span data-ttu-id="7c83d-114">La clase **Win32 \_ ClusterShare** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7c83d-114">The **Win32\_ClusterShare** class has these methods.</span></span>



| <span data-ttu-id="7c83d-115">Método</span><span class="sxs-lookup"><span data-stu-id="7c83d-115">Method</span></span>                                                    | <span data-ttu-id="7c83d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c83d-116">Description</span></span>                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="7c83d-117">**A**</span><span class="sxs-lookup"><span data-stu-id="7c83d-117">**Create**</span></span>](create-win32-clustershare.md)               | <span data-ttu-id="7c83d-118">Crea una nueva instancia de **\_ ClusterShare de Win32** .</span><span class="sxs-lookup"><span data-stu-id="7c83d-118">Creates a new **Win32\_ClusterShare** instance.</span></span><br/>       |
| [<span data-ttu-id="7c83d-119">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="7c83d-119">**Delete**</span></span>](delete-win32-clustershare.md)               | <span data-ttu-id="7c83d-120">Elimina una instancia de **Win32 \_ ClusterShare** .</span><span class="sxs-lookup"><span data-stu-id="7c83d-120">Deletes a **Win32\_ClusterShare** instance.</span></span><br/>           |
| [<span data-ttu-id="7c83d-121">**GetAccessMask**</span><span class="sxs-lookup"><span data-stu-id="7c83d-121">**GetAccessMask**</span></span>](getaccessmask-win32-clustershare.md) | <span data-ttu-id="7c83d-122">Devuelve un mapa de bits con los derechos de acceso al recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="7c83d-122">Returns a bitmap with the access rights to the share.</span></span><br/> |
| [<span data-ttu-id="7c83d-123">**SetShareInfo**</span><span class="sxs-lookup"><span data-stu-id="7c83d-123">**SetShareInfo**</span></span>](setshareinfo-win32-clustershare.md)   | <span data-ttu-id="7c83d-124">Establece los parámetros del recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="7c83d-124">Sets the parameters of the shared resource.</span></span><br/>           |



 

### <a name="properties"></a><span data-ttu-id="7c83d-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c83d-125">Properties</span></span>

<span data-ttu-id="7c83d-126">La **clase \_ ClusterShare de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7c83d-126">The **Win32\_ClusterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c83d-127">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="7c83d-127">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-128">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c83d-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-130">Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7c83d-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-131">Esta propiedad está obsoleta y ya no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7c83d-131">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="7c83d-132">En su lugar, use el método [**\_ share. GetAccessMask de Win32**](getaccessmask-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="7c83d-132">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="7c83d-133">WMI establece el valor de la propiedad **AccessMask** en **null** .</span><span class="sxs-lookup"><span data-stu-id="7c83d-133">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="7c83d-134">Para obtener más información sobre cómo configurar el acceso cuando se crea un recurso compartido, vea el método [**Create**](create-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="7c83d-134">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

<span data-ttu-id="7c83d-135">Esta propiedad se hereda del [**\_ recurso compartido de Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="7c83d-135">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c83d-136">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="7c83d-136">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-137">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7c83d-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")</span><span class="sxs-lookup"><span data-stu-id="7c83d-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-140">Se ha limitado el número de usuarios simultáneos para este recurso.</span><span class="sxs-lookup"><span data-stu-id="7c83d-140">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="7c83d-141">Si es **true**, se omite el valor de la propiedad **MaximumAllowed** .</span><span class="sxs-lookup"><span data-stu-id="7c83d-141">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

<span data-ttu-id="7c83d-142">Esta propiedad se hereda del [**\_ recurso compartido de Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="7c83d-142">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c83d-143">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7c83d-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c83d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-146">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7c83d-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-147">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7c83d-147">A short textual description of the object.</span></span>

<span data-ttu-id="7c83d-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7c83d-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c83d-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c83d-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c83d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-152">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7c83d-152">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-153">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7c83d-153">A textual description of the object.</span></span>

<span data-ttu-id="7c83d-154">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7c83d-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c83d-155">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7c83d-155">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-156">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7c83d-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-158">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7c83d-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-159">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7c83d-159">Indicates when the object was installed.</span></span> <span data-ttu-id="7c83d-160">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="7c83d-160">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7c83d-161">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7c83d-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c83d-162">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="7c83d-162">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-163">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c83d-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-165">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")</span><span class="sxs-lookup"><span data-stu-id="7c83d-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-166">Límite en el número máximo de usuarios a los que se les permite usar este recurso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="7c83d-166">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="7c83d-167">El valor solo es válido si la propiedad **AllowMaximum** está establecida en **false**.</span><span class="sxs-lookup"><span data-stu-id="7c83d-167">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

<span data-ttu-id="7c83d-168">Esta propiedad se hereda del [**\_ recurso compartido de Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="7c83d-168">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c83d-169">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7c83d-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c83d-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-172">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Network Management Structures \| [**share \_ info \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 red \_ ")</span><span class="sxs-lookup"><span data-stu-id="7c83d-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-173">Alias dado a una ruta de acceso configurada como un recurso compartido en un equipo con Windows.</span><span class="sxs-lookup"><span data-stu-id="7c83d-173">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="7c83d-174">Windows 2008 ejemplo: " \\ SERVER01 \\ Public": windows Server 2008 requiere que se coloque la UNC en el nombre.</span><span class="sxs-lookup"><span data-stu-id="7c83d-174">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

<span data-ttu-id="7c83d-175">Esta propiedad se hereda del [**\_ recurso compartido de Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="7c83d-175">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c83d-176">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="7c83d-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c83d-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-179">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")</span><span class="sxs-lookup"><span data-stu-id="7c83d-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-180">Ruta de acceso local del recurso compartido de Windows.</span><span class="sxs-lookup"><span data-stu-id="7c83d-180">Local path of the Windows share.</span></span>

<span data-ttu-id="7c83d-181">Ejemplo: "C: \\ archivos de programa"</span><span class="sxs-lookup"><span data-stu-id="7c83d-181">Example: "C:\\Program Files"</span></span>

<span data-ttu-id="7c83d-182">Esta propiedad se hereda del [**\_ recurso compartido de Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="7c83d-182">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c83d-183">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="7c83d-183">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c83d-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-186">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Network Management structures \| [**reshare \_ info \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ ServerName")</span><span class="sxs-lookup"><span data-stu-id="7c83d-186">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)\|shi503\_servername")</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-187">El servidor de clúster en el que se hospeda el recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="7c83d-187">The cluster server on which the share is hosted.</span></span>

</dd> <dt>

<span data-ttu-id="7c83d-188">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7c83d-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c83d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-191">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7c83d-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-192">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7c83d-192">String that indicates the current status of the object.</span></span> <span data-ttu-id="7c83d-193">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="7c83d-193">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7c83d-194">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="7c83d-194">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7c83d-195">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="7c83d-195">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7c83d-196">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="7c83d-196">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7c83d-197">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="7c83d-197">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7c83d-198">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="7c83d-198">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7c83d-199">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7c83d-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7c83d-200">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7c83d-200">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7c83d-201">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7c83d-201">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7c83d-202">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7c83d-202">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7c83d-203">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7c83d-203">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c83d-204">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7c83d-204">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7c83d-205">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7c83d-205">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7c83d-206">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7c83d-206">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7c83d-207">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7c83d-207">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7c83d-208">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7c83d-208">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7c83d-209">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7c83d-209">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7c83d-210">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7c83d-210">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7c83d-211">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7c83d-211">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7c83d-212">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7c83d-212">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7c83d-213">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7c83d-213">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83d-214">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c83d-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c83d-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c83d-216">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ type")</span><span class="sxs-lookup"><span data-stu-id="7c83d-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="7c83d-217">Tipo de recurso que se va a compartir.</span><span class="sxs-lookup"><span data-stu-id="7c83d-217">Type of resource being shared.</span></span> <span data-ttu-id="7c83d-218">Entre los tipos se incluyen las unidades de disco, las colas de impresión, las comunicaciones entre procesos (IPC) y los dispositivos generales.</span><span class="sxs-lookup"><span data-stu-id="7c83d-218">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<span data-ttu-id="7c83d-219">Esta propiedad se hereda del [**\_ recurso compartido de Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="7c83d-219">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="7c83d-220">**Unidad de disco** (0)</span><span class="sxs-lookup"><span data-stu-id="7c83d-220">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="7c83d-221">**Cola de impresión** (1)</span><span class="sxs-lookup"><span data-stu-id="7c83d-221">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="7c83d-222">**Dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="7c83d-222">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="7c83d-223">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="7c83d-223">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="7c83d-224">**Administrador de unidad de disco** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="7c83d-224">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="7c83d-225">**Administrador** de la cola de impresión (2147483649)</span><span class="sxs-lookup"><span data-stu-id="7c83d-225">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="7c83d-226">**Administrador de dispositivos** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="7c83d-226">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="7c83d-227">**Administración de IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="7c83d-227">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="7c83d-228"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7c83d-228"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7c83d-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c83d-229">Requirements</span></span>



| <span data-ttu-id="7c83d-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c83d-230">Requirement</span></span> | <span data-ttu-id="7c83d-231">Value</span><span class="sxs-lookup"><span data-stu-id="7c83d-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c83d-232">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c83d-232">Minimum supported client</span></span><br/> | <span data-ttu-id="7c83d-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c83d-233">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="7c83d-234">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c83d-234">Minimum supported server</span></span><br/> | <span data-ttu-id="7c83d-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c83d-235">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="7c83d-236">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7c83d-236">Namespace</span></span><br/>                | <span data-ttu-id="7c83d-237">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7c83d-237">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c83d-238">MOF</span><span class="sxs-lookup"><span data-stu-id="7c83d-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c83d-239"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c83d-239"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c83d-240">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c83d-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c83d-241"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c83d-241"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c83d-242">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c83d-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c83d-243">**\_Recurso compartido de Win32**</span><span class="sxs-lookup"><span data-stu-id="7c83d-243">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

