---
description: La propiedad FeatureCurrentState del objeto de sesión es una propiedad de solo lectura que devuelve el estado instalado actual de la característica designada. Para los valores de estado, consulte la propiedad FeatureRequestState.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Propiedad Session. FeatureCurrentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680408"
---
# <a name="sessionfeaturecurrentstate-property"></a><span data-ttu-id="ed4cb-104">Propiedad Session. FeatureCurrentState</span><span class="sxs-lookup"><span data-stu-id="ed4cb-104">Session.FeatureCurrentState property</span></span>

<span data-ttu-id="ed4cb-105">La propiedad **FeatureCurrentState** del objeto de [**sesión**](session-object.md) es una propiedad de solo lectura que devuelve el estado instalado actual de la característica designada.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-105">The **FeatureCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated feature.</span></span> <span data-ttu-id="ed4cb-106">Para los valores de estado, consulte la propiedad [**FeatureRequestState**](session-featurerequeststate.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4cb-106">For state values, see the [**FeatureRequestState**](session-featurerequeststate.md) property.</span></span>

<span data-ttu-id="ed4cb-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed4cb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed4cb-108">Syntax</span></span>


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a><span data-ttu-id="ed4cb-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ed4cb-109">Property value</span></span>

<span data-ttu-id="ed4cb-110">Nombre de cadena requerido de la característica solicitada y una clave principal en la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ed4cb-110">Required string name of the requested feature, and a primary key into the [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed4cb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed4cb-111">Remarks</span></span>

<span data-ttu-id="ed4cb-112">Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4cb-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed4cb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed4cb-113">Requirements</span></span>



| <span data-ttu-id="ed4cb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed4cb-114">Requirement</span></span> | <span data-ttu-id="ed4cb-115">Value</span><span class="sxs-lookup"><span data-stu-id="ed4cb-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4cb-116">Versión</span><span class="sxs-lookup"><span data-stu-id="ed4cb-116">Version</span></span><br/> | <span data-ttu-id="ed4cb-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ed4cb-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ed4cb-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="ed4cb-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ed4cb-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed4cb-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="ed4cb-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed4cb-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ed4cb-122">IID</span><span class="sxs-lookup"><span data-stu-id="ed4cb-122">IID</span></span><br/>     | <span data-ttu-id="ed4cb-123">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ed4cb-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="ed4cb-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed4cb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4cb-125">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="ed4cb-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="ed4cb-126">**Propiedad FeatureRequestState**</span><span class="sxs-lookup"><span data-stu-id="ed4cb-126">**FeatureRequestState property**</span></span>](session-featurerequeststate.md)
</dt> </dl>

 

 




