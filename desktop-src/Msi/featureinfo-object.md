---
description: El objeto FeatureInfo contiene información sobre la característica de destino y se crea a partir del objeto de sesión mediante el método FeatureInfo.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: Objeto FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670350"
---
# <a name="featureinfo-object"></a><span data-ttu-id="ab734-103">Objeto FeatureInfo</span><span class="sxs-lookup"><span data-stu-id="ab734-103">FeatureInfo object</span></span>

<span data-ttu-id="ab734-104">El objeto **FeatureInfo** contiene información sobre la característica de destino y se crea a partir del objeto de [**sesión**](session-object.md) mediante el método [**FeatureInfo**](session-featureinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ab734-104">The **FeatureInfo** object contains information regarding the targeted feature and is created from the [**Session**](session-object.md) object using the [**FeatureInfo**](session-featureinfo.md) Method.</span></span>

## <a name="members"></a><span data-ttu-id="ab734-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab734-105">Members</span></span>

<span data-ttu-id="ab734-106">El objeto **FeatureInfo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ab734-106">The **FeatureInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="ab734-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab734-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab734-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab734-108">Properties</span></span>

<span data-ttu-id="ab734-109">El objeto **FeatureInfo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ab734-109">The **FeatureInfo** object has these properties.</span></span>



| <span data-ttu-id="ab734-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab734-110">Property</span></span>                                                  | <span data-ttu-id="ab734-111">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="ab734-111">Access type</span></span>           | <span data-ttu-id="ab734-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab734-112">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab734-113">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="ab734-113">**Attributes**</span></span>](featureinfo-attributes.md)<br/>   | <span data-ttu-id="ab734-114">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ab734-114">Read/write</span></span><br/> | <span data-ttu-id="ab734-115">Devuelve el valor de la característica en la columna Attributes de la tabla de características.</span><span class="sxs-lookup"><span data-stu-id="ab734-115">Returns the value for the feature in the Attributes column of the Feature table.</span></span><br/> |
| [<span data-ttu-id="ab734-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab734-116">**Description**</span></span>](featureinfo-description.md)<br/> |                       | <span data-ttu-id="ab734-117">Devuelve la descripción de la característica.</span><span class="sxs-lookup"><span data-stu-id="ab734-117">Returns the description of the feature.</span></span><br/>                                          |
| [<span data-ttu-id="ab734-118">**Title**</span><span class="sxs-lookup"><span data-stu-id="ab734-118">**Title**</span></span>](featureinfo-title.md)<br/>             | <span data-ttu-id="ab734-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab734-119">Read-only</span></span><br/>  | <span data-ttu-id="ab734-120">Devuelve el título de la característica.</span><span class="sxs-lookup"><span data-stu-id="ab734-120">Returns the title of the feature.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="ab734-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab734-121">Requirements</span></span>



| <span data-ttu-id="ab734-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab734-122">Requirement</span></span> | <span data-ttu-id="ab734-123">Value</span><span class="sxs-lookup"><span data-stu-id="ab734-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab734-124">Versión</span><span class="sxs-lookup"><span data-stu-id="ab734-124">Version</span></span><br/> | <span data-ttu-id="ab734-125">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ab734-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ab734-126">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ab734-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ab734-127">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="ab734-127">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ab734-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab734-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="ab734-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab734-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ab734-130">IID</span><span class="sxs-lookup"><span data-stu-id="ab734-130">IID</span></span><br/>     | <span data-ttu-id="ab734-131">IID \_ IFeatureInfo se define como 000C109F-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ab734-131">IID\_IFeatureInfo is defined as 000C109F-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="ab734-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab734-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab734-133">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ab734-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




