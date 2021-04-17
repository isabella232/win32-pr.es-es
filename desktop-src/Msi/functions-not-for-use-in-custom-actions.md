---
description: Nunca se debe llamar a las siguientes funciones de base de datos desde una acción personalizada.
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: Funciones que no se usan en acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c77c4714ca65614200cf77d6b207b6eebcaf179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667790"
---
# <a name="functions-not-for-use-in-custom-actions"></a><span data-ttu-id="0b9de-103">Funciones que no se usan en acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="0b9de-103">Functions Not for Use in Custom Actions</span></span>

<span data-ttu-id="0b9de-104">Nunca se debe llamar a las siguientes [funciones de base de datos](database-functions.md) desde una acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="0b9de-104">The following [Database Functions](database-functions.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="0b9de-105">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="0b9de-105">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="0b9de-106">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="0b9de-106">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="0b9de-107">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="0b9de-107">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [<span data-ttu-id="0b9de-108">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="0b9de-108">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [<span data-ttu-id="0b9de-109">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="0b9de-109">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [<span data-ttu-id="0b9de-110">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="0b9de-110">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [<span data-ttu-id="0b9de-111">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="0b9de-111">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [<span data-ttu-id="0b9de-112">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="0b9de-112">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [<span data-ttu-id="0b9de-113">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="0b9de-113">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [<span data-ttu-id="0b9de-114">**MsiEnableLog**</span><span class="sxs-lookup"><span data-stu-id="0b9de-114">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="0b9de-115">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="0b9de-115">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [<span data-ttu-id="0b9de-116">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="0b9de-116">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [<span data-ttu-id="0b9de-117">**MsiOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="0b9de-117">**MsiOpenDatabase**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [<span data-ttu-id="0b9de-118">**MsiPreviewBillboard**</span><span class="sxs-lookup"><span data-stu-id="0b9de-118">**MsiPreviewBillboard**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [<span data-ttu-id="0b9de-119">**MsiPreviewDialog**</span><span class="sxs-lookup"><span data-stu-id="0b9de-119">**MsiPreviewDialog**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [<span data-ttu-id="0b9de-120">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="0b9de-120">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="0b9de-121">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="0b9de-121">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="0b9de-122">**MsiSetExternalUIRecord**</span><span class="sxs-lookup"><span data-stu-id="0b9de-122">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="0b9de-123">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="0b9de-123">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

<span data-ttu-id="0b9de-124">Nunca se debe llamar a las siguientes [funciones de instalador](installer-function-reference.md) desde una acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="0b9de-124">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="0b9de-125">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="0b9de-125">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [<span data-ttu-id="0b9de-126">**MsiCollectUserInfo**</span><span class="sxs-lookup"><span data-stu-id="0b9de-126">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [<span data-ttu-id="0b9de-127">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="0b9de-127">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [<span data-ttu-id="0b9de-128">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="0b9de-128">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="0b9de-129">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="0b9de-129">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="0b9de-130">**MsiEnableLog**</span><span class="sxs-lookup"><span data-stu-id="0b9de-130">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="0b9de-131">**MsiGetFeatureInfo**</span><span class="sxs-lookup"><span data-stu-id="0b9de-131">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [<span data-ttu-id="0b9de-132">**MsiGetProductCode**</span><span class="sxs-lookup"><span data-stu-id="0b9de-132">**MsiGetProductCode**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [<span data-ttu-id="0b9de-133">**MsiGetProductProperty**</span><span class="sxs-lookup"><span data-stu-id="0b9de-133">**MsiGetProductProperty**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [<span data-ttu-id="0b9de-134">**MsiInstallMissingComponent**</span><span class="sxs-lookup"><span data-stu-id="0b9de-134">**MsiInstallMissingComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [<span data-ttu-id="0b9de-135">**MsiInstallMissingFile**</span><span class="sxs-lookup"><span data-stu-id="0b9de-135">**MsiInstallMissingFile**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [<span data-ttu-id="0b9de-136">**MsiInstallProduct**</span><span class="sxs-lookup"><span data-stu-id="0b9de-136">**MsiInstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [<span data-ttu-id="0b9de-137">**MsiOpenPackage**</span><span class="sxs-lookup"><span data-stu-id="0b9de-137">**MsiOpenPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [<span data-ttu-id="0b9de-138">**MsiOpenProduct**</span><span class="sxs-lookup"><span data-stu-id="0b9de-138">**MsiOpenProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [<span data-ttu-id="0b9de-139">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="0b9de-139">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [<span data-ttu-id="0b9de-140">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="0b9de-140">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="0b9de-141">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="0b9de-141">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="0b9de-142">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="0b9de-142">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [<span data-ttu-id="0b9de-143">**MsiUseFeature**</span><span class="sxs-lookup"><span data-stu-id="0b9de-143">**MsiUseFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [<span data-ttu-id="0b9de-144">**MsiUseFeatureEx**</span><span class="sxs-lookup"><span data-stu-id="0b9de-144">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [<span data-ttu-id="0b9de-145">**MsiVerifyPackage**</span><span class="sxs-lookup"><span data-stu-id="0b9de-145">**MsiVerifyPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

<span data-ttu-id="0b9de-146">Nunca se debe llamar a las siguientes [funciones de instalador](installer-function-reference.md) desde una acción personalizada si al hacerlo se inicia otra instalación.</span><span class="sxs-lookup"><span data-stu-id="0b9de-146">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action if doing so starts another installation.</span></span> <span data-ttu-id="0b9de-147">Pueden llamarse desde una acción personalizada que no inicia otra instalación.</span><span class="sxs-lookup"><span data-stu-id="0b9de-147">They may be called from a custom action that does not start another installation.</span></span>

-   [<span data-ttu-id="0b9de-148">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="0b9de-148">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [<span data-ttu-id="0b9de-149">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="0b9de-149">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [<span data-ttu-id="0b9de-150">**MsiProvideQualifiedComponentEx**</span><span class="sxs-lookup"><span data-stu-id="0b9de-150">**MsiProvideQualifiedComponentEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

<span data-ttu-id="0b9de-151">Una acción personalizada nunca debe generar un nuevo subproceso que use funciones de Windows Installer para cambiar el estado de la característica, el estado del componente o para enviar mensajes desde un evento de control.</span><span class="sxs-lookup"><span data-stu-id="0b9de-151">A custom action should never spawn a new thread that uses Windows Installer functions to change the feature state, component state, or to send messages from a Control Event.</span></span> <span data-ttu-id="0b9de-152">Si intenta hacerlo, se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="0b9de-152">Attempting to do this causes the installation to fail.</span></span>

 

 



