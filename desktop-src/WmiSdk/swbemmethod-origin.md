---
description: La propiedad Origin del objeto SWbemMethod devuelve el nombre de la clase en la que se presentó este método.
ms.assetid: da98393b-af95-47ad-b589-663063f65afb
ms.tgt_platform: multiple
title: Propiedad SWbemMethod. Origin (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.Origin
- ISWbemMethod.Origin
- ISWbemMethod.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1b903a2c55bbd571a9cd1f36a51812a70c123cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276129"
---
# <a name="swbemmethodorigin-property"></a><span data-ttu-id="75526-103">Propiedad SWbemMethod. Origin</span><span class="sxs-lookup"><span data-stu-id="75526-103">SWbemMethod.Origin property</span></span>

<span data-ttu-id="75526-104">La propiedad **Origin** del objeto [**SWbemMethod**](swbemmethod.md) devuelve el nombre de la clase en la que se presentó este método.</span><span class="sxs-lookup"><span data-stu-id="75526-104">The **Origin** property of the [**SWbemMethod**](swbemmethod.md) object returns the name of the class in which this method was introduced.</span></span> <span data-ttu-id="75526-105">En el caso de las clases con jerarquías de herencia profunda, a menudo es conveniente saber qué métodos se han declarado en cada clase.</span><span class="sxs-lookup"><span data-stu-id="75526-105">For classes with deep inheritance hierarchies, it is often desirable to know which methods were declared in which classes.</span></span> <span data-ttu-id="75526-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75526-106">This property is read-only.</span></span>

<span data-ttu-id="75526-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="75526-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="75526-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75526-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="75526-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75526-109">Syntax</span></span>


```VB
SWbemMethod.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="75526-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="75526-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="75526-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75526-111">Requirements</span></span>



| <span data-ttu-id="75526-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="75526-112">Requirement</span></span> | <span data-ttu-id="75526-113">Value</span><span class="sxs-lookup"><span data-stu-id="75526-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75526-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75526-114">Minimum supported client</span></span><br/> | <span data-ttu-id="75526-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75526-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75526-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75526-116">Minimum supported server</span></span><br/> | <span data-ttu-id="75526-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75526-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75526-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75526-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="75526-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="75526-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="75526-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="75526-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="75526-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="75526-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="75526-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75526-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75526-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75526-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="75526-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="75526-124">CLSID</span></span><br/>                    | <span data-ttu-id="75526-125">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="75526-125">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="75526-126">IID</span><span class="sxs-lookup"><span data-stu-id="75526-126">IID</span></span><br/>                      | <span data-ttu-id="75526-127">\_ISWBEMMETHOD IID</span><span class="sxs-lookup"><span data-stu-id="75526-127">IID\_ISWbemMethod</span></span><br/>                                                            |



 

 




