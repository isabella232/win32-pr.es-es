---
description: La propiedad CIMType del objeto SWbemProperty es un entero que se puede utilizar para determinar el tipo CIM de esta propiedad. Esta propiedad es de solo lectura.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Propiedad SWbemProperty. CIMType (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002118"
---
# <a name="swbempropertycimtype-property"></a><span data-ttu-id="d2fe8-104">Propiedad SWbemProperty. CIMType</span><span class="sxs-lookup"><span data-stu-id="d2fe8-104">SWbemProperty.CIMType property</span></span>

<span data-ttu-id="d2fe8-105">La propiedad **CIMType** del objeto [**SWbemProperty**](swbemproperty.md) es un entero que se puede utilizar para determinar el tipo CIM de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d2fe8-105">The **CIMType** property of the [**SWbemProperty**](swbemproperty.md) object is an integer that can be used to determine the CIM type of this property.</span></span> <span data-ttu-id="d2fe8-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d2fe8-106">This property is read-only.</span></span>

<span data-ttu-id="d2fe8-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d2fe8-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d2fe8-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d2fe8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2fe8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2fe8-109">Syntax</span></span>


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a><span data-ttu-id="d2fe8-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d2fe8-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d2fe8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2fe8-111">Remarks</span></span>

<span data-ttu-id="d2fe8-112">Para obtener más información sobre los tipos válidos para esta propiedad, vea [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="d2fe8-112">For more information about valid types for this property, see [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>

<span data-ttu-id="d2fe8-113">Las instancias de objetos incrustados se almacenan en objetos compuestos como propiedades del tipo de **\_ objeto CIM**.</span><span class="sxs-lookup"><span data-stu-id="d2fe8-113">Instances of embedded objects are stored in composite objects as properties of type **CIM\_OBJECT**.</span></span> <span data-ttu-id="d2fe8-114">Para determinar la clase de un objeto incrustado en una instancia de una clase compuesta, debe examinar el calificador **CIMType** de la propiedad tipo de **\_ objeto CIM** .</span><span class="sxs-lookup"><span data-stu-id="d2fe8-114">To determine the class of an embedded object in an instance of a composite class, you must examine the **CIMType** qualifier of the **CIM\_OBJECT** type property.</span></span>

<span data-ttu-id="d2fe8-115">Las referencias de objeto en una clase de asociación se almacenan en las propiedades de tipo **\_ referencia CIM**.</span><span class="sxs-lookup"><span data-stu-id="d2fe8-115">The object references in an association class are stored in properties of type **CIM\_REFERENCE**.</span></span> <span data-ttu-id="d2fe8-116">Para determinar las rutas de acceso de objeto reales, debe examinar el calificador **CIMType** de la propiedad tipo de **\_ referencia CIM** .</span><span class="sxs-lookup"><span data-stu-id="d2fe8-116">To determine the actual object paths you must examine the **CIMType** qualifier of the **CIM\_REFERENCE** type property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2fe8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2fe8-117">Requirements</span></span>



| <span data-ttu-id="d2fe8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2fe8-118">Requirement</span></span> | <span data-ttu-id="d2fe8-119">Value</span><span class="sxs-lookup"><span data-stu-id="d2fe8-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2fe8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2fe8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d2fe8-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2fe8-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2fe8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2fe8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d2fe8-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2fe8-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2fe8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2fe8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2fe8-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2fe8-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2fe8-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d2fe8-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="d2fe8-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d2fe8-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d2fe8-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2fe8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2fe8-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2fe8-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d2fe8-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="d2fe8-130">CLSID</span></span><br/>                    | <span data-ttu-id="d2fe8-131">CLSID \_ SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="d2fe8-131">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="d2fe8-132">IID</span><span class="sxs-lookup"><span data-stu-id="d2fe8-132">IID</span></span><br/>                      | <span data-ttu-id="d2fe8-133">\_ISWBEMPROPERTY IID</span><span class="sxs-lookup"><span data-stu-id="d2fe8-133">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




