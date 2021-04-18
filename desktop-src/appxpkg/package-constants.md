---
title: Constantes de paquete (AppModel. h)
description: Especifica cómo se van a procesar los paquetes.
ms.assetid: 72E565C3-6CFD-47E3-8BAC-17D6E86B99DA
topic_type:
- apiref
api_name:
- PACKAGE_APPLICATIONS_MAX_COUNT
- PACKAGE_APPLICATIONS_MIN_COUNT
- PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES
- PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES
- PACKAGE_FILTER_ALL_LOADED
- PACKAGE_FILTER_BUNDLE
- PACKAGE_FILTER_DIRECT
- PACKAGE_FILTER_HEAD
- PACKAGE_FILTER_OPTIONAL
- PACKAGE_FILTER_RESOURCE
- PACKAGE_GRAPH_MAX_SIZE
- PACKAGE_GRAPH_MIN_SIZE
- PACKAGE_INFORMATION_BASIC
- PACKAGE_INFORMATION_FULL
- PACKAGE_MAX_DEPENDENCIES
- PACKAGE_MIN_DEPENDENCIES
- PACKAGE_PROPERTY_BUNDLE
- PACKAGE_PROPERTY_DEVELOPMENT_MODE
- PACKAGE_PROPERTY_FRAMEWORK
- PACKAGE_PROPERTY_OPTIONAL
- PACKAGE_PROPERTY_RESOURCE
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb3a4630eb6e132c7a82ea6b45839f6d2684cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705125"
---
# <a name="package-constants"></a><span data-ttu-id="30755-103">Constantes de paquete</span><span class="sxs-lookup"><span data-stu-id="30755-103">Package constants</span></span>

<span data-ttu-id="30755-104">Especifica cómo se van a procesar los paquetes.</span><span class="sxs-lookup"><span data-stu-id="30755-104">Specifies how packages are to be processed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="30755-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="30755-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="30755-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="30755-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_APPLICATIONS_MAX_COUNT"></span><span id="package_applications_max_count"></span><dl> <span data-ttu-id="30755-107"><dt><strong>PACKAGE_APPLICATIONS_MAX_COUNT</strong></dt> <dt>100</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-107"><dt><strong>PACKAGE_APPLICATIONS_MAX_COUNT</strong></dt> <dt>100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-108">El número máximo de aplicaciones en un paquete.</span><span class="sxs-lookup"><span data-stu-id="30755-108">The maximum number of apps in a package.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_APPLICATIONS_MIN_COUNT"></span><span id="package_applications_min_count"></span><dl> <span data-ttu-id="30755-109"><dt><strong>PACKAGE_APPLICATIONS_MIN_COUNT</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-109"><dt><strong>PACKAGE_APPLICATIONS_MIN_COUNT</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-110">El número mínimo de aplicaciones en un paquete.</span><span class="sxs-lookup"><span data-stu-id="30755-110">The minimum number of apps in a package.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES"></span><span id="package_family_max_resource_packages"></span><dl> <span data-ttu-id="30755-111"><dt><strong>PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES</strong></dt> <dt>512</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-111"><dt><strong>PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES</strong></dt> <dt>512</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-112">Número máximo de paquetes de recursos que puede tener un paquete.</span><span class="sxs-lookup"><span data-stu-id="30755-112">The maximum number of resource packages a package can have.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES"></span><span id="package_family_min_resource_packages"></span><dl> <span data-ttu-id="30755-113"><dt><strong>PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-113"><dt><strong>PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-114">El número mínimo de paquetes de recursos que puede tener un paquete.</span><span class="sxs-lookup"><span data-stu-id="30755-114">The minimum number of resource packages a package can have.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_ALL_LOADED"></span><span id="package_filter_all_loaded"></span><dl> <span data-ttu-id="30755-115"><dt><strong>PACKAGE_FILTER_ALL_LOADED</strong></dt> <dt>0x00000000</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-115"><dt><strong>PACKAGE_FILTER_ALL_LOADED</strong></dt> <dt>0x00000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-116">Procesa todos los paquetes en el gráfico de dependencias.</span><span class="sxs-lookup"><span data-stu-id="30755-116">Process all packages in the dependency graph.</span></span><br/> <span data-ttu-id="30755-117">Esto es equivalente a <strong>PACKAGE_FILTER_HEAD</strong>  |  <strong>PACKAGE_FILTER_DIRECT</strong>.</span><span class="sxs-lookup"><span data-stu-id="30755-117">This is equivalent to <strong>PACKAGE_FILTER_HEAD</strong> | <strong>PACKAGE_FILTER_DIRECT</strong>.</span></span><br/>
<blockquote>
[!Note]<br /><span data-ttu-id="30755-118">
<strong>PACKAGE_FILTER_ALL_LOADED</strong> pueden modificarse o no estar disponibles para versiones posteriores a Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="30755-118">
<strong>PACKAGE_FILTER_ALL_LOADED</strong> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="30755-119">En su lugar, utilice <strong>PACKAGE_FILTER_HEAD</strong>  |  <strong>PACKAGE_FILTER_DIRECT</strong>.</span><span class="sxs-lookup"><span data-stu-id="30755-119">Instead, use <strong>PACKAGE_FILTER_HEAD</strong> | <strong>PACKAGE_FILTER_DIRECT</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_BUNDLE"></span><span id="package_filter_bundle"></span><dl> <span data-ttu-id="30755-120"><dt><strong>PACKAGE_FILTER_BUNDLE</strong></dt> <dt>0x00000080</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-120"><dt><strong>PACKAGE_FILTER_BUNDLE</strong></dt> <dt>0x00000080</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-121">Procesar paquetes de agrupación en el gráfico de paquetes.</span><span class="sxs-lookup"><span data-stu-id="30755-121">Process bundle packages in the package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_DIRECT"></span><span id="package_filter_direct"></span><dl> <span data-ttu-id="30755-122"><dt><strong>PACKAGE_FILTER_DIRECT</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-122"><dt><strong>PACKAGE_FILTER_DIRECT</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-123">Procese los paquetes dependientes directamente del paquete principal (primero) del gráfico de dependencias.</span><span class="sxs-lookup"><span data-stu-id="30755-123">Process the directly dependent packages of the head (first) package in the dependency graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_HEAD"></span><span id="package_filter_head"></span><dl> <span data-ttu-id="30755-124"><dt><strong>PACKAGE_FILTER_HEAD</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-124"><dt><strong>PACKAGE_FILTER_HEAD</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-125">Procesa el primer paquete del gráfico de dependencias.</span><span class="sxs-lookup"><span data-stu-id="30755-125">Process the first package in the dependency graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_OPTIONAL"></span><span id="package_filter_optional"></span><dl> <span data-ttu-id="30755-126"><dt><strong>PACKAGE_FILTER_OPTIONAL</strong></dt> <dt>0x00020000</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-126"><dt><strong>PACKAGE_FILTER_OPTIONAL</strong></dt> <dt>0x00020000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-127">Procesar paquetes de agrupación en el gráfico de paquetes.</span><span class="sxs-lookup"><span data-stu-id="30755-127">Process bundle packages in the package graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_RESOURCE"></span><span id="package_filter_resource"></span><dl> <span data-ttu-id="30755-128"><dt><strong>PACKAGE_FILTER_RESOURCE</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-128"><dt><strong>PACKAGE_FILTER_RESOURCE</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-129">Procesar paquetes de recursos en el gráfico de paquetes.</span><span class="sxs-lookup"><span data-stu-id="30755-129">Process resource packages in the package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_GRAPH_MAX_SIZE"></span><span id="package_graph_max_size"></span><dl> <span data-ttu-id="30755-130"><dt><strong>PACKAGE_GRAPH_MAX_SIZE</strong></dt> <dt>(1 + PACKAGE_MAX_DEPENDENCIES + PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES)</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-130"><dt><strong>PACKAGE_GRAPH_MAX_SIZE</strong></dt> <dt>(1 + PACKAGE_MAX_DEPENDENCIES + PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-131">Tamaño máximo de un gráfico de paquete.</span><span class="sxs-lookup"><span data-stu-id="30755-131">The maximum size of a package graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_GRAPH_MIN_SIZE"></span><span id="package_graph_min_size"></span><dl> <span data-ttu-id="30755-132"><dt><strong>PACKAGE_GRAPH_MIN_SIZE</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-132"><dt><strong>PACKAGE_GRAPH_MIN_SIZE</strong></dt> <dt>1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-133">El tamaño mínimo de un gráfico de paquete.</span><span class="sxs-lookup"><span data-stu-id="30755-133">The minimum size of a package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_INFORMATION_BASIC"></span><span id="package_information_basic"></span><dl> <span data-ttu-id="30755-134"><dt><strong>PACKAGE_INFORMATION_BASIC</strong></dt> <dt>0x00000000</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-134"><dt><strong>PACKAGE_INFORMATION_BASIC</strong></dt> <dt>0x00000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-135">Recuperar información básica.</span><span class="sxs-lookup"><span data-stu-id="30755-135">Retrieve basic information.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_INFORMATION_FULL"></span><span id="package_information_full"></span><dl> <span data-ttu-id="30755-136"><dt><strong>PACKAGE_INFORMATION_FULL</strong></dt> <dt>0x00000100</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-136"><dt><strong>PACKAGE_INFORMATION_FULL</strong></dt> <dt>0x00000100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-137">Recupere toda la información.</span><span class="sxs-lookup"><span data-stu-id="30755-137">Retrieve full information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_MAX_DEPENDENCIES"></span><span id="package_max_dependencies"></span><dl> <span data-ttu-id="30755-138"><dt><strong>PACKAGE_MAX_DEPENDENCIES</strong></dt> <dt>128</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-138"><dt><strong>PACKAGE_MAX_DEPENDENCIES</strong></dt> <dt>128</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-139">Número máximo de paquetes de los que depende un paquete.</span><span class="sxs-lookup"><span data-stu-id="30755-139">The maximum number of packages a package depends on.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_MIN_DEPENDENCIES"></span><span id="package_min_dependencies"></span><dl> <span data-ttu-id="30755-140"><dt><strong>PACKAGE_MIN_DEPENDENCIES</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-140"><dt><strong>PACKAGE_MIN_DEPENDENCIES</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-141">Número mínimo de paquetes de los que depende un paquete.</span><span class="sxs-lookup"><span data-stu-id="30755-141">The minimum number of packages a package depends on.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_BUNDLE"></span><span id="package_property_bundle"></span><dl> <span data-ttu-id="30755-142"><dt><strong>PACKAGE_PROPERTY_BUNDLE</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-142"><dt><strong>PACKAGE_PROPERTY_BUNDLE</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-143">El paquete es un paquete de paquetes.</span><span class="sxs-lookup"><span data-stu-id="30755-143">The package is a bundle package.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_DEVELOPMENT_MODE"></span><span id="package_property_development_mode"></span><dl> <span data-ttu-id="30755-144"><dt><strong>PACKAGE_PROPERTY_DEVELOPMENT_MODE</strong></dt> <dt>0x00010000</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-144"><dt><strong>PACKAGE_PROPERTY_DEVELOPMENT_MODE</strong></dt> <dt>0x00010000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-145">El paquete se registró con la enumeración <a href="/uwp/api/Windows.Management.Deployment.DeploymentOptions"><strong>archivo deploymentoptions</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="30755-145">The package was registered with the <a href="/uwp/api/Windows.Management.Deployment.DeploymentOptions"><strong>DeploymentOptions</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_FRAMEWORK"></span><span id="package_property_framework"></span><dl> <span data-ttu-id="30755-146"><dt><strong>PACKAGE_PROPERTY_FRAMEWORK</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-146"><dt><strong>PACKAGE_PROPERTY_FRAMEWORK</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-147">El paquete es un marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="30755-147">The package is a framework.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_OPTIONAL"></span><span id="package_property_optional"></span><dl> <span data-ttu-id="30755-148"><dt><strong>PACKAGE_PROPERTY_OPTIONAL</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-148"><dt><strong>PACKAGE_PROPERTY_OPTIONAL</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-149">El paquete es un paquete opcional.</span><span class="sxs-lookup"><span data-stu-id="30755-149">The package is an optional package.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_RESOURCE"></span><span id="package_property_resource"></span><dl> <span data-ttu-id="30755-150"><dt><strong>PACKAGE_PROPERTY_RESOURCE</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="30755-150"><dt><strong>PACKAGE_PROPERTY_RESOURCE</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="30755-151">El paquete es un paquete de recursos.</span><span class="sxs-lookup"><span data-stu-id="30755-151">The package is a resource package.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="30755-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30755-152">Requirements</span></span>



| <span data-ttu-id="30755-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="30755-153">Requirement</span></span> | <span data-ttu-id="30755-154">Value</span><span class="sxs-lookup"><span data-stu-id="30755-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30755-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30755-155">Minimum supported client</span></span><br/> | <span data-ttu-id="30755-156">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="30755-156">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="30755-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30755-157">Minimum supported server</span></span><br/> | <span data-ttu-id="30755-158">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="30755-158">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30755-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30755-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="30755-160"><dt>AppModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="30755-160"><dt>AppModel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30755-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="30755-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30755-162">**GetCurrentPackageInfo**</span><span class="sxs-lookup"><span data-stu-id="30755-162">**GetCurrentPackageInfo**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)
</dt> <dt>

[<span data-ttu-id="30755-163">**GetPackageInfo**</span><span class="sxs-lookup"><span data-stu-id="30755-163">**GetPackageInfo**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)
</dt> <dt>

[<span data-ttu-id="30755-164">**PackageIdFromFullName**</span><span class="sxs-lookup"><span data-stu-id="30755-164">**PackageIdFromFullName**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)
</dt> </dl>

 

