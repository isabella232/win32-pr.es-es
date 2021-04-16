---
description: La propiedad DisplayName de un objeto SWbemPrivilege es una cadena que muestra una descripción de un objeto SWbemPrivilege.
ms.assetid: 9ed91a6a-e513-4a72-b8a9-3180e42b811f
ms.tgt_platform: multiple
title: Propiedad SWbemPrivilege. DisplayName (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.DisplayName
- ISWbemPrivilege.DisplayName
- ISWbemPrivilege.get_DisplayName
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bb45bdce52b1930f1893f7716d573033627e0cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706041"
---
# <a name="swbemprivilegedisplayname-property"></a><span data-ttu-id="93f69-103">Propiedad SWbemPrivilege. DisplayName</span><span class="sxs-lookup"><span data-stu-id="93f69-103">SWbemPrivilege.DisplayName property</span></span>

<span data-ttu-id="93f69-104">La propiedad **displayName** de un objeto [**SWbemPrivilege**](swbemprivilege.md) es una cadena que muestra una descripción de un objeto **SWbemPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="93f69-104">The **DisplayName** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that displays a description of an **SWbemPrivilege** object.</span></span> <span data-ttu-id="93f69-105">Por ejemplo, el privilegio que controla si un usuario puede ejecutar el método Shutdown de un objeto tiene la cadena "apagar el sistema" en la propiedad **SWbemPrivilege. DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="93f69-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "Shut down the system" string in the **SWbemPrivilege.DisplayName** property.</span></span> <span data-ttu-id="93f69-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="93f69-106">This property is read-only.</span></span>

<span data-ttu-id="93f69-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="93f69-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="93f69-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="93f69-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f69-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93f69-109">Syntax</span></span>


```VB
SWbemPrivilege.DisplayName As 
```



## <a name="property-value"></a><span data-ttu-id="93f69-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="93f69-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="93f69-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93f69-111">Requirements</span></span>



| <span data-ttu-id="93f69-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="93f69-112">Requirement</span></span> | <span data-ttu-id="93f69-113">Value</span><span class="sxs-lookup"><span data-stu-id="93f69-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93f69-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93f69-114">Minimum supported client</span></span><br/> | <span data-ttu-id="93f69-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93f69-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93f69-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93f69-116">Minimum supported server</span></span><br/> | <span data-ttu-id="93f69-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93f69-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93f69-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93f69-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="93f69-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="93f69-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="93f69-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="93f69-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="93f69-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="93f69-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="93f69-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93f69-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93f69-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93f69-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="93f69-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="93f69-124">CLSID</span></span><br/>                    | <span data-ttu-id="93f69-125">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="93f69-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="93f69-126">IID</span><span class="sxs-lookup"><span data-stu-id="93f69-126">IID</span></span><br/>                      | <span data-ttu-id="93f69-127">\_ISWBEMPRIVILEGE IID</span><span class="sxs-lookup"><span data-stu-id="93f69-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




