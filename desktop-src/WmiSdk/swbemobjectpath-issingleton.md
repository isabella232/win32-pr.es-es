---
description: La propiedad IsSingleton del objeto SWbemObjectPath es un valor booleano que indica si esta ruta de acceso representa una instancia singleton. Una instancia singleton es una instancia de una clase que nunca puede tener más de una instancia. Esta propiedad es de solo lectura.
ms.assetid: 0d0533be-89fe-4ab6-bafa-2da6195ff02c
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath. IsSingleton (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.IsSingleton
- ISWbemObjectPath.IsSingleton
- ISWbemObjectPath.get_IsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bd267c3d8ad36459a04b835cb2f130c3e98420a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279104"
---
# <a name="swbemobjectpathissingleton-property"></a><span data-ttu-id="7b23b-105">Propiedad SWbemObjectPath. IsSingleton</span><span class="sxs-lookup"><span data-stu-id="7b23b-105">SWbemObjectPath.IsSingleton property</span></span>

<span data-ttu-id="7b23b-106">La propiedad **IsSingleton** del objeto [**SWbemObjectPath**](swbemobjectpath.md) es un valor booleano que indica si esta ruta de acceso representa una instancia singleton.</span><span class="sxs-lookup"><span data-stu-id="7b23b-106">The **IsSingleton** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is a Boolean value that indicates if this path represents a singleton instance.</span></span> <span data-ttu-id="7b23b-107">Una instancia singleton es una instancia de una clase que nunca puede tener más de una instancia.</span><span class="sxs-lookup"><span data-stu-id="7b23b-107">A singleton instance is an instance of a class that can never have more than one instance.</span></span> <span data-ttu-id="7b23b-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7b23b-108">This property is read-only.</span></span>

<span data-ttu-id="7b23b-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7b23b-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="7b23b-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7b23b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b23b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b23b-111">Syntax</span></span>


```VB
SWbemObjectPath.IsSingleton As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7b23b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7b23b-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="7b23b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b23b-113">Requirements</span></span>



| <span data-ttu-id="7b23b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b23b-114">Requirement</span></span> | <span data-ttu-id="7b23b-115">Value</span><span class="sxs-lookup"><span data-stu-id="7b23b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b23b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b23b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7b23b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b23b-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b23b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b23b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7b23b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b23b-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b23b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b23b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b23b-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b23b-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b23b-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7b23b-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="7b23b-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7b23b-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7b23b-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b23b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b23b-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b23b-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7b23b-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="7b23b-126">CLSID</span></span><br/>                    | <span data-ttu-id="7b23b-127">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="7b23b-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="7b23b-128">IID</span><span class="sxs-lookup"><span data-stu-id="7b23b-128">IID</span></span><br/>                      | <span data-ttu-id="7b23b-129">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="7b23b-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




