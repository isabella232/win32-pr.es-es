---
description: La propiedad IsEnabled de un objeto SWbemPrivilege es un valor booleano que se usa para habilitar o deshabilitar este privilegio. Para obtener más información sobre las consecuencias de habilitar privilegios específicos, vea ejecutar con privilegios especiales.
ms.assetid: 282c8865-ba0d-4e82-be05-96a940036590
ms.tgt_platform: multiple
title: Propiedad SWbemPrivilege. IsEnabled (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.IsEnabled
- ISWbemPrivilege.IsEnabled
- ISWbemPrivilege.get_IsEnabled
- ISWbemPrivilege.put_IsEnabled
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ec27b2344c42dca56ac629144f6edc402f81ea4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706038"
---
# <a name="swbemprivilegeisenabled-property"></a><span data-ttu-id="de66f-104">Propiedad SWbemPrivilege. IsEnabled</span><span class="sxs-lookup"><span data-stu-id="de66f-104">SWbemPrivilege.IsEnabled property</span></span>

<span data-ttu-id="de66f-105">La propiedad **IsEnabled** de un objeto [**SWbemPrivilege**](swbemprivilege.md) es un valor booleano que se usa para habilitar o deshabilitar este privilegio.</span><span class="sxs-lookup"><span data-stu-id="de66f-105">The **IsEnabled** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a Boolean value that you use to enable or disable this privilege.</span></span> <span data-ttu-id="de66f-106">Para obtener más información sobre las consecuencias de habilitar privilegios específicos, vea [**ejecutar con privilegios especiales**](swbemsecurity-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="de66f-106">For more information about the consequences of enabling specific privileges, see [**Running with Special Privileges**](swbemsecurity-privileges.md).</span></span>

<span data-ttu-id="de66f-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="de66f-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="de66f-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="de66f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="de66f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de66f-109">Syntax</span></span>


```VB
SWbemPrivilege.IsEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="de66f-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="de66f-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="de66f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de66f-111">Requirements</span></span>



| <span data-ttu-id="de66f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="de66f-112">Requirement</span></span> | <span data-ttu-id="de66f-113">Value</span><span class="sxs-lookup"><span data-stu-id="de66f-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de66f-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de66f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="de66f-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de66f-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de66f-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de66f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="de66f-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de66f-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de66f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de66f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="de66f-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de66f-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="de66f-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="de66f-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="de66f-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="de66f-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="de66f-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de66f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de66f-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de66f-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="de66f-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="de66f-124">CLSID</span></span><br/>                    | <span data-ttu-id="de66f-125">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="de66f-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="de66f-126">IID</span><span class="sxs-lookup"><span data-stu-id="de66f-126">IID</span></span><br/>                      | <span data-ttu-id="de66f-127">\_ISWBEMPRIVILEGE IID</span><span class="sxs-lookup"><span data-stu-id="de66f-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




