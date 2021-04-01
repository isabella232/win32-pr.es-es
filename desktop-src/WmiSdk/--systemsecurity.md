---
description: Contiene métodos que permiten obtener acceso y modificar la configuración de seguridad de un espacio de nombres.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: __SystemSecurity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156929"
---
# <a name="__systemsecurity-class"></a><span data-ttu-id="8ada4-103">\_\_Clase SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="8ada4-103">\_\_SystemSecurity class</span></span>

<span data-ttu-id="8ada4-104">La clase del sistema **\_ \_ SystemSecurity** contiene métodos que permiten obtener acceso a la configuración de seguridad de un espacio de nombres y modificarla.</span><span class="sxs-lookup"><span data-stu-id="8ada4-104">The **\_\_SystemSecurity** system class contains methods that let you access and modify the security settings for a namespace.</span></span> <span data-ttu-id="8ada4-105">La clase **\_ \_ SystemSecurity** es una clase singleton en cada espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8ada4-105">The **\_\_SystemSecurity** class is a singleton class in each namespace.</span></span>

> [!Note]  
> <span data-ttu-id="8ada4-106">Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="8ada4-106">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

 

<span data-ttu-id="8ada4-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8ada4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8ada4-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="8ada4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ada4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ada4-109">Syntax</span></span>

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a><span data-ttu-id="8ada4-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="8ada4-110">Members</span></span>

<span data-ttu-id="8ada4-111">La clase **\_ \_ SystemSecurity** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8ada4-111">The **\_\_SystemSecurity** class has these types of members:</span></span>

-   [<span data-ttu-id="8ada4-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8ada4-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8ada4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8ada4-113">Methods</span></span>

<span data-ttu-id="8ada4-114">La clase **\_ \_ SystemSecurity** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8ada4-114">The **\_\_SystemSecurity** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8ada4-115">Método</span><span class="sxs-lookup"><span data-stu-id="8ada4-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8ada4-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ada4-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8ada4-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ada4-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8ada4-118">Obtiene una lista de usuarios a los que se permite el acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="8ada4-118">Gets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ada4-119">Este método no funciona en las versiones compatibles de Windows.</span><span class="sxs-lookup"><span data-stu-id="8ada4-119">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="8ada4-120">En su lugar, <a href="--systemsecurity-getsd.md"><strong>se usa.</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ada4-120">Use <a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8ada4-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ada4-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8ada4-122">Devuelve una máscara con cada bit que corresponde a un derecho de acceso.</span><span class="sxs-lookup"><span data-stu-id="8ada4-122">Returns a mask with each bit that corresponds to an access right.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8ada4-123"><a href="--systemsecurity-getsd.md"><strong>Se obtiene</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ada4-123"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8ada4-124">Obtiene el <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> del espacio de nombres al que está conectado el usuario.</span><span class="sxs-lookup"><span data-stu-id="8ada4-124">Gets the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8ada4-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ada4-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8ada4-126">Obtiene el descriptor de seguridad que controla el acceso al espacio de nombres WMI asociado a la instancia de <strong>__SystemSecurity</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ada4-126">Gets the security descriptor that controls access to the WMI namespace associated with the instance of <strong>__SystemSecurity</strong>.</span></span> <span data-ttu-id="8ada4-127">El descriptor de seguridad se devuelve como una instancia de<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8ada4-127">The security descriptor is returned as an instance of<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8ada4-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ada4-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8ada4-129">Establece una lista de usuarios a los que se permite el acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="8ada4-129">Sets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ada4-130">Este método no funciona en las versiones compatibles de Windows.</span><span class="sxs-lookup"><span data-stu-id="8ada4-130">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="8ada4-131">En su lugar, use <a href="--systemsecurity-setsd.md"><strong>establecido</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8ada4-131">Use <a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8ada4-132"><a href="--systemsecurity-setsd.md"><strong>Establecido</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ada4-132"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8ada4-133">Establece el descriptor de seguridad para el espacio de nombres al que está conectado el usuario.</span><span class="sxs-lookup"><span data-stu-id="8ada4-133">Sets the security descriptor for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8ada4-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ada4-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8ada4-135">Escribe una versión actualizada del descriptor de seguridad que controla el acceso a la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ada4-135">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="8ada4-136">El descriptor de seguridad se representa mediante una instancia de <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8ada4-136">The security descriptor is represented by an instance of <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8ada4-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ada4-137">Remarks</span></span>

<span data-ttu-id="8ada4-138">Puede requerir que las aplicaciones y los scripts de cliente usen una conexión cifrada para la autenticación agregando el calificador **RequiresEncryption** al archivo. mof que crea el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8ada4-138">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="8ada4-139">También puede modificar un espacio de nombres existente agregando este atributo y compilando de nuevo el archivo. mof.</span><span class="sxs-lookup"><span data-stu-id="8ada4-139">You can also modify an existing namespace by adding this attribute and compile the .mof file again.</span></span> <span data-ttu-id="8ada4-140">Para obtener más información sobre cómo usar **RequiresEncryption**, vea [requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="8ada4-140">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ada4-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ada4-141">Requirements</span></span>



| <span data-ttu-id="8ada4-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ada4-142">Requirement</span></span> | <span data-ttu-id="8ada4-143">Value</span><span class="sxs-lookup"><span data-stu-id="8ada4-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8ada4-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ada4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="8ada4-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ada4-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8ada4-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ada4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="8ada4-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ada4-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8ada4-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8ada4-148">Namespace</span></span><br/>                | <span data-ttu-id="8ada4-149">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="8ada4-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8ada4-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ada4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ada4-151">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8ada4-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="8ada4-152">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="8ada4-152">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="8ada4-153">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="8ada4-153">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="8ada4-154">Proteger los espacios de nombres de WMI</span><span class="sxs-lookup"><span data-stu-id="8ada4-154">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="8ada4-155">Establecer la herencia de la seguridad del espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8ada4-155">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="8ada4-156">Listas de Access Control (ACL)</span><span class="sxs-lookup"><span data-stu-id="8ada4-156">Access Control Lists (ACLs)</span></span>](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[<span data-ttu-id="8ada4-157">**Descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="8ada4-157">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

