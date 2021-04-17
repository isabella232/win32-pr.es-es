---
description: La propiedad FeatureUsageCount es una propiedad de solo lectura que devuelve el número de veces que se ha utilizado la característica.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Propiedad Installer. FeatureUsageCount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fbacb6b6fd5dc4d31d7c727d719e1253969c0d43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653344"
---
# <a name="installerfeatureusagecount-property"></a><span data-ttu-id="3bba0-103">Propiedad Installer. FeatureUsageCount</span><span class="sxs-lookup"><span data-stu-id="3bba0-103">Installer.FeatureUsageCount property</span></span>

<span data-ttu-id="3bba0-104">La propiedad **FeatureUsageCount** es una propiedad de solo lectura que devuelve el número de veces que se ha utilizado la característica.</span><span class="sxs-lookup"><span data-stu-id="3bba0-104">The **FeatureUsageCount** property is a read-only property that returns the number of times the feature has been used.</span></span>

<span data-ttu-id="3bba0-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3bba0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bba0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bba0-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a><span data-ttu-id="3bba0-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3bba0-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3bba0-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3bba0-108">Remarks</span></span>

<span data-ttu-id="3bba0-109">El uso de los métodos [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) o [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) o sus equivalentes de API en la característica especificada incrementa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3bba0-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature increments this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bba0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bba0-110">Requirements</span></span>



| <span data-ttu-id="3bba0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bba0-111">Requirement</span></span> | <span data-ttu-id="3bba0-112">Value</span><span class="sxs-lookup"><span data-stu-id="3bba0-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bba0-113">Versión</span><span class="sxs-lookup"><span data-stu-id="3bba0-113">Version</span></span><br/> | <span data-ttu-id="3bba0-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3bba0-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3bba0-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3bba0-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3bba0-116">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="3bba0-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3bba0-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3bba0-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="3bba0-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bba0-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3bba0-119">IID</span><span class="sxs-lookup"><span data-stu-id="3bba0-119">IID</span></span><br/>     | <span data-ttu-id="3bba0-120">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3bba0-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="3bba0-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bba0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bba0-122">**MsiGetFeatureUsage**</span><span class="sxs-lookup"><span data-stu-id="3bba0-122">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




