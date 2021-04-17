---
description: La propiedad FeatureValidStates del objeto de sesión devuelve un entero que representa las marcas de bits con cada bit pertinente que representa un estado de instalación válido de la característica especificada.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Propiedad Session. FeatureValidStates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653826"
---
# <a name="sessionfeaturevalidstates-property"></a><span data-ttu-id="2008f-103">Propiedad Session. FeatureValidStates</span><span class="sxs-lookup"><span data-stu-id="2008f-103">Session.FeatureValidStates property</span></span>

<span data-ttu-id="2008f-104">La propiedad **FeatureValidStates** del objeto de [**sesión**](session-object.md) devuelve un entero que representa las marcas de bits con cada bit pertinente que representa un estado de instalación válido de la característica especificada.</span><span class="sxs-lookup"><span data-stu-id="2008f-104">The **FeatureValidStates** property of the [**Session**](session-object.md) object returns an integer representing bit flags with each relevant bit representing a valid installation state for the specified feature.</span></span>

<span data-ttu-id="2008f-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2008f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2008f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2008f-106">Syntax</span></span>


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a><span data-ttu-id="2008f-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2008f-107">Property value</span></span>

<span data-ttu-id="2008f-108">Nombre de cadena necesario del elemento de característica cuyos Estados de instalación válidos se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="2008f-108">Required string name of the feature item whose valid installation states are to be retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="2008f-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2008f-109">Remarks</span></span>

<span data-ttu-id="2008f-110">El valor devuelto se compone de marcas de bits como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="2008f-110">The return value is composed of bit flags as follows.</span></span> <span data-ttu-id="2008f-111">Bit 0: si se establece, local es un estado válido.</span><span class="sxs-lookup"><span data-stu-id="2008f-111">Bit 0: if set, Local is a valid state.</span></span> <span data-ttu-id="2008f-112">Bit 1: si se establece, el origen es un estado válido.</span><span class="sxs-lookup"><span data-stu-id="2008f-112">Bit 1: if set, Source is a valid state.</span></span>

<span data-ttu-id="2008f-113">La propiedad **FeatureValidStates** solo se realiza correctamente después de que el instalador haya llamado a las acciones [CostInitialize](costinitialize-action.md) y [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2008f-113">The **FeatureValidStates** property only succeeds after the installer has called the [CostInitialize](costinitialize-action.md) and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="2008f-114">**FeatureValidStates** determina la validez del estado mediante la consulta de todos los componentes que están vinculados a la característica especificada sin tener en cuenta el estado de instalación actual de ningún componente.</span><span class="sxs-lookup"><span data-stu-id="2008f-114">**FeatureValidStates** determines state validity by querying all components that are linked to the specified feature without taking into account the current installed state of any component.</span></span>

<span data-ttu-id="2008f-115">Los posibles estados válidos para una característica se determinan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2008f-115">The possible valid states for a feature are determined as follows:</span></span>

-   <span data-ttu-id="2008f-116">Si la característica no contiene componentes, tanto \_ \_ el origen de installstate local como el de installstate son Estados válidos para la característica.</span><span class="sxs-lookup"><span data-stu-id="2008f-116">If the feature does not contain components, both INSTALLSTATE\_LOCAL and INSTALLSTATE\_SOURCE are valid states for the feature.</span></span>
-   <span data-ttu-id="2008f-117">Si al menos un componente de la característica tiene un atributo de msidbComponentAttributesLocalOnly o msidbComponentAttributesOptional, INSTALLSTATE \_ local es un estado válido para la característica.</span><span class="sxs-lookup"><span data-stu-id="2008f-117">If at least one component of the feature has an attribute of msidbComponentAttributesLocalOnly or msidbComponentAttributesOptional, INSTALLSTATE\_LOCAL is a valid state for the feature.</span></span>
-   <span data-ttu-id="2008f-118">Si al menos un componente de la característica tiene un atributo de msidbComponentAttributesSourceOnly o msidbComponentAttributesOptional, \_ el origen de INSTALLSTATE es un estado válido para la característica.</span><span class="sxs-lookup"><span data-stu-id="2008f-118">If at least one component of the feature has an attribute of msidbComponentAttributesSourceOnly or msidbComponentAttributesOptional, INSTALLSTATE\_SOURCE is a valid state for the feature.</span></span>
-   <span data-ttu-id="2008f-119">Si se aplica una revisión a un archivo de un componente que pertenece a la característica o desde un origen comprimido, \_ el origen de INSTALLSTATE no se incluye como un estado válido para la característica.</span><span class="sxs-lookup"><span data-stu-id="2008f-119">If a file of a component belonging to the feature is patched or from a compressed source, then INSTALLSTATE\_SOURCE is not included as a valid state for the feature.</span></span>
-   <span data-ttu-id="2008f-120">INSTALLSTATE \_ anunciar no es un estado válido si la característica no permite el anuncio (msidbFeatureAttributesDisallowAdvertise) o la característica requiere compatibilidad con la plataforma para el anuncio (msidbFeatureAttributesNoUnsupportedAdvertise) y la plataforma no lo admite.</span><span class="sxs-lookup"><span data-stu-id="2008f-120">INSTALLSTATE\_ADVERTISE is not a valid state if the feature disallows advertisement (msidbFeatureAttributesDisallowAdvertise) or the feature requires platform support for advertisement (msidbFeatureAttributesNoUnsupportedAdvertise) and the platform does not support it.</span></span>
-   <span data-ttu-id="2008f-121">INSTALLSTATE \_ ausente es un estado válido para la característica si sus atributos no incluyen msidbFeatureAttributesUIDisallowAbsent.</span><span class="sxs-lookup"><span data-stu-id="2008f-121">INSTALLSTATE\_ABSENT is a valid state for the feature if its attributes do not include msidbFeatureAttributesUIDisallowAbsent.</span></span>
-   <span data-ttu-id="2008f-122">Los Estados válidos para las características secundarias marcadas para seguir la característica primaria (msidbFeatureAttributesFollowParent) se basan en la acción o el estado instalado de la característica primaria.</span><span class="sxs-lookup"><span data-stu-id="2008f-122">Valid states for child features marked to follow the parent feature (msidbFeatureAttributesFollowParent) are based upon the parent feature's action or installed state.</span></span>

<span data-ttu-id="2008f-123">Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="2008f-123">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2008f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2008f-124">Requirements</span></span>



| <span data-ttu-id="2008f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2008f-125">Requirement</span></span> | <span data-ttu-id="2008f-126">Value</span><span class="sxs-lookup"><span data-stu-id="2008f-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2008f-127">Versión</span><span class="sxs-lookup"><span data-stu-id="2008f-127">Version</span></span><br/> | <span data-ttu-id="2008f-128">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2008f-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2008f-129">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2008f-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2008f-130">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="2008f-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2008f-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2008f-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="2008f-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2008f-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2008f-133">IID</span><span class="sxs-lookup"><span data-stu-id="2008f-133">IID</span></span><br/>     | <span data-ttu-id="2008f-134">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2008f-134">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




