---
title: Win32_RDMSDeploymentSettings (clase)
description: Administra la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSDeploymentSettings de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534011"
---
# <a name="win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="5ed84-105">\_Clase Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="5ed84-105">Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="5ed84-106">Administra la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-106">Manages deployment settings for a virtual desktop collection.</span></span>

<span data-ttu-id="5ed84-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5ed84-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed84-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ed84-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a><span data-ttu-id="5ed84-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5ed84-109">Members</span></span>

<span data-ttu-id="5ed84-110">La **clase \_ RDMSDeploymentSettings de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5ed84-110">The **Win32\_RDMSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="5ed84-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ed84-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5ed84-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ed84-112">Methods</span></span>

<span data-ttu-id="5ed84-113">La clase **Win32 \_ RDMSDeploymentSettings** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5ed84-113">The **Win32\_RDMSDeploymentSettings** class has these methods.</span></span>



| <span data-ttu-id="5ed84-114">Método</span><span class="sxs-lookup"><span data-stu-id="5ed84-114">Method</span></span>                                                                                                  | <span data-ttu-id="5ed84-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ed84-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ed84-116">**GetBaseVHDPath**</span><span class="sxs-lookup"><span data-stu-id="5ed84-116">**GetBaseVHDPath**</span></span>](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="5ed84-117">Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-117">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="5ed84-118">**GetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="5ed84-118">**GetConnectionString**</span></span>](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | <span data-ttu-id="5ed84-119">Recupera la cadena de conexión de base de datos de nivel de implementación.</span><span class="sxs-lookup"><span data-stu-id="5ed84-119">Retrieves the deployment-level database connection string.</span></span><br/>                                                             |
| [<span data-ttu-id="5ed84-120">**GetDiffVHDPath**</span><span class="sxs-lookup"><span data-stu-id="5ed84-120">**GetDiffVHDPath**</span></span>](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="5ed84-121">Recupera la ruta de acceso al directorio en la que se implementan los discos de diferenciación para una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-121">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>            |
| [<span data-ttu-id="5ed84-122">**GetExportPath**</span><span class="sxs-lookup"><span data-stu-id="5ed84-122">**GetExportPath**</span></span>](getexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="5ed84-123">Recupera la ruta de acceso al directorio en el que se implementan las máquinas virtuales para una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-123">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                  |
| [<span data-ttu-id="5ed84-124">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="5ed84-124">**GetInt32Property**</span></span>](getint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="5ed84-125">Recupera una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-125">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                             |
| [<span data-ttu-id="5ed84-126">**GetSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="5ed84-126">**GetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | <span data-ttu-id="5ed84-127">Recupera la cadena de conexión secundaria de base de datos de nivel de implementación, que se puede usar para admitir la expiración de contraseña.</span><span class="sxs-lookup"><span data-stu-id="5ed84-127">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span><br/> |
| [<span data-ttu-id="5ed84-128">**GetSMBPath**</span><span class="sxs-lookup"><span data-stu-id="5ed84-128">**GetSMBPath**</span></span>](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="5ed84-129">Recupera la ruta de acceso UNC al recurso compartido de SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-129">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>      |
| [<span data-ttu-id="5ed84-130">**GetStringArrayDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="5ed84-130">**GetStringArrayDeploymentSetting**</span></span>](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="5ed84-131">Recupera la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-131">Retrieves the deployment settings for a virtual desktop collection.</span></span><br/>                                                    |
| [<span data-ttu-id="5ed84-132">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="5ed84-132">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="5ed84-133">Recupera una propiedad de cadena para la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-133">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="5ed84-134">**RemoveDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="5ed84-134">**RemoveDeploymentSetting**</span></span>](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | <span data-ttu-id="5ed84-135">Elimina la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-135">Deletes the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="5ed84-136">**SetBaseVHDPath**</span><span class="sxs-lookup"><span data-stu-id="5ed84-136">**SetBaseVHDPath**</span></span>](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="5ed84-137">Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-137">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="5ed84-138">**SetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="5ed84-138">**SetConnectionString**</span></span>](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | <span data-ttu-id="5ed84-139">Establece la cadena de conexión de base de datos de nivel de implementación.</span><span class="sxs-lookup"><span data-stu-id="5ed84-139">Sets the deployment-level database connection string.</span></span><br/>                                                                  |
| [<span data-ttu-id="5ed84-140">**SetDiffVHDPath**</span><span class="sxs-lookup"><span data-stu-id="5ed84-140">**SetDiffVHDPath**</span></span>](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="5ed84-141">Actualiza la ruta de acceso al directorio en la que se implementan los discos de diferenciación para una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-141">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>              |
| [<span data-ttu-id="5ed84-142">**SetExportPath**</span><span class="sxs-lookup"><span data-stu-id="5ed84-142">**SetExportPath**</span></span>](setexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="5ed84-143">Actualiza la ruta de acceso al directorio en el que se implementan las máquinas virtuales para una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-143">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                    |
| [<span data-ttu-id="5ed84-144">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="5ed84-144">**SetInt32Property**</span></span>](setint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="5ed84-145">Actualiza una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-145">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="5ed84-146">**SetSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="5ed84-146">**SetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | <span data-ttu-id="5ed84-147">Establece la cadena de conexión secundaria de base de datos de nivel de implementación.</span><span class="sxs-lookup"><span data-stu-id="5ed84-147">Sets the deployment-level database secondary connection string.</span></span><br/>                                                        |
| [<span data-ttu-id="5ed84-148">**SetSMBPath**</span><span class="sxs-lookup"><span data-stu-id="5ed84-148">**SetSMBPath**</span></span>](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="5ed84-149">Actualiza la ruta de acceso UNC al recurso compartido de SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-149">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>        |
| [<span data-ttu-id="5ed84-150">**SetStringArrayDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="5ed84-150">**SetStringArrayDeploymentSetting**</span></span>](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="5ed84-151">Actualiza la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-151">Updates the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="5ed84-152">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="5ed84-152">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="5ed84-153">Actualiza una propiedad de cadena para la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="5ed84-153">Updates a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="5ed84-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ed84-154">Requirements</span></span>



| <span data-ttu-id="5ed84-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed84-155">Requirement</span></span> | <span data-ttu-id="5ed84-156">Value</span><span class="sxs-lookup"><span data-stu-id="5ed84-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed84-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ed84-157">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed84-158">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5ed84-158">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5ed84-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ed84-159">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed84-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ed84-160">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5ed84-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5ed84-161">Namespace</span></span><br/>                | <span data-ttu-id="5ed84-162">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="5ed84-162">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5ed84-163">MOF</span><span class="sxs-lookup"><span data-stu-id="5ed84-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ed84-164"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ed84-164"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ed84-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ed84-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ed84-166"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ed84-166"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5ed84-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ed84-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed84-168">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="5ed84-168">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





