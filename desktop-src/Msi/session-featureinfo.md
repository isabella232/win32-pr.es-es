---
description: El método FeatureInfo del objeto de sesión devuelve un objeto FeatureInfo que contiene información descriptiva de la característica especificada.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Método Session. FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6cb2acd17dd7d07024e0b490beb6d13ad2bafd6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653827"
---
# <a name="sessionfeatureinfo-method"></a><span data-ttu-id="d7119-103">Método Session. FeatureInfo</span><span class="sxs-lookup"><span data-stu-id="d7119-103">Session.FeatureInfo method</span></span>

<span data-ttu-id="d7119-104">El método **FeatureInfo** del objeto de [**sesión**](session-object.md) devuelve un objeto **FeatureInfo** que contiene información descriptiva de la característica especificada.</span><span class="sxs-lookup"><span data-stu-id="d7119-104">The **FeatureInfo** method of the [**Session**](session-object.md) object returns a **FeatureInfo** object containing descriptive information for the specified feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7119-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7119-105">Syntax</span></span>


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="d7119-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7119-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7119-107">*Característica*</span><span class="sxs-lookup"><span data-stu-id="d7119-107">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="d7119-108">Identifica la característica de interés.</span><span class="sxs-lookup"><span data-stu-id="d7119-108">Identifies the feature of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7119-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7119-109">Return value</span></span>

<span data-ttu-id="d7119-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d7119-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7119-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7119-111">Requirements</span></span>



| <span data-ttu-id="d7119-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7119-112">Requirement</span></span> | <span data-ttu-id="d7119-113">Value</span><span class="sxs-lookup"><span data-stu-id="d7119-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7119-114">Versión</span><span class="sxs-lookup"><span data-stu-id="d7119-114">Version</span></span><br/> | <span data-ttu-id="d7119-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d7119-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d7119-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d7119-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d7119-117">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7119-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d7119-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7119-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="d7119-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7119-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d7119-120">IID</span><span class="sxs-lookup"><span data-stu-id="d7119-120">IID</span></span><br/>     | <span data-ttu-id="d7119-121">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d7119-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="d7119-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7119-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7119-123">**MsiGetFeatureInfo**</span><span class="sxs-lookup"><span data-stu-id="d7119-123">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




