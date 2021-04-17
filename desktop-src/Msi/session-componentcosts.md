---
description: La propiedad ComponentCosts del objeto de sesión devuelve un objeto RecordList que enumera el espacio en disco por unidad necesaria para instalar un componente.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Propiedad Session. ComponentCosts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679523"
---
# <a name="sessioncomponentcosts-property"></a><span data-ttu-id="c053d-103">Propiedad Session. ComponentCosts</span><span class="sxs-lookup"><span data-stu-id="c053d-103">Session.ComponentCosts property</span></span>

<span data-ttu-id="c053d-104">La propiedad ComponentCosts del objeto de [**sesión**](session-object.md) devuelve un objeto [**RecordList**](recordlist-object.md) que enumera el espacio en disco por unidad necesaria para instalar un componente.</span><span class="sxs-lookup"><span data-stu-id="c053d-104">The ComponentCosts property of the [**Session**](session-object.md) object returns a [**RecordList**](recordlist-object.md) object enumerating the disk space per drive required to install a component.</span></span> <span data-ttu-id="c053d-105">La interfaz de usuario usa esta información para mostrar el espacio en disco necesario para todas las unidades.</span><span class="sxs-lookup"><span data-stu-id="c053d-105">This information is used by the user interface to display the disk space required for all drives.</span></span> <span data-ttu-id="c053d-106">Los costos de espacio en disco devueltos son múltiplos de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="c053d-106">The returned disk space costs are in multiples of 512 bytes.</span></span>

<span data-ttu-id="c053d-107">La propiedad ComponentCosts solo debe usarse después de que el instalador haya completado el [costo de archivos](file-costing.md) y después de la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="c053d-107">The ComponentCosts property should only be used after the installer has completed [file costing](file-costing.md) and after the [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="c053d-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c053d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c053d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c053d-109">Syntax</span></span>


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a><span data-ttu-id="c053d-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c053d-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c053d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c053d-111">Remarks</span></span>

<span data-ttu-id="c053d-112">Para obtener el costo total, agregue los costos de todos los componentes más el costo del motor de instalación (componente = "").</span><span class="sxs-lookup"><span data-stu-id="c053d-112">To obtain the total cost, add the costs for all components plus the installer engine cost (Component = "").</span></span>

<span data-ttu-id="c053d-113">ComponentCosts devuelve un [**objeto RecordList**](recordlist-object.md).</span><span class="sxs-lookup"><span data-stu-id="c053d-113">ComponentCosts returns a [**RecordList object**](recordlist-object.md).</span></span> <span data-ttu-id="c053d-114">Cada registro del objeto RecordList devuelto tiene los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="c053d-114">Each record in the returned RecordList object has the following fields:</span></span>



| <span data-ttu-id="c053d-115">Campo</span><span class="sxs-lookup"><span data-stu-id="c053d-115">Field</span></span> | <span data-ttu-id="c053d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c053d-116">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="c053d-117">1</span><span class="sxs-lookup"><span data-stu-id="c053d-117">1</span></span>     | <span data-ttu-id="c053d-118">Nombre de volumen o unidad</span><span class="sxs-lookup"><span data-stu-id="c053d-118">Volume/Drive name</span></span>                                    |
| <span data-ttu-id="c053d-119">2</span><span class="sxs-lookup"><span data-stu-id="c053d-119">2</span></span>     | <span data-ttu-id="c053d-120">Costo final de espacio en disco en múltiplos de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="c053d-120">Final disk space cost in multiples of 512 bytes.</span></span>     |
| <span data-ttu-id="c053d-121">3</span><span class="sxs-lookup"><span data-stu-id="c053d-121">3</span></span>     | <span data-ttu-id="c053d-122">Costo de espacio en disco temporal en múltiplos de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="c053d-122">Temporary disk space cost in multiples of 512 bytes.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c053d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c053d-123">Requirements</span></span>



| <span data-ttu-id="c053d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c053d-124">Requirement</span></span> | <span data-ttu-id="c053d-125">Value</span><span class="sxs-lookup"><span data-stu-id="c053d-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c053d-126">Versión</span><span class="sxs-lookup"><span data-stu-id="c053d-126">Version</span></span><br/> | <span data-ttu-id="c053d-127">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c053d-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c053d-128">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c053d-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c053d-129">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c053d-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c053d-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c053d-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="c053d-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c053d-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c053d-132">IID</span><span class="sxs-lookup"><span data-stu-id="c053d-132">IID</span></span><br/>     | <span data-ttu-id="c053d-133">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c053d-133">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




