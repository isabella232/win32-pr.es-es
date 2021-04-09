---
description: La \_ clase de recurso compartido de Win32 representa un recurso compartido en un equipo que ejecuta Windows. Puede tratarse de una unidad de disco, impresora, comunicación entre procesos u otro dispositivo compartible. Para obtener más información sobre cómo recuperar clases WMI, vea recuperar una clase.
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Win32_Share (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153347"
---
# <a name="win32_share-class"></a><span data-ttu-id="7da57-105">\_Clase de recurso compartido Win32</span><span class="sxs-lookup"><span data-stu-id="7da57-105">Win32\_Share class</span></span>

<span data-ttu-id="7da57-106">La clase de **\_ recurso compartido de Win32** representa un recurso compartido en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="7da57-106">The **Win32\_Share** class represents a shared resource on a computer system running Windows.</span></span> <span data-ttu-id="7da57-107">Puede tratarse de una unidad de disco, impresora, comunicación entre procesos u otro dispositivo compartible.</span><span class="sxs-lookup"><span data-stu-id="7da57-107">This may be a disk drive, printer, interprocess communication, or other sharable device.</span></span> <span data-ttu-id="7da57-108">Para obtener más información sobre cómo recuperar clases WMI, vea [recuperar una clase](../wmisdk/retrieving-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="7da57-108">For more information about retrieving WMI classes, see [Retrieving a Class](../wmisdk/retrieving-a-class.md).</span></span>

<span data-ttu-id="7da57-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7da57-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7da57-110">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7da57-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da57-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7da57-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="7da57-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="7da57-112">Members</span></span>

<span data-ttu-id="7da57-113">La clase de **\_ recurso compartido de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7da57-113">The **Win32\_Share** class has these types of members:</span></span>

-   [<span data-ttu-id="7da57-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="7da57-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="7da57-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7da57-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7da57-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="7da57-116">Methods</span></span>

<span data-ttu-id="7da57-117">La clase de **\_ recurso compartido de Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7da57-117">The **Win32\_Share** class has these methods.</span></span>



| <span data-ttu-id="7da57-118">Método</span><span class="sxs-lookup"><span data-stu-id="7da57-118">Method</span></span>                                                             | <span data-ttu-id="7da57-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7da57-119">Description</span></span>                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7da57-120">**A**</span><span class="sxs-lookup"><span data-stu-id="7da57-120">**Create**</span></span>](create-method-in-class-win32-share.md)               | <span data-ttu-id="7da57-121">Método de clase que inicia el uso compartido para un recurso de servidor.</span><span class="sxs-lookup"><span data-stu-id="7da57-121">Class method that initiates sharing for a server resource.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="7da57-122">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="7da57-122">**Delete**</span></span>](delete-method-in-class-win32-share.md)               | <span data-ttu-id="7da57-123">Método de clase que elimina un nombre de recurso compartido de la lista de recursos compartidos de un servidor y desconecta las conexiones al recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="7da57-123">Class method that deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span><br/>                                                                       |
| [<span data-ttu-id="7da57-124">**GetAccessMask**</span><span class="sxs-lookup"><span data-stu-id="7da57-124">**GetAccessMask**</span></span>](getaccessmask-method-in-class-win32-share.md) | <span data-ttu-id="7da57-125">Devuelve los derechos de acceso al recurso compartido mantenido por el usuario o grupo en cuyo nombre se devuelve la instancia.</span><span class="sxs-lookup"><span data-stu-id="7da57-125">Returns the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="7da57-126">Debe utilizar este método en lugar de la propiedad **AccessMask** , que es siempre **null**.</span><span class="sxs-lookup"><span data-stu-id="7da57-126">You should use this method in place of the **AccessMask** property, which is always **NULL**.</span></span><br/> |
| [<span data-ttu-id="7da57-127">**SetShareInfo**</span><span class="sxs-lookup"><span data-stu-id="7da57-127">**SetShareInfo**</span></span>](setshareinfo-method-in-class-win32-share.md)   | <span data-ttu-id="7da57-128">Método de clase que establece los parámetros de un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="7da57-128">Class method that sets the parameters of a shared resource.</span></span><br/>                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="7da57-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7da57-129">Properties</span></span>

<span data-ttu-id="7da57-130">La clase de **\_ recurso compartido de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7da57-130">The **Win32\_Share** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7da57-131">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="7da57-131">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da57-132">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7da57-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7da57-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7da57-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da57-134">Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7da57-134">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7da57-135">Esta propiedad está obsoleta y ya no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7da57-135">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="7da57-136">En su lugar, use el método [**\_ share. GetAccessMask de Win32**](getaccessmask-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="7da57-136">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="7da57-137">WMI establece el valor de la propiedad **AccessMask** en **null** .</span><span class="sxs-lookup"><span data-stu-id="7da57-137">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="7da57-138">Para obtener más información sobre cómo configurar el acceso cuando se crea un recurso compartido, vea el método [**Create**](create-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="7da57-138">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="7da57-139">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="7da57-139">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da57-140">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7da57-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7da57-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7da57-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da57-142">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")</span><span class="sxs-lookup"><span data-stu-id="7da57-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="7da57-143">Se ha limitado el número de usuarios simultáneos para este recurso.</span><span class="sxs-lookup"><span data-stu-id="7da57-143">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="7da57-144">Si es **true**, se omite el valor de la propiedad **MaximumAllowed** .</span><span class="sxs-lookup"><span data-stu-id="7da57-144">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="7da57-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7da57-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da57-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7da57-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da57-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7da57-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da57-148">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7da57-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7da57-149">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7da57-149">A short textual description of the object.</span></span>

<span data-ttu-id="7da57-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7da57-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7da57-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7da57-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da57-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7da57-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da57-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7da57-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da57-154">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7da57-154">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7da57-155">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7da57-155">A textual description of the object.</span></span>

<span data-ttu-id="7da57-156">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7da57-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7da57-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7da57-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da57-158">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7da57-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7da57-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7da57-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da57-160">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7da57-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7da57-161">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7da57-161">Indicates when the object was installed.</span></span> <span data-ttu-id="7da57-162">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="7da57-162">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7da57-163">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7da57-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7da57-164">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="7da57-164">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da57-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7da57-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7da57-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7da57-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da57-167">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")</span><span class="sxs-lookup"><span data-stu-id="7da57-167">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="7da57-168">Límite en el número máximo de usuarios a los que se les permite usar este recurso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="7da57-168">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="7da57-169">El valor solo es válido si la propiedad **AllowMaximum** está establecida en **false**.</span><span class="sxs-lookup"><span data-stu-id="7da57-169">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7da57-170">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7da57-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da57-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7da57-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da57-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7da57-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da57-173">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**share \_ info \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)shi1 nombre de red \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="7da57-173">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="7da57-174">Alias dado a una ruta de acceso configurada como un recurso compartido en un equipo con Windows.</span><span class="sxs-lookup"><span data-stu-id="7da57-174">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="7da57-175">Windows 2008 ejemplo: " \\ SERVER01 \\ Public": windows Server 2008 requiere que se coloque la UNC en el nombre.</span><span class="sxs-lookup"><span data-stu-id="7da57-175">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

</dd> <dt>

<span data-ttu-id="7da57-176">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="7da57-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da57-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7da57-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da57-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7da57-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da57-179">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")</span><span class="sxs-lookup"><span data-stu-id="7da57-179">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="7da57-180">Ruta de acceso local del recurso compartido de Windows.</span><span class="sxs-lookup"><span data-stu-id="7da57-180">Local path of the Windows share.</span></span>

<span data-ttu-id="7da57-181">Ejemplo: "C: \\ archivos de programa"</span><span class="sxs-lookup"><span data-stu-id="7da57-181">Example: "C:\\Program Files"</span></span>

</dd> <dt>

<span data-ttu-id="7da57-182">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7da57-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da57-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7da57-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da57-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7da57-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da57-185">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="7da57-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7da57-186">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7da57-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="7da57-187">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="7da57-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7da57-188">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="7da57-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7da57-189">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="7da57-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7da57-190">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="7da57-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7da57-191">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="7da57-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7da57-192">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="7da57-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7da57-193">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7da57-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7da57-194">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7da57-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7da57-195">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7da57-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7da57-196">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7da57-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7da57-197">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7da57-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7da57-198">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7da57-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7da57-199">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7da57-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7da57-200">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7da57-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7da57-201">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7da57-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7da57-202">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7da57-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7da57-203">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7da57-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7da57-204">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7da57-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7da57-205">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7da57-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7da57-206">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7da57-206">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7da57-207">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7da57-207">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da57-208">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7da57-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7da57-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7da57-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da57-210">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ type")</span><span class="sxs-lookup"><span data-stu-id="7da57-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="7da57-211">Tipo de recurso que se va a compartir.</span><span class="sxs-lookup"><span data-stu-id="7da57-211">Type of resource being shared.</span></span> <span data-ttu-id="7da57-212">Entre los tipos se incluyen las unidades de disco, las colas de impresión, las comunicaciones entre procesos (IPC) y los dispositivos generales.</span><span class="sxs-lookup"><span data-stu-id="7da57-212">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="7da57-213">**Unidad de disco** (0)</span><span class="sxs-lookup"><span data-stu-id="7da57-213">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="7da57-214">**Cola de impresión** (1)</span><span class="sxs-lookup"><span data-stu-id="7da57-214">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="7da57-215">**Dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="7da57-215">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="7da57-216">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="7da57-216">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="7da57-217">**Administrador de unidad de disco** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="7da57-217">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="7da57-218">**Administrador** de la cola de impresión (2147483649)</span><span class="sxs-lookup"><span data-stu-id="7da57-218">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="7da57-219">**Administrador de dispositivos** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="7da57-219">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="7da57-220">**Administración de IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="7da57-220">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="7da57-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7da57-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7da57-222">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7da57-222">Remarks</span></span>

<span data-ttu-id="7da57-223">La clase de **\_ recurso compartido de Win32** se deriva de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7da57-223">The **Win32\_Share** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="7da57-224">El método Create de esta clase es un método estático.</span><span class="sxs-lookup"><span data-stu-id="7da57-224">The Create method in this class is a static method.</span></span> <span data-ttu-id="7da57-225">Los métodos **Delete**, **GetAccessMask** y **SetShareInfo** son métodos de instancia.</span><span class="sxs-lookup"><span data-stu-id="7da57-225">The **Delete**, **GetAccessMask** and **SetShareInfo** methods are all instance methods.</span></span>

<span data-ttu-id="7da57-226">En función de los permisos de seguridad, es posible que no pueda recuperar todas las propiedades de esta clase.</span><span class="sxs-lookup"><span data-stu-id="7da57-226">Depending on your security permissions, you may not be able to retrieve all of the properties of this class.</span></span> <span data-ttu-id="7da57-227">Por ejemplo, las propiedades **AllowMaximum**, **MaximumAllowed**, **path** y **Type** pueden devolver null.</span><span class="sxs-lookup"><span data-stu-id="7da57-227">For example, **AllowMaximum**, **MaximumAllowed**, **Path**, and **Type** properties may return null.</span></span> <span data-ttu-id="7da57-228">En general, los usuarios avanzados y los administradores podrán recuperar todos los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7da57-228">Generally speaking, Power Users and Administrators will be able to retrieve all property values.</span></span>

## <a name="examples"></a><span data-ttu-id="7da57-229">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7da57-229">Examples</span></span>

<span data-ttu-id="7da57-230">En el siguiente[ejemplo de código](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) del centro de script se enumeran todos los recursos compartidos de un equipo y se enumeran todos los permisos de recurso compartido para cada recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="7da57-230">The following Script Center[code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) lists all shares on a computer, and list all the share permissions for each share.</span></span>

<span data-ttu-id="7da57-231">La [información del recurso compartido Get similar a Win32 \_ share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell Sample queries Win32 \_ share y proporciona los resultados.</span><span class="sxs-lookup"><span data-stu-id="7da57-231">The [Get Share Information similar to Win32\_Share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell sample queries Win32\_Share and provides the results.</span></span>

<span data-ttu-id="7da57-232">En el siguiente ejemplo de PowerShell se muestran los recursos compartidos en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="7da57-232">The following PowerShell sample displays the shares on the local system.</span></span>


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



<span data-ttu-id="7da57-233">Como alternativa, si desea filtrar más de manera precisa, puede usar el siguiente fragmento de código de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="7da57-233">Alternately, if you wish to filter more precisely, you can use the following PowerShell snippet:</span></span>


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



<span data-ttu-id="7da57-234">En el siguiente ejemplo de VBScript se muestran los recursos compartidos del sistema local.</span><span class="sxs-lookup"><span data-stu-id="7da57-234">The Following VBScript sample displays the shares on the local system.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
Next
```



## <a name="requirements"></a><span data-ttu-id="7da57-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7da57-235">Requirements</span></span>



| <span data-ttu-id="7da57-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="7da57-236">Requirement</span></span> | <span data-ttu-id="7da57-237">Value</span><span class="sxs-lookup"><span data-stu-id="7da57-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7da57-238">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7da57-238">Minimum supported client</span></span><br/> | <span data-ttu-id="7da57-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7da57-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7da57-240">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7da57-240">Minimum supported server</span></span><br/> | <span data-ttu-id="7da57-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7da57-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7da57-242">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7da57-242">Namespace</span></span><br/>                | <span data-ttu-id="7da57-243">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7da57-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7da57-244">MOF</span><span class="sxs-lookup"><span data-stu-id="7da57-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7da57-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7da57-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7da57-246">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7da57-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7da57-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7da57-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7da57-248">Vea también</span><span class="sxs-lookup"><span data-stu-id="7da57-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da57-249">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="7da57-249">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="7da57-250">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="7da57-250">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="7da57-251">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="7da57-251">WMI Tasks: Files and Folders</span></span>](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
