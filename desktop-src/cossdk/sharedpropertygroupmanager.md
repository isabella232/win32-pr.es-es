---
description: Crea grupos de propiedades compartidas y para obtener acceso a grupos de propiedades compartidas existentes.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: SharedPropertyGroupManager (clase) (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907154"
---
# <a name="sharedpropertygroupmanager-class"></a><span data-ttu-id="5b679-103">SharedPropertyGroupManager (clase)</span><span class="sxs-lookup"><span data-stu-id="5b679-103">SharedPropertyGroupManager class</span></span>

<span data-ttu-id="5b679-104">Crea grupos de propiedades compartidas y para obtener acceso a grupos de propiedades compartidas existentes.</span><span class="sxs-lookup"><span data-stu-id="5b679-104">Creates shared property groups and to obtain access to existing shared property groups.</span></span>

<span data-ttu-id="5b679-105">Para obtener más información acerca del uso del Administrador de propiedades compartido en COM+, consulte [Administrador de propiedades compartido de com+](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="5b679-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="5b679-106">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="5b679-106">When to implement</span></span>

<span data-ttu-id="5b679-107">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="5b679-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="5b679-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b679-108">Requirement</span></span> | <span data-ttu-id="5b679-109">Value</span><span class="sxs-lookup"><span data-stu-id="5b679-109">Value</span></span> |
|------------|--------------------------------------------------------------------|
| <span data-ttu-id="5b679-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="5b679-110">CLSID</span></span>      | <span data-ttu-id="5b679-111">CLSID \_ SharedPropertyGroupManager</span><span class="sxs-lookup"><span data-stu-id="5b679-111">CLSID\_SharedPropertyGroupManager</span></span>                                  |
| <span data-ttu-id="5b679-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="5b679-112">ProgID</span></span>     | <span data-ttu-id="5b679-113">L "MTxSpm. SharedPropertyGroupManager"</span><span class="sxs-lookup"><span data-stu-id="5b679-113">L"MTxSpm.SharedPropertyGroupManager"</span></span>                               |
| <span data-ttu-id="5b679-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="5b679-114">Interfaces</span></span> | [<span data-ttu-id="5b679-115">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="5b679-115">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a><span data-ttu-id="5b679-116">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="5b679-116">When to use</span></span>

<span data-ttu-id="5b679-117">Utilice esta clase para tener acceso a los métodos de [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span><span class="sxs-lookup"><span data-stu-id="5b679-117">Use this class to access the methods of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

## <a name="remarks"></a><span data-ttu-id="5b679-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b679-118">Remarks</span></span>

<span data-ttu-id="5b679-119">Para crear este objeto, llame a [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="5b679-119">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="5b679-120">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="5b679-120">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="5b679-121">Un objeto SharedPropertyGroupManager se puede declarar con "COMSVCSLib. SharedPropertyGroupManager" como nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="5b679-121">A SharedPropertyGroupManager object can be declared using "COMSVCSLib.SharedPropertyGroupManager" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b679-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b679-122">Requirements</span></span>



| <span data-ttu-id="5b679-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b679-123">Requirement</span></span> | <span data-ttu-id="5b679-124">Value</span><span class="sxs-lookup"><span data-stu-id="5b679-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b679-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b679-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5b679-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5b679-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5b679-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b679-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5b679-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b679-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5b679-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b679-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b679-130"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b679-130"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b679-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b679-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b679-132">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="5b679-132">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[<span data-ttu-id="5b679-133">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="5b679-133">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="5b679-134">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="5b679-134">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> </dl>

 

 




