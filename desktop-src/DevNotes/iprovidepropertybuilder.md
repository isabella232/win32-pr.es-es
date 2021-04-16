---
description: La interfaz IProvidePropertyBuilder, cuando se implementa, permite a los objetos especificar objetos generador de propiedades para las propiedades.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Interfaz IProvidePropertyBuilder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649566"
---
# <a name="iprovidepropertybuilder-interface"></a><span data-ttu-id="dabf3-103">Interfaz IProvidePropertyBuilder</span><span class="sxs-lookup"><span data-stu-id="dabf3-103">IProvidePropertyBuilder interface</span></span>

<span data-ttu-id="dabf3-104">La interfaz **IProvidePropertyBuilder** , cuando se implementa, permite a los objetos especificar objetos generador de propiedades para las propiedades.</span><span class="sxs-lookup"><span data-stu-id="dabf3-104">The **IProvidePropertyBuilder** interface, when implemented, allows objects to specify property builder objects for properties.</span></span> <span data-ttu-id="dabf3-105">Los generadores se invocan mediante un botón de puntos suspensivos ( \[ ... \] ) en el explorador de propiedades Microsoft Visual Studio y se invocan a través de [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) cuando se presiona el botón.</span><span class="sxs-lookup"><span data-stu-id="dabf3-105">Builders are invoked by an ellipsis button (\[...\]) on the Microsoft Visual Studio property browser and is invoked through [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) when the button is pressed.</span></span> <span data-ttu-id="dabf3-106">Para proporcionar un generador para una propiedad determinada, devuelva un GUID para el generador de propiedades que se debe invocar para la propiedad actual desde [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span><span class="sxs-lookup"><span data-stu-id="dabf3-106">To supply a builder for a given property, return a GUID for the property builder that should be invoked for the current property from [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span> <span data-ttu-id="dabf3-107">Los generadores generalmente se implementan a través de cuadros de diálogo modales.</span><span class="sxs-lookup"><span data-stu-id="dabf3-107">Builders are generally implemented through modal dialog boxes.</span></span>

<span data-ttu-id="dabf3-108">La versión de esta interfaz es 1,0.</span><span class="sxs-lookup"><span data-stu-id="dabf3-108">The version for this interface is 1.0.</span></span> <span data-ttu-id="dabf3-109">Las llamadas a métodos se reciben en un punto de conexión asignado dinámicamente (como se describe en la documentación binaria de MSMQ en la asignación de extremos) y usan el UUID (identificador único universal) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span><span class="sxs-lookup"><span data-stu-id="dabf3-109">Method calls are received at a dynamically assigned endpoint (as described in the MSMQ binary documentation on endpoint mapping) and use the UUID (universally unique identifier) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span></span>

## <a name="members"></a><span data-ttu-id="dabf3-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="dabf3-110">Members</span></span>

<span data-ttu-id="dabf3-111">La interfaz **IProvidePropertyBuilder: IUnknown** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dabf3-111">The **IProvidePropertyBuilder:IUnknown** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dabf3-112">**IProvidePropertyBuilder** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dabf3-112">**IProvidePropertyBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="dabf3-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="dabf3-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dabf3-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="dabf3-114">Methods</span></span>

<span data-ttu-id="dabf3-115">La interfaz **IProvidePropertyBuilder: IUnknown** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dabf3-115">The **IProvidePropertyBuilder:IUnknown** interface has these methods.</span></span>



| <span data-ttu-id="dabf3-116">Método</span><span class="sxs-lookup"><span data-stu-id="dabf3-116">Method</span></span>                                                                       | <span data-ttu-id="dabf3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="dabf3-117">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dabf3-118">**ExecuteBuilder**</span><span class="sxs-lookup"><span data-stu-id="dabf3-118">**ExecuteBuilder**</span></span>](iprovidepropertybuilder-executebuilder.md)             | <span data-ttu-id="dabf3-119">Notifica a un objeto que debe mostrar su generador para la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="dabf3-119">Notifies an object that it should display its builder for the specified property.</span></span><br/> |
| [<span data-ttu-id="dabf3-120">**MapPropertyToBuilder**</span><span class="sxs-lookup"><span data-stu-id="dabf3-120">**MapPropertyToBuilder**</span></span>](iprovidepropertybuilder-mappropertytobuilder.md) | <span data-ttu-id="dabf3-121">Comprueba si un generador se debe asociar a una propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="dabf3-121">Checks whether a builder should be associated with a particular property.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="dabf3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dabf3-122">Requirements</span></span>



| <span data-ttu-id="dabf3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dabf3-123">Requirement</span></span> | <span data-ttu-id="dabf3-124">Value</span><span class="sxs-lookup"><span data-stu-id="dabf3-124">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dabf3-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dabf3-125">DLL</span></span><br/> | <dl> <span data-ttu-id="dabf3-126"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dabf3-126"><dt>Vsp.dll</dt></span></span> </dl> |



 

 
