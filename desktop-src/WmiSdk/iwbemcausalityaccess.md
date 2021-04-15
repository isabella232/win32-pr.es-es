---
description: Realiza el seguimiento de las solicitudes secundarias que se generan a partir de una solicitud primaria.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Interfaz IWbemCausalityAccess (Wbemint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: db4c7a76b04b659cd467f7a4a7a9a8c1ba42721f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648547"
---
# <a name="iwbemcausalityaccess-interface"></a><span data-ttu-id="2f72f-103">Interfaz IWbemCausalityAccess</span><span class="sxs-lookup"><span data-stu-id="2f72f-103">IWbemCausalityAccess interface</span></span>

<span data-ttu-id="2f72f-104">La interfaz **IWbemCausalityAccess** realiza un seguimiento de las solicitudes secundarias que se generan a partir de una solicitud primaria.</span><span class="sxs-lookup"><span data-stu-id="2f72f-104">The **IWbemCausalityAccess** interface keeps track of child requests that are generated from a parent request.</span></span> <span data-ttu-id="2f72f-105">Puede obtener un objeto **IWbemCausalityAccess** mediante una interfaz de consulta (Qi) para [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span><span class="sxs-lookup"><span data-stu-id="2f72f-105">You can obtain an **IWbemCausalityAccess** object by using a query interface (QI) for [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span></span> <span data-ttu-id="2f72f-106">Cada solicitud se identifica mediante un identificador único global (GUID) y puede tener una solicitud primaria o puede ser una solicitud Top.</span><span class="sxs-lookup"><span data-stu-id="2f72f-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="2f72f-107">Un GUID es un número único de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="2f72f-107">A GUID is a unique 128-bit number.</span></span> <span data-ttu-id="2f72f-108">Por ejemplo, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="2f72f-108">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

## <a name="members"></a><span data-ttu-id="2f72f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2f72f-109">Members</span></span>

<span data-ttu-id="2f72f-110">La interfaz **IWbemCausalityAccess** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2f72f-110">The **IWbemCausalityAccess** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2f72f-111">**IWbemCausalityAccess** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2f72f-111">**IWbemCausalityAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="2f72f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2f72f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2f72f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2f72f-113">Methods</span></span>

<span data-ttu-id="2f72f-114">La interfaz **IWbemCausalityAccess** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2f72f-114">The **IWbemCausalityAccess** interface has these methods.</span></span>



| <span data-ttu-id="2f72f-115">Método</span><span class="sxs-lookup"><span data-stu-id="2f72f-115">Method</span></span>                                                    | <span data-ttu-id="2f72f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f72f-116">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f72f-117">**GetRequestId**</span><span class="sxs-lookup"><span data-stu-id="2f72f-117">**GetRequestId**</span></span>](iwbemcausalityaccess-getrequestid.md) | <span data-ttu-id="2f72f-118">Devuelve un identificador GUID único para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f72f-118">Returns a unique GUID identifier for a request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="2f72f-119">**IsChildOf**</span><span class="sxs-lookup"><span data-stu-id="2f72f-119">**IsChildOf**</span></span>](iwbemcausalityaccess-ischildof.md)       | <span data-ttu-id="2f72f-120">Determina si una solicitud es un elemento secundario de una solicitud primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="2f72f-120">Determines if a request is a child of a specified parent request.</span></span> <span data-ttu-id="2f72f-121">Una solicitud primaria puede tener varias solicitudes secundarias, cada una identificada por un valor GUID único.</span><span class="sxs-lookup"><span data-stu-id="2f72f-121">A parent request can have multiple child requests, each identified by a unique GUID value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2f72f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f72f-122">Requirements</span></span>



| <span data-ttu-id="2f72f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f72f-123">Requirement</span></span> | <span data-ttu-id="2f72f-124">Value</span><span class="sxs-lookup"><span data-stu-id="2f72f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f72f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f72f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2f72f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f72f-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f72f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f72f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2f72f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f72f-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f72f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f72f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f72f-130"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f72f-130"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="2f72f-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f72f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f72f-132"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f72f-132"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f72f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f72f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f72f-134">API COM para WMI</span><span class="sxs-lookup"><span data-stu-id="2f72f-134">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

