---
description: La propiedad FeatureCost del objeto de sesión devuelve la cantidad total de espacio en disco (en unidades de 512 bytes) que requiere la característica especificada y sus características principales (hasta la raíz de la tabla de características).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Propiedad Session. FeatureCost
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653703"
---
# <a name="sessionfeaturecost-property"></a><span data-ttu-id="0d251-103">Propiedad Session. FeatureCost</span><span class="sxs-lookup"><span data-stu-id="0d251-103">Session.FeatureCost property</span></span>

<span data-ttu-id="0d251-104">La propiedad **FeatureCost** del objeto de [**sesión**](session-object.md) devuelve la cantidad total de espacio en disco (en unidades de 512 bytes) que requiere la característica especificada y sus características principales (hasta la raíz de la tabla de características).</span><span class="sxs-lookup"><span data-stu-id="0d251-104">The **FeatureCost** property of the [**Session**](session-object.md) object returns the total amount of disk space (in units of 512 bytes) required by the specified feature and its parent features (up to the root of the Feature table).</span></span> <span data-ttu-id="0d251-105">Para cada característica, el costo total se compone de los costos de disco atribuidos a cada componente vinculado a la característica.</span><span class="sxs-lookup"><span data-stu-id="0d251-105">For each feature, the total cost is made up of the disk costs attributed to every component linked to the feature.</span></span>

<span data-ttu-id="0d251-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0d251-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d251-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d251-107">Syntax</span></span>


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a><span data-ttu-id="0d251-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0d251-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0d251-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d251-109">Remarks</span></span>

<span data-ttu-id="0d251-110">Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="0d251-110">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d251-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d251-111">Requirements</span></span>



| <span data-ttu-id="0d251-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d251-112">Requirement</span></span> | <span data-ttu-id="0d251-113">Value</span><span class="sxs-lookup"><span data-stu-id="0d251-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d251-114">Versión</span><span class="sxs-lookup"><span data-stu-id="0d251-114">Version</span></span><br/> | <span data-ttu-id="0d251-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d251-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0d251-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d251-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0d251-117">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d251-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0d251-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d251-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d251-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d251-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0d251-120">IID</span><span class="sxs-lookup"><span data-stu-id="0d251-120">IID</span></span><br/>     | <span data-ttu-id="0d251-121">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0d251-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




