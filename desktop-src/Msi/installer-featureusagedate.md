---
description: La propiedad FeatureUsageDate es una propiedad de solo lectura que devuelve la fecha en que se usó por última vez la característica especificada.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Propiedad Installer. FeatureUsageDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653340"
---
# <a name="installerfeatureusagedate-property"></a><span data-ttu-id="18f4f-103">Propiedad Installer. FeatureUsageDate</span><span class="sxs-lookup"><span data-stu-id="18f4f-103">Installer.FeatureUsageDate property</span></span>

<span data-ttu-id="18f4f-104">La propiedad **FeatureUsageDate** es una propiedad de solo lectura que devuelve la fecha en que se usó por última vez la característica especificada.</span><span class="sxs-lookup"><span data-stu-id="18f4f-104">The **FeatureUsageDate** property is a read-only property that returns the date the specified feature was last used.</span></span>

<span data-ttu-id="18f4f-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="18f4f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="18f4f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18f4f-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a><span data-ttu-id="18f4f-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="18f4f-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="18f4f-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18f4f-108">Remarks</span></span>

<span data-ttu-id="18f4f-109">El uso de los métodos [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) o [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) o sus equivalentes de API en la característica especificada establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="18f4f-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature sets this property.</span></span>

<span data-ttu-id="18f4f-110">La fecha está en el formato de fecha de MS-DOS, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="18f4f-110">The date is in the MS-DOS date format as shown in the following table.</span></span>



| <span data-ttu-id="18f4f-111">Bits</span><span class="sxs-lookup"><span data-stu-id="18f4f-111">Bits</span></span> | <span data-ttu-id="18f4f-112">Contenido</span><span class="sxs-lookup"><span data-stu-id="18f4f-112">Contents</span></span>                                            |
|------|-----------------------------------------------------|
| <span data-ttu-id="18f4f-113">0-4</span><span class="sxs-lookup"><span data-stu-id="18f4f-113">0-4</span></span>  | <span data-ttu-id="18f4f-114">Día del mes (1-31)</span><span class="sxs-lookup"><span data-stu-id="18f4f-114">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="18f4f-115">5-8</span><span class="sxs-lookup"><span data-stu-id="18f4f-115">5-8</span></span>  | <span data-ttu-id="18f4f-116">Mes (1 = enero, 2 = febrero, etc.)</span><span class="sxs-lookup"><span data-stu-id="18f4f-116">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="18f4f-117">9-15</span><span class="sxs-lookup"><span data-stu-id="18f4f-117">9-15</span></span> | <span data-ttu-id="18f4f-118">Desplazamiento de año desde 1980 (agregue 1980 para obtener el año real)</span><span class="sxs-lookup"><span data-stu-id="18f4f-118">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="18f4f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18f4f-119">Requirements</span></span>



| <span data-ttu-id="18f4f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="18f4f-120">Requirement</span></span> | <span data-ttu-id="18f4f-121">Value</span><span class="sxs-lookup"><span data-stu-id="18f4f-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18f4f-122">Versión</span><span class="sxs-lookup"><span data-stu-id="18f4f-122">Version</span></span><br/> | <span data-ttu-id="18f4f-123">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="18f4f-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="18f4f-124">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="18f4f-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="18f4f-125">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="18f4f-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="18f4f-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18f4f-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="18f4f-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18f4f-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="18f4f-128">IID</span><span class="sxs-lookup"><span data-stu-id="18f4f-128">IID</span></span><br/>     | <span data-ttu-id="18f4f-129">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="18f4f-129">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="18f4f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="18f4f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f4f-131">**MsiGetFeatureUsage**</span><span class="sxs-lookup"><span data-stu-id="18f4f-131">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




