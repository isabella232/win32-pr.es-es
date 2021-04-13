---
title: Win32_RDMSPublishedApplication (clase)
description: Administra una aplicación publicada.
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSPublishedApplication clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSPublishedApplication de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb003faf5e51c9da1f46f23c5f8d6b5ae977987c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359823"
---
# <a name="win32_rdmspublishedapplication-class"></a><span data-ttu-id="f0c83-105">\_Clase Win32 RDMSPublishedApplication</span><span class="sxs-lookup"><span data-stu-id="f0c83-105">Win32\_RDMSPublishedApplication class</span></span>

<span data-ttu-id="f0c83-106">Administra una aplicación publicada.</span><span class="sxs-lookup"><span data-stu-id="f0c83-106">Manages a published application.</span></span>

<span data-ttu-id="f0c83-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f0c83-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c83-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0c83-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a><span data-ttu-id="f0c83-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0c83-109">Members</span></span>

<span data-ttu-id="f0c83-110">La **clase \_ RDMSPublishedApplication de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f0c83-110">The **Win32\_RDMSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="f0c83-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0c83-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0c83-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0c83-112">Properties</span></span>

<span data-ttu-id="f0c83-113">La **clase \_ RDMSPublishedApplication de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f0c83-113">The **Win32\_RDMSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0c83-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="f0c83-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0c83-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-117">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0c83-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-118">Obtiene y establece el alias de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-118">Gets and sets the alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-119">**AppPath**</span><span class="sxs-lookup"><span data-stu-id="f0c83-119">**AppPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0c83-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-122">Obtiene y establece la ruta de acceso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-122">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-123">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="f0c83-123">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0c83-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-126">Obtiene y establece la configuración de la línea de comandos para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-126">Gets and sets the command line setting for the application.</span></span>

<span data-ttu-id="f0c83-127">Esta propiedad puede definirse en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="f0c83-127">This property can be set to one of the following values:</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="f0c83-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span><span class="sxs-lookup"><span data-stu-id="f0c83-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f0c83-129">No se permiten argumentos de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f0c83-129">Do not allow command line arguments.</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="f0c83-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Permitir** (1)</span><span class="sxs-lookup"><span data-stu-id="f0c83-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f0c83-131">Permitir argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f0c83-131">Allow command line arguments.</span></span>

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="f0c83-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Requerir** (2)</span><span class="sxs-lookup"><span data-stu-id="f0c83-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f0c83-133">Requerir argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f0c83-133">Require command line arguments.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f0c83-134">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="f0c83-134">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0c83-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-137">Obtiene y establece el nombre para mostrar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-137">Gets and sets the display name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-138">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="f0c83-138">**Folder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0c83-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-141">Obtiene y establece la ruta de acceso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-141">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-142">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="f0c83-142">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-143">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="f0c83-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-145">Obtiene y establece una matriz que contiene el icono de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-145">Gets and sets an array that contains the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-146">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="f0c83-146">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f0c83-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-149">Obtiene y establece el índice del icono de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-149">Gets and sets the index for the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-150">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="f0c83-150">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0c83-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-153">Obtiene y establece la ruta de acceso al icono para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-153">Gets and sets the path to the icon for this application.</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-154">**Nombredegrupo**</span><span class="sxs-lookup"><span data-stu-id="f0c83-154">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0c83-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-156">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-157">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0c83-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-158">Obtiene y establece el nombre del grupo de aplicaciones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-158">Gets and sets the name of the application pool of the application.</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-159">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="f0c83-159">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0c83-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-161">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-161">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-162">Obtiene y establece los argumentos de la línea de comandos necesarios para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-162">Gets and sets the command line arguments that are required for the application</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f0c83-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0c83-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-166">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f0c83-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-167">Obtiene y establece el descriptor de seguridad que controla el acceso a la aplicación, en formato de lenguaje de definición de descriptores de seguridad (SDDL).</span><span class="sxs-lookup"><span data-stu-id="f0c83-167">Gets and sets the security descriptor that controls access to the application, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-168">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="f0c83-168">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-169">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f0c83-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-171">Indica si se va a mostrar la aplicación en Terminal Services Web Access (acceso web de TS).</span><span class="sxs-lookup"><span data-stu-id="f0c83-171">Indicates whether to display the application in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="f0c83-172">**True** para mostrar la aplicación en acceso web de TS; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f0c83-172">**TRUE** to display the application in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f0c83-173">**VirtualPath**</span><span class="sxs-lookup"><span data-stu-id="f0c83-173">**VirtualPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c83-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0c83-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c83-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0c83-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f0c83-176">Obtiene y establece la ruta de acceso virtual a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c83-176">Gets and sets the virtual path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0c83-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0c83-177">Requirements</span></span>



| <span data-ttu-id="f0c83-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0c83-178">Requirement</span></span> | <span data-ttu-id="f0c83-179">Value</span><span class="sxs-lookup"><span data-stu-id="f0c83-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c83-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0c83-180">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c83-181">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f0c83-181">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f0c83-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0c83-182">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c83-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0c83-183">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f0c83-184">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0c83-184">Namespace</span></span><br/>                | <span data-ttu-id="f0c83-185">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="f0c83-185">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f0c83-186">MOF</span><span class="sxs-lookup"><span data-stu-id="f0c83-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0c83-187"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0c83-187"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0c83-188">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0c83-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0c83-189"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0c83-189"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f0c83-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0c83-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c83-191">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="f0c83-191">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

