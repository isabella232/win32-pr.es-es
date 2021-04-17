---
description: Describe la instalación local de WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: __CIMOMIdentification (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706605"
---
# <a name="__cimomidentification-class"></a><span data-ttu-id="4cd35-103">\_\_Clase CIMOMIdentification</span><span class="sxs-lookup"><span data-stu-id="4cd35-103">\_\_CIMOMIdentification class</span></span>

<span data-ttu-id="4cd35-104">La clase del sistema **\_ \_ CIMOMIdentification** describe la instalación local de WMI.</span><span class="sxs-lookup"><span data-stu-id="4cd35-104">The **\_\_CIMOMIdentification** system class describes the local installation of WMI.</span></span> <span data-ttu-id="4cd35-105">Se trata de una clase singleton; solo hay una instancia.</span><span class="sxs-lookup"><span data-stu-id="4cd35-105">This is a singleton class; there is only one instance.</span></span> <span data-ttu-id="4cd35-106">La clase **\_ \_ CIMOMIdentification** solo está disponible en los **espacios de nombres raíz y raíz** **\\ predeterminados** .</span><span class="sxs-lookup"><span data-stu-id="4cd35-106">The **\_\_CIMOMIdentification** class is available only in the **Root** and **Root\\Default** namespaces.</span></span> <span data-ttu-id="4cd35-107">Los usuarios consultan la instancia para obtener información sobre la instalación de WMI.</span><span class="sxs-lookup"><span data-stu-id="4cd35-107">Users query for the instance to obtain information about the WMI installation.</span></span>

<span data-ttu-id="4cd35-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4cd35-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4cd35-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4cd35-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd35-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cd35-110">Syntax</span></span>

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a><span data-ttu-id="4cd35-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4cd35-111">Members</span></span>

<span data-ttu-id="4cd35-112">La clase **\_ \_ CIMOMIdentification** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4cd35-112">The **\_\_CIMOMIdentification** class has these types of members:</span></span>

-   [<span data-ttu-id="4cd35-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4cd35-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4cd35-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4cd35-114">Properties</span></span>

<span data-ttu-id="4cd35-115">La clase **\_ \_ CIMOMIdentification** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4cd35-115">The **\_\_CIMOMIdentification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4cd35-116">**SetupDateTime**</span><span class="sxs-lookup"><span data-stu-id="4cd35-116">**SetupDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cd35-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4cd35-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cd35-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4cd35-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cd35-119">Fecha y hora de instalación.</span><span class="sxs-lookup"><span data-stu-id="4cd35-119">Date and time of installation.</span></span> <span data-ttu-id="4cd35-120">Esta propiedad está vacía después de instalar el sistema operativo por primera vez.</span><span class="sxs-lookup"><span data-stu-id="4cd35-120">This property is empty after the operating system is installed for the first time.</span></span>

<span data-ttu-id="4cd35-121">Si se ha eliminado el repositorio WMI y, a continuación, se ha creado de nuevo, esta propiedad contiene la fecha y la hora de creación del repositorio de nuevo.</span><span class="sxs-lookup"><span data-stu-id="4cd35-121">If the WMI repository has been deleted and then created again, this property contains the date and time that the repository is created again.</span></span>

</dd> <dt>

<span data-ttu-id="4cd35-122">**VersionCurrentlyRunning**</span><span class="sxs-lookup"><span data-stu-id="4cd35-122">**VersionCurrentlyRunning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cd35-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4cd35-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cd35-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4cd35-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cd35-125">Indica la versión de la imagen real que contiene el servicio WMI que creó el repositorio Modelo de información común (CIM).</span><span class="sxs-lookup"><span data-stu-id="4cd35-125">Indicates the version of the actual image containing the WMI service that created the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="4cd35-126">Dado que el formato del repositorio puede cambiar entre las versiones de WMI, esta propiedad permite futuras actualizaciones de WMI para determinar si se debe actualizar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="4cd35-126">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="4cd35-127">El formato es:</span><span class="sxs-lookup"><span data-stu-id="4cd35-127">The format is:</span></span>

<span data-ttu-id="4cd35-128">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="4cd35-128">"1.00.183.0000"</span></span>

<span data-ttu-id="4cd35-129">donde el primer dígito es la versión principal, los dos dígitos siguientes son versiones secundarias y los tres dígitos siguientes son el número de compilación.</span><span class="sxs-lookup"><span data-stu-id="4cd35-129">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="4cd35-130">No se usan los dígitos restantes.</span><span class="sxs-lookup"><span data-stu-id="4cd35-130">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="4cd35-131">**VersionUsedToCreateDB**</span><span class="sxs-lookup"><span data-stu-id="4cd35-131">**VersionUsedToCreateDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cd35-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4cd35-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cd35-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4cd35-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cd35-134">Indica la versión de la imagen real que contiene el servicio WMI que creó el repositorio CIM.</span><span class="sxs-lookup"><span data-stu-id="4cd35-134">Indicates the version of the actual image containing the WMI service that created the CIM repository.</span></span> <span data-ttu-id="4cd35-135">Dado que el formato del repositorio puede cambiar entre las versiones de WMI, esta propiedad permite futuras actualizaciones de WMI para determinar si se debe actualizar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="4cd35-135">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="4cd35-136">El formato es:</span><span class="sxs-lookup"><span data-stu-id="4cd35-136">The format is:</span></span>

<span data-ttu-id="4cd35-137">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="4cd35-137">"1.00.183.0000"</span></span>

<span data-ttu-id="4cd35-138">donde el primer dígito es la versión principal, los dos dígitos siguientes son versiones secundarias y los tres dígitos siguientes son el número de compilación.</span><span class="sxs-lookup"><span data-stu-id="4cd35-138">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="4cd35-139">No se usan los dígitos restantes.</span><span class="sxs-lookup"><span data-stu-id="4cd35-139">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="4cd35-140">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="4cd35-140">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cd35-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4cd35-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cd35-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4cd35-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cd35-143">Directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="4cd35-143">Installation directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cd35-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cd35-144">Remarks</span></span>

<span data-ttu-id="4cd35-145">La clase **\_ \_ CIMOMIdentification** se deriva de [**\_ \_ SystemClass**](--systemclass.md), que no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="4cd35-145">The **\_\_CIMOMIdentification** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

## <a name="examples"></a><span data-ttu-id="4cd35-146">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4cd35-146">Examples</span></span>

<span data-ttu-id="4cd35-147">El siguiente ejemplo de código de VBScript describe cómo mostrar la información de identificación del modelo de objetos CIM y se tomó del directorio de ejemplo en \\ \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ sysmgmt \\ WMI \\ scripting.</span><span class="sxs-lookup"><span data-stu-id="4cd35-147">The following VBScript code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



<span data-ttu-id="4cd35-148">El siguiente ejemplo de código Perl describe cómo mostrar la información de identificación del modelo de objetos CIM y se tomó del directorio de ejemplo en \\ \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ sysmgmt \\ WMI \\ scripting.</span><span class="sxs-lookup"><span data-stu-id="4cd35-148">The following Perl code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="4cd35-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cd35-149">Requirements</span></span>



| <span data-ttu-id="4cd35-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cd35-150">Requirement</span></span> | <span data-ttu-id="4cd35-151">Value</span><span class="sxs-lookup"><span data-stu-id="4cd35-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4cd35-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cd35-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4cd35-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cd35-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4cd35-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cd35-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4cd35-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cd35-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4cd35-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4cd35-156">Namespace</span></span><br/>                | <span data-ttu-id="4cd35-157">Root</span><span class="sxs-lookup"><span data-stu-id="4cd35-157">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="4cd35-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cd35-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd35-159">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="4cd35-159">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="4cd35-160">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="4cd35-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

