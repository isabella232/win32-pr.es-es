---
description: La propiedad ComponentRequestState del objeto de sesión obtiene o solicita un cambio en el estado de acción de una fila de la tabla de componentes.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Propiedad Session. ComponentRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680411"
---
# <a name="sessioncomponentrequeststate-property"></a><span data-ttu-id="db7cb-103">Propiedad Session. ComponentRequestState</span><span class="sxs-lookup"><span data-stu-id="db7cb-103">Session.ComponentRequestState property</span></span>

<span data-ttu-id="db7cb-104">La propiedad **ComponentRequestState** del objeto de [**sesión**](session-object.md) obtiene o solicita un cambio en el estado de acción de una fila de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="db7cb-104">The **ComponentRequestState** property of the [**Session**](session-object.md) object obtains or requests a change in the Action state of a row in the [Component table](component-table.md).</span></span>

<span data-ttu-id="db7cb-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="db7cb-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7cb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db7cb-106">Syntax</span></span>


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a><span data-ttu-id="db7cb-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="db7cb-107">Property value</span></span>

<span data-ttu-id="db7cb-108">Nombre de cadena necesario del elemento de componente, clave principal de la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="db7cb-108">Required string name of the component item, primary key of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="db7cb-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db7cb-109">Remarks</span></span>



| <span data-ttu-id="db7cb-110">Estado de selección</span><span class="sxs-lookup"><span data-stu-id="db7cb-110">Selection state</span></span>        | <span data-ttu-id="db7cb-111">Value</span><span class="sxs-lookup"><span data-stu-id="db7cb-111">Value</span></span> | <span data-ttu-id="db7cb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="db7cb-112">Description</span></span>                                                    |
|------------------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="db7cb-113">Null</span><span class="sxs-lookup"><span data-stu-id="db7cb-113">Null</span></span>                   | <span data-ttu-id="db7cb-114">Null</span><span class="sxs-lookup"><span data-stu-id="db7cb-114">Null</span></span>  | <span data-ttu-id="db7cb-115">Solicita que no se realice ninguna acción para este elemento.</span><span class="sxs-lookup"><span data-stu-id="db7cb-115">Requests that no action be taken for this item.</span></span>                |
| <span data-ttu-id="db7cb-116">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="db7cb-116">msiInstallStateAbsent</span></span>  | <span data-ttu-id="db7cb-117">2</span><span class="sxs-lookup"><span data-stu-id="db7cb-117">2</span></span>     | <span data-ttu-id="db7cb-118">Se va a quitar el elemento.</span><span class="sxs-lookup"><span data-stu-id="db7cb-118">Item is to be removed.</span></span>                                         |
| <span data-ttu-id="db7cb-119">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="db7cb-119">msiInstallStateLocal</span></span>   | <span data-ttu-id="db7cb-120">3</span><span class="sxs-lookup"><span data-stu-id="db7cb-120">3</span></span>     | <span data-ttu-id="db7cb-121">El elemento se instalará localmente.</span><span class="sxs-lookup"><span data-stu-id="db7cb-121">Item is to be installed locally.</span></span>                               |
| <span data-ttu-id="db7cb-122">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="db7cb-122">msiInstallStateSource</span></span>  | <span data-ttu-id="db7cb-123">4</span><span class="sxs-lookup"><span data-stu-id="db7cb-123">4</span></span>     | <span data-ttu-id="db7cb-124">El elemento debe instalarse y ejecutarse desde el medio de origen.</span><span class="sxs-lookup"><span data-stu-id="db7cb-124">Item is to be installed and run from the source media.</span></span>         |
| <span data-ttu-id="db7cb-125">msiInstallStateDefault</span><span class="sxs-lookup"><span data-stu-id="db7cb-125">msiInstallStateDefault</span></span> | <span data-ttu-id="db7cb-126">5</span><span class="sxs-lookup"><span data-stu-id="db7cb-126">5</span></span>     | <span data-ttu-id="db7cb-127">Si está instalado, el elemento se debe volver a instalar en el mismo estado.</span><span class="sxs-lookup"><span data-stu-id="db7cb-127">If installed, the item is to be reinstalled in the same state.</span></span> |



 

<span data-ttu-id="db7cb-128">Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="db7cb-128">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="db7cb-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db7cb-129">Requirements</span></span>



| <span data-ttu-id="db7cb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="db7cb-130">Requirement</span></span> | <span data-ttu-id="db7cb-131">Value</span><span class="sxs-lookup"><span data-stu-id="db7cb-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db7cb-132">Versión</span><span class="sxs-lookup"><span data-stu-id="db7cb-132">Version</span></span><br/> | <span data-ttu-id="db7cb-133">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="db7cb-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="db7cb-134">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="db7cb-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="db7cb-135">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="db7cb-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="db7cb-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="db7cb-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="db7cb-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db7cb-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="db7cb-138">IID</span><span class="sxs-lookup"><span data-stu-id="db7cb-138">IID</span></span><br/>     | <span data-ttu-id="db7cb-139">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="db7cb-139">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




