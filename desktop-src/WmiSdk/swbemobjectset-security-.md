---
description: La \_ propiedad Security del objeto SWbemObjectSet se usa para obtener o establecer la configuración de seguridad de un objeto SWbemObjectSet. Esta propiedad es un objeto SWbemSecurity.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: Propiedad SWbemObjectSet.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706039"
---
# <a name="swbemobjectsetsecurity_-property"></a><span data-ttu-id="73e08-104">Propiedad SWbemObjectSet. Security \_</span><span class="sxs-lookup"><span data-stu-id="73e08-104">SWbemObjectSet.Security\_ property</span></span>

<span data-ttu-id="73e08-105">La **propiedad \_ Security** del objeto [**SWbemObjectSet**](swbemobjectset.md) se usa para obtener o establecer la configuración de seguridad de un objeto **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="73e08-105">The **Security\_** property of the [**SWbemObjectSet**](swbemobjectset.md) object is used to get or set the security settings for an **SWbemObjectSet** object.</span></span> <span data-ttu-id="73e08-106">Esta propiedad es un objeto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="73e08-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="73e08-107">Al establecer la propiedad [**\_ Security**](swbemobject-security-.md) de un objeto [**SWbemObjectSet**](swbemobjectset.md) en **null** , se concede acceso ilimitado a todos los usuarios en todo momento.</span><span class="sxs-lookup"><span data-stu-id="73e08-107">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectSet**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="73e08-108">Para obtener más información sobre las implicaciones de acceso ilimitado, vea [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="73e08-108">For more information about the implications of unlimited access, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="73e08-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="73e08-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="73e08-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73e08-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e08-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73e08-111">Syntax</span></span>


```VB
SWbemObjectSet.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="73e08-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="73e08-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="73e08-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73e08-113">Requirements</span></span>



| <span data-ttu-id="73e08-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="73e08-114">Requirement</span></span> | <span data-ttu-id="73e08-115">Value</span><span class="sxs-lookup"><span data-stu-id="73e08-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73e08-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73e08-116">Minimum supported client</span></span><br/> | <span data-ttu-id="73e08-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73e08-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73e08-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73e08-118">Minimum supported server</span></span><br/> | <span data-ttu-id="73e08-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73e08-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73e08-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73e08-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="73e08-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="73e08-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="73e08-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="73e08-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="73e08-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="73e08-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="73e08-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73e08-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73e08-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73e08-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="73e08-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="73e08-126">CLSID</span></span><br/>                    | <span data-ttu-id="73e08-127">CLSID \_ SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="73e08-127">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="73e08-128">IID</span><span class="sxs-lookup"><span data-stu-id="73e08-128">IID</span></span><br/>                      | <span data-ttu-id="73e08-129">\_ISWBEMOBJECTSET IID</span><span class="sxs-lookup"><span data-stu-id="73e08-129">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="73e08-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="73e08-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e08-131">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="73e08-131">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="73e08-132">Crear una aplicación o un script WMI</span><span class="sxs-lookup"><span data-stu-id="73e08-132">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="73e08-133">Protección de los clientes de scripting</span><span class="sxs-lookup"><span data-stu-id="73e08-133">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

 




