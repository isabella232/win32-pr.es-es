---
description: La propiedad FeatureState de solo lectura devuelve el estado instalado de una característica.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Propiedad Installer. FeatureState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653345"
---
# <a name="installerfeaturestate-property"></a><span data-ttu-id="42425-103">Propiedad Installer. FeatureState</span><span class="sxs-lookup"><span data-stu-id="42425-103">Installer.FeatureState property</span></span>

<span data-ttu-id="42425-104">La propiedad **FeatureState** de solo lectura devuelve el estado instalado de una característica.</span><span class="sxs-lookup"><span data-stu-id="42425-104">The read-only **FeatureState** property returns the installed state of a feature.</span></span>

<span data-ttu-id="42425-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="42425-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="42425-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42425-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a><span data-ttu-id="42425-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="42425-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="42425-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42425-108">Remarks</span></span>

<span data-ttu-id="42425-109">Esta propiedad devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="42425-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="42425-110">Value</span><span class="sxs-lookup"><span data-stu-id="42425-110">Value</span></span>                     | <span data-ttu-id="42425-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="42425-111">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="42425-112">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="42425-112">msiInstallStateAbsent</span></span>     | <span data-ttu-id="42425-113">La característica no está instalada.</span><span class="sxs-lookup"><span data-stu-id="42425-113">The feature is not installed.</span></span>                    |
| <span data-ttu-id="42425-114">msiInstallStateAdvertised</span><span class="sxs-lookup"><span data-stu-id="42425-114">msiInstallStateAdvertised</span></span> | <span data-ttu-id="42425-115">La característica se anuncia.</span><span class="sxs-lookup"><span data-stu-id="42425-115">The feature is advertised.</span></span>                       |
| <span data-ttu-id="42425-116">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="42425-116">msiInstallStateLocal</span></span>      | <span data-ttu-id="42425-117">La característica se instala para ejecutarse localmente.</span><span class="sxs-lookup"><span data-stu-id="42425-117">The feature is installed to run locally.</span></span>         |
| <span data-ttu-id="42425-118">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="42425-118">msiInstallStateSource</span></span>     | <span data-ttu-id="42425-119">La característica se instala para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="42425-119">The feature is installed to run from source.</span></span>     |
| <span data-ttu-id="42425-120">msiInstallStateInvalidArg</span><span class="sxs-lookup"><span data-stu-id="42425-120">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="42425-121">Se pasó un parámetro no válido a la función.</span><span class="sxs-lookup"><span data-stu-id="42425-121">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="42425-122">msiInstallStateUnknown</span><span class="sxs-lookup"><span data-stu-id="42425-122">msiInstallStateUnknown</span></span>    | <span data-ttu-id="42425-123">Se desconoce el código de producto o el ID. de característica.</span><span class="sxs-lookup"><span data-stu-id="42425-123">The product code or feature ID is unknown.</span></span>       |
| <span data-ttu-id="42425-124">msiInstallStateBadConfig</span><span class="sxs-lookup"><span data-stu-id="42425-124">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="42425-125">Los datos de configuración están dañados.</span><span class="sxs-lookup"><span data-stu-id="42425-125">The configuration data is corrupt.</span></span>               |



 

 

<span data-ttu-id="42425-126">La propiedad **FeatureState** no valida que la característica sea accesible.</span><span class="sxs-lookup"><span data-stu-id="42425-126">The **FeatureState** property does not validate that the feature is accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="42425-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42425-127">Requirements</span></span>



| <span data-ttu-id="42425-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="42425-128">Requirement</span></span> | <span data-ttu-id="42425-129">Value</span><span class="sxs-lookup"><span data-stu-id="42425-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42425-130">Versión</span><span class="sxs-lookup"><span data-stu-id="42425-130">Version</span></span><br/> | <span data-ttu-id="42425-131">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="42425-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="42425-132">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="42425-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="42425-133">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="42425-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="42425-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42425-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="42425-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42425-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="42425-136">IID</span><span class="sxs-lookup"><span data-stu-id="42425-136">IID</span></span><br/>     | <span data-ttu-id="42425-137">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="42425-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="42425-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="42425-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42425-139">**MsiQueryFeatureState**</span><span class="sxs-lookup"><span data-stu-id="42425-139">**MsiQueryFeatureState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




