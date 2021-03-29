---
description: Crea y obtiene acceso a las propiedades compartidas de un grupo de propiedades compartidas.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: Clase SharedPropertyGroup (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807279"
---
# <a name="sharedpropertygroup-class"></a><span data-ttu-id="2dbac-103">Clase SharedPropertyGroup</span><span class="sxs-lookup"><span data-stu-id="2dbac-103">SharedPropertyGroup class</span></span>

<span data-ttu-id="2dbac-104">Crea y obtiene acceso a las propiedades compartidas de un grupo de propiedades compartidas.</span><span class="sxs-lookup"><span data-stu-id="2dbac-104">Creates and accesses the shared properties in a shared property group.</span></span>

<span data-ttu-id="2dbac-105">Para obtener más información acerca del uso del Administrador de propiedades compartido en COM+, consulte [Administrador de propiedades compartido de com+](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="2dbac-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="2dbac-106">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="2dbac-106">When to implement</span></span>

<span data-ttu-id="2dbac-107">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="2dbac-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="2dbac-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dbac-108">Requirement</span></span> | <span data-ttu-id="2dbac-109">Value</span><span class="sxs-lookup"><span data-stu-id="2dbac-109">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="2dbac-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2dbac-110">Interfaces</span></span> | [<span data-ttu-id="2dbac-111">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="2dbac-111">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a><span data-ttu-id="2dbac-112">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="2dbac-112">When to use</span></span>

<span data-ttu-id="2dbac-113">Utilice esta clase para tener acceso a los métodos de [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span><span class="sxs-lookup"><span data-stu-id="2dbac-113">Use this class to access the methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

## <a name="remarks"></a><span data-ttu-id="2dbac-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dbac-114">Remarks</span></span>

<span data-ttu-id="2dbac-115">Puede crear un objeto **SharedPropertyGroup** mediante el método [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) de [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span><span class="sxs-lookup"><span data-stu-id="2dbac-115">You can create a **SharedPropertyGroup** object using the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

<span data-ttu-id="2dbac-116">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="2dbac-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="2dbac-117">Un objeto SharedPropertyGroup se crea llamando al método [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) del objeto [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="2dbac-117">A SharedPropertyGroup object is created by calling the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dbac-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dbac-118">Requirements</span></span>



| <span data-ttu-id="2dbac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dbac-119">Requirement</span></span> | <span data-ttu-id="2dbac-120">Value</span><span class="sxs-lookup"><span data-stu-id="2dbac-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2dbac-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dbac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2dbac-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2dbac-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2dbac-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dbac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2dbac-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2dbac-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2dbac-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dbac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dbac-126"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dbac-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dbac-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dbac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dbac-128">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="2dbac-128">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[<span data-ttu-id="2dbac-129">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="2dbac-129">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="2dbac-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="2dbac-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




