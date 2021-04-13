---
title: Win32_RDMSFileTypeAssociation (clase)
description: Administra una asociación de tipo de archivo para una aplicación publicada.
ms.assetid: 22c945cb-4c47-431a-bc9b-d33ba15c8ab3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSFileTypeAssociation clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSFileTypeAssociation de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSFileTypeAssociation
- Win32_RDMSFileTypeAssociation.AppAlias
- Win32_RDMSFileTypeAssociation.PoolName
- Win32_RDMSFileTypeAssociation.ExtName
- Win32_RDMSFileTypeAssociation.ProgIdHint
- Win32_RDMSFileTypeAssociation.IconPath
- Win32_RDMSFileTypeAssociation.IconIndex
- Win32_RDMSFileTypeAssociation.IconContents
- Win32_RDMSFileTypeAssociation.IsPrimaryHandler
- Win32_RDMSFileTypeAssociation.IsPublished
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2e569077bf47a2b0eba63db39ae1e86c39feb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421966"
---
# <a name="win32_rdmsfiletypeassociation-class"></a><span data-ttu-id="26311-105">\_Clase Win32 RDMSFileTypeAssociation</span><span class="sxs-lookup"><span data-stu-id="26311-105">Win32\_RDMSFileTypeAssociation class</span></span>

<span data-ttu-id="26311-106">Administra una asociación de tipo de archivo para una aplicación publicada.</span><span class="sxs-lookup"><span data-stu-id="26311-106">Manages a file type association for a published application.</span></span>

<span data-ttu-id="26311-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="26311-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26311-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26311-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSFileTypeAssociation
{
  string  AppAlias;
  string  PoolName;
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean IsPrimaryHandler;
  boolean IsPublished;
};
```

## <a name="members"></a><span data-ttu-id="26311-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="26311-109">Members</span></span>

<span data-ttu-id="26311-110">La **clase \_ RDMSFileTypeAssociation de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="26311-110">The **Win32\_RDMSFileTypeAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="26311-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26311-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26311-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26311-112">Properties</span></span>

<span data-ttu-id="26311-113">La **clase \_ RDMSFileTypeAssociation de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="26311-113">The **Win32\_RDMSFileTypeAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26311-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="26311-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26311-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26311-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26311-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26311-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="26311-117">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26311-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26311-118">Obtiene y establece el alias de la aplicación que está asociada al tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="26311-118">Gets and sets the alias of the application that is associated with the file type.</span></span>

</dd> <dt>

<span data-ttu-id="26311-119">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="26311-119">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26311-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26311-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26311-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26311-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26311-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26311-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26311-123">Obtiene el nombre de la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="26311-123">Gets the name of the file extension.</span></span>

</dd> <dt>

<span data-ttu-id="26311-124">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="26311-124">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26311-125">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="26311-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="26311-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26311-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="26311-127">Obtiene y establece el contenido del icono para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="26311-127">Gets and sets the content of the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="26311-128">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="26311-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26311-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="26311-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26311-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26311-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="26311-131">Obtiene y establece el índice del icono para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="26311-131">Gets and sets the index to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="26311-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="26311-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26311-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26311-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26311-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26311-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="26311-135">Obtiene y establece la ruta de acceso al icono para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="26311-135">Gets and sets the path to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="26311-136">**IsPrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="26311-136">**IsPrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26311-137">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26311-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26311-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26311-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="26311-139">Obtiene y establece un valor que indica si la Asociación de tipo de archivo es para el controlador principal.</span><span class="sxs-lookup"><span data-stu-id="26311-139">Gets and sets a value that indicates whether the file type association is for the primary handler.</span></span> <span data-ttu-id="26311-140">**True** si la Asociación de tipo de archivo es para el controlador principal; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="26311-140">**TRUE** if the file type association is for the primary handler; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="26311-141">**IsPublished**</span><span class="sxs-lookup"><span data-stu-id="26311-141">**IsPublished**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26311-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26311-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26311-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26311-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="26311-144">Indica si este FTA está publicado.</span><span class="sxs-lookup"><span data-stu-id="26311-144">Whether this FTA is published.</span></span>

<span data-ttu-id="26311-145">Obtiene y establece un valor que indica si se publica la Asociación de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="26311-145">Gets and sets a value that indicates whether the file type association is published.</span></span> <span data-ttu-id="26311-146">**True** si se publica la Asociación de tipo de archivo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="26311-146">**TRUE** if the file type association is published; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="26311-147">**Nombredegrupo**</span><span class="sxs-lookup"><span data-stu-id="26311-147">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26311-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26311-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26311-149">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26311-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="26311-150">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26311-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26311-151">Obtiene y establece el nombre del grupo de aplicaciones para la Asociación de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="26311-151">Gets and sets the name of the application pool for the file type association.</span></span>

</dd> <dt>

<span data-ttu-id="26311-152">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="26311-152">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26311-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26311-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26311-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26311-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26311-155">Obtiene una sugerencia para ayudar a los usuarios a abrir la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="26311-155">Gets a hint to help users open the file extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26311-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26311-156">Requirements</span></span>



| <span data-ttu-id="26311-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="26311-157">Requirement</span></span> | <span data-ttu-id="26311-158">Value</span><span class="sxs-lookup"><span data-stu-id="26311-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="26311-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26311-159">Minimum supported client</span></span><br/> | <span data-ttu-id="26311-160">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="26311-160">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="26311-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26311-161">Minimum supported server</span></span><br/> | <span data-ttu-id="26311-162">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26311-162">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="26311-163">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="26311-163">Namespace</span></span><br/>                | <span data-ttu-id="26311-164">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="26311-164">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="26311-165">MOF</span><span class="sxs-lookup"><span data-stu-id="26311-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26311-166"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26311-166"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="26311-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26311-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26311-168"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26311-168"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="26311-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="26311-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26311-170">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="26311-170">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

