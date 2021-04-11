---
description: La propiedad Name de un objeto SWbemPrivilege es una cadena que describe un privilegio de forma única.
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: Propiedad SWbemPrivilege.Name (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b83ccc7c2757c5d5a0746efd4434db3d108b6992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279099"
---
# <a name="swbemprivilegename-property"></a><span data-ttu-id="5e722-103">Propiedad SWbemPrivilege.Name</span><span class="sxs-lookup"><span data-stu-id="5e722-103">SWbemPrivilege.Name property</span></span>

<span data-ttu-id="5e722-104">La propiedad **Name** de un objeto [**SWbemPrivilege**](swbemprivilege.md) es una cadena que describe un privilegio de forma única.</span><span class="sxs-lookup"><span data-stu-id="5e722-104">The **Name** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that uniquely describes a privilege.</span></span> <span data-ttu-id="5e722-105">Por ejemplo, el privilegio que controla si un usuario puede ejecutar el método Shutdown de un objeto tiene la cadena "SeShutdownPrivilege" en la propiedad **SWbemPrivilege.Name** .</span><span class="sxs-lookup"><span data-stu-id="5e722-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "SeShutdownPrivilege" string in the **SWbemPrivilege.Name** property.</span></span> <span data-ttu-id="5e722-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5e722-106">This property is read-only.</span></span>

<span data-ttu-id="5e722-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5e722-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5e722-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5e722-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e722-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e722-109">Syntax</span></span>


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a><span data-ttu-id="5e722-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5e722-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="5e722-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e722-111">Requirements</span></span>



| <span data-ttu-id="5e722-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e722-112">Requirement</span></span> | <span data-ttu-id="5e722-113">Value</span><span class="sxs-lookup"><span data-stu-id="5e722-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e722-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e722-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5e722-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e722-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e722-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e722-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5e722-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e722-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e722-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e722-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e722-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e722-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e722-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5e722-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e722-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5e722-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5e722-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e722-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e722-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e722-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5e722-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="5e722-124">CLSID</span></span><br/>                    | <span data-ttu-id="5e722-125">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="5e722-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="5e722-126">IID</span><span class="sxs-lookup"><span data-stu-id="5e722-126">IID</span></span><br/>                      | <span data-ttu-id="5e722-127">\_ISWBEMPRIVILEGE IID</span><span class="sxs-lookup"><span data-stu-id="5e722-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




