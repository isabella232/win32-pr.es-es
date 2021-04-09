---
title: Interfaz INapComponentInfo (NapCommon. h)
description: Proporciona métodos que los componentes de complemento (como Sha y SHV) deben implementar para que el sistema NAP se comunique con ellos.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- Interfaz INapComponentInfo NAP
- Interfaz INapComponentInfo NAP, descripción
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996184"
---
# <a name="inapcomponentinfo-interface"></a><span data-ttu-id="0f35a-105">Interfaz INapComponentInfo</span><span class="sxs-lookup"><span data-stu-id="0f35a-105">INapComponentInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="0f35a-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0f35a-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0f35a-107">La interfaz **INapComponentInfo** proporciona métodos que los componentes de complemento (como Sha y SHV) deben implementar para que el sistema NAP se comunique con ellos.</span><span class="sxs-lookup"><span data-stu-id="0f35a-107">The **INapComponentInfo** interface provides methods that plug-in components (such as SHAs and SHVs) must implement for the NAP system to communicate with them.</span></span> <span data-ttu-id="0f35a-108">El sistema NAP llama a la implementación de estos métodos para recuperar información administrativa estática (por ejemplo, un nombre descriptivo o cadenas localizadas).</span><span class="sxs-lookup"><span data-stu-id="0f35a-108">The NAP system calls your implementation of these methods to retrieve static administrative information (for example, friendly name or localized strings).</span></span>

## <a name="members"></a><span data-ttu-id="0f35a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f35a-109">Members</span></span>

<span data-ttu-id="0f35a-110">La interfaz **INapComponentInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0f35a-110">The **INapComponentInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0f35a-111">**INapComponentInfo** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0f35a-111">**INapComponentInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="0f35a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0f35a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0f35a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="0f35a-113">Methods</span></span>

<span data-ttu-id="0f35a-114">La interfaz **INapComponentInfo** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0f35a-114">The **INapComponentInfo** interface has these methods.</span></span>



| <span data-ttu-id="0f35a-115">Método</span><span class="sxs-lookup"><span data-stu-id="0f35a-115">Method</span></span>                                                                                                         | <span data-ttu-id="0f35a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f35a-116">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f35a-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span><span class="sxs-lookup"><span data-stu-id="0f35a-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span></span>](inapcomponentinfo-converterrorcodetomessageid-method.md) | <span data-ttu-id="0f35a-118">Lo usa el sistema NAP para solicitar al cliente de mantenimiento que convierta un código de error HRESULT en un ID. de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0f35a-118">Used by the NAP System to request the health client convert an HRESULT error code to a message ID.</span></span><br/> |
| [<span data-ttu-id="0f35a-119">**INapComponentInfo:: GetDescription**</span><span class="sxs-lookup"><span data-stu-id="0f35a-119">**INapComponentInfo::GetDescription**</span></span>](inapcomponentinfo-getdescription-method.md)                           | <span data-ttu-id="0f35a-120">Lo usa el sistema NAP para obtener la descripción de un cliente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="0f35a-120">Used by the NAP System to get the description of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="0f35a-121">**INapComponentInfo::GetFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="0f35a-121">**INapComponentInfo::GetFriendlyName**</span></span>](inapcomponentinfo-getfriendlyname-method.md)                         | <span data-ttu-id="0f35a-122">Lo usa el sistema NAP para obtener el nombre descriptivo de un cliente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="0f35a-122">Used by the NAP System to get the friendly name of a health client.</span></span><br/>                                |
| [<span data-ttu-id="0f35a-123">**INapComponentInfo:: GetIcon**</span><span class="sxs-lookup"><span data-stu-id="0f35a-123">**INapComponentInfo::GetIcon**</span></span>](inapcomponentinfo-geticon-method.md)                                         | <span data-ttu-id="0f35a-124">Lo usa el sistema NAP para obtener el icono de un cliente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="0f35a-124">Used by the NAP System to get the icon of a health client.</span></span><br/>                                         |
| [<span data-ttu-id="0f35a-125">**INapComponentInfo::GetLocalizedString**</span><span class="sxs-lookup"><span data-stu-id="0f35a-125">**INapComponentInfo::GetLocalizedString**</span></span>](inapcomponentinfo-getlocalizedstring-method.md)                   | <span data-ttu-id="0f35a-126">Lo usa el sistema NAP para obtener cadenas traducidas.</span><span class="sxs-lookup"><span data-stu-id="0f35a-126">Used by the NAP System to get localized strings.</span></span><br/>                                                   |
| [<span data-ttu-id="0f35a-127">**INapComponentInfo::GetVendorName**</span><span class="sxs-lookup"><span data-stu-id="0f35a-127">**INapComponentInfo::GetVendorName**</span></span>](inapcomponentinfo-getvendorname-method.md)                             | <span data-ttu-id="0f35a-128">Lo usa el sistema NAP para obtener el nombre del proveedor de un cliente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="0f35a-128">Used by the NAP System to get the vendor name of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="0f35a-129">**INapComponentInfo:: GetVersion**</span><span class="sxs-lookup"><span data-stu-id="0f35a-129">**INapComponentInfo::GetVersion**</span></span>](inapcomponentinfo-getversion-method.md)                                   | <span data-ttu-id="0f35a-130">Lo usa el sistema NAP para obtener la versión de un cliente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="0f35a-130">Used by the NAP System to get the version of a health client.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="0f35a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f35a-131">Requirements</span></span>



| <span data-ttu-id="0f35a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f35a-132">Requirement</span></span> | <span data-ttu-id="0f35a-133">Value</span><span class="sxs-lookup"><span data-stu-id="0f35a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f35a-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f35a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0f35a-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0f35a-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0f35a-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f35a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0f35a-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f35a-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0f35a-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f35a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f35a-139"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f35a-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f35a-140">IDL</span><span class="sxs-lookup"><span data-stu-id="0f35a-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f35a-141"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f35a-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f35a-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f35a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f35a-143">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="0f35a-143">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0f35a-144">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="0f35a-144">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

