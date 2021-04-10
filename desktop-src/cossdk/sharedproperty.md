---
description: Establece o recupera el valor de una propiedad compartida.
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: Clase SharedProperty (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: a7a7857ad280ad722601bdced6c25d04b03dc0b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153022"
---
# <a name="sharedproperty-class"></a><span data-ttu-id="94801-103">Clase SharedProperty</span><span class="sxs-lookup"><span data-stu-id="94801-103">SharedProperty class</span></span>

<span data-ttu-id="94801-104">Establece o recupera el valor de una propiedad compartida.</span><span class="sxs-lookup"><span data-stu-id="94801-104">Sets or retrieves the value of a shared property.</span></span>

<span data-ttu-id="94801-105">Para obtener información general sobre el uso del Administrador de propiedades compartido en COM+, consulte [Administrador de propiedades compartido de com+](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="94801-105">For general information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="94801-106">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="94801-106">When to implement</span></span>

<span data-ttu-id="94801-107">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="94801-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="94801-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="94801-108">Requirement</span></span> | <span data-ttu-id="94801-109">Value</span><span class="sxs-lookup"><span data-stu-id="94801-109">Value</span></span> |
|------------|--------------------------------------------|
| <span data-ttu-id="94801-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="94801-110">Interfaces</span></span> | [<span data-ttu-id="94801-111">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="94801-111">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a><span data-ttu-id="94801-112">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="94801-112">When to use</span></span>

<span data-ttu-id="94801-113">Utilice esta clase para tener acceso a los métodos de [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span><span class="sxs-lookup"><span data-stu-id="94801-113">Use this class to access the methods of [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span></span>

## <a name="remarks"></a><span data-ttu-id="94801-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94801-114">Remarks</span></span>

<span data-ttu-id="94801-115">Puede crear un objeto **SharedProperty** mediante los métodos [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) o [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) de [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span><span class="sxs-lookup"><span data-stu-id="94801-115">You can create a **SharedProperty** object by using the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

<span data-ttu-id="94801-116">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="94801-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="94801-117">Un objeto SharedProperty se crea llamando a los métodos [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) o [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) del objeto [**SharedPropertyGroup**](sharedpropertygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="94801-117">A SharedProperty object is created by calling the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of the [**SharedPropertyGroup**](sharedpropertygroup.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="94801-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94801-118">Requirements</span></span>



| <span data-ttu-id="94801-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="94801-119">Requirement</span></span> | <span data-ttu-id="94801-120">Value</span><span class="sxs-lookup"><span data-stu-id="94801-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="94801-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94801-121">Minimum supported client</span></span><br/> | <span data-ttu-id="94801-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="94801-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="94801-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94801-123">Minimum supported server</span></span><br/> | <span data-ttu-id="94801-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="94801-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="94801-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94801-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="94801-126"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="94801-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94801-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="94801-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94801-128">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="94801-128">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[<span data-ttu-id="94801-129">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="94801-129">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> <dt>

[<span data-ttu-id="94801-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="94801-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




