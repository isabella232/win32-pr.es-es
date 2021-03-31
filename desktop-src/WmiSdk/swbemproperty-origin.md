---
description: La propiedad Origin del objeto SWbemProperty recupera el nombre de la clase WMI en la que se presentó esta propiedad. En el caso de las clases con jerarquías de herencia profunda, a menudo es conveniente saber qué propiedades se han declarado en cada clase.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Propiedad SWbemProperty. Origin (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277123"
---
# <a name="swbempropertyorigin-property"></a><span data-ttu-id="52f10-104">Propiedad SWbemProperty. Origin</span><span class="sxs-lookup"><span data-stu-id="52f10-104">SWbemProperty.Origin property</span></span>

<span data-ttu-id="52f10-105">La propiedad **Origin** del objeto [**SWbemProperty**](swbemproperty.md) recupera el nombre de la clase WMI en la que se presentó esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="52f10-105">The **Origin** property of the [**SWbemProperty**](swbemproperty.md) object retrieves the name of the WMI class in which this property was introduced.</span></span> <span data-ttu-id="52f10-106">En el caso de las clases con jerarquías de herencia profunda, a menudo es conveniente saber qué propiedades se han declarado en cada clase.</span><span class="sxs-lookup"><span data-stu-id="52f10-106">For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes.</span></span>

<span data-ttu-id="52f10-107">Si la propiedad es local (vea [**SWbemQualifier. IsLocal**](swbemqualifier-islocal.md)), este valor es el mismo que el de la clase propietaria.</span><span class="sxs-lookup"><span data-stu-id="52f10-107">If the property is local (see [**SWbemQualifier.IsLocal**](swbemqualifier-islocal.md)), this value is the same as the owning class.</span></span> <span data-ttu-id="52f10-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="52f10-108">This property is read-only.</span></span>

<span data-ttu-id="52f10-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="52f10-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="52f10-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="52f10-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52f10-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52f10-111">Syntax</span></span>


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="52f10-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="52f10-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="52f10-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52f10-113">Requirements</span></span>



| <span data-ttu-id="52f10-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52f10-114">Requirement</span></span> | <span data-ttu-id="52f10-115">Value</span><span class="sxs-lookup"><span data-stu-id="52f10-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52f10-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52f10-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52f10-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52f10-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52f10-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52f10-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52f10-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52f10-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52f10-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52f10-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="52f10-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f10-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="52f10-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="52f10-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="52f10-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="52f10-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="52f10-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52f10-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52f10-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52f10-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="52f10-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="52f10-126">CLSID</span></span><br/>                    | <span data-ttu-id="52f10-127">CLSID \_ SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="52f10-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="52f10-128">IID</span><span class="sxs-lookup"><span data-stu-id="52f10-128">IID</span></span><br/>                      | <span data-ttu-id="52f10-129">\_ISWBEMPROPERTY IID</span><span class="sxs-lookup"><span data-stu-id="52f10-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




