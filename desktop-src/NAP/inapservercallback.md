---
title: Interfaz INapServerCallback (NapSystemHealthValidator. h)
description: Los SHV usan para indicar la finalización de la solicitud asincrónica.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- Interfaz INapServerCallback NAP
- Interfaz INapServerCallback NAP, descripción
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489160"
---
# <a name="inapservercallback-interface"></a><span data-ttu-id="bd6ab-105">Interfaz INapServerCallback</span><span class="sxs-lookup"><span data-stu-id="bd6ab-105">INapServerCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="bd6ab-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="bd6ab-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bd6ab-107">**INapServerCallback** proporciona un método que los SHV usan para indicar la finalización de la solicitud asincrónica.</span><span class="sxs-lookup"><span data-stu-id="bd6ab-107">The **INapServerCallback** provides a method that SHVs use to signal asynchronous request completion.</span></span>

## <a name="members"></a><span data-ttu-id="bd6ab-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bd6ab-108">Members</span></span>

<span data-ttu-id="bd6ab-109">La interfaz **INapServerCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bd6ab-109">The **INapServerCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bd6ab-110">**INapServerCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bd6ab-110">**INapServerCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="bd6ab-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="bd6ab-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bd6ab-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="bd6ab-112">Methods</span></span>

<span data-ttu-id="bd6ab-113">La interfaz **INapServerCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bd6ab-113">The **INapServerCallback** interface has these methods.</span></span>



| <span data-ttu-id="bd6ab-114">Método</span><span class="sxs-lookup"><span data-stu-id="bd6ab-114">Method</span></span>                                                                         | <span data-ttu-id="bd6ab-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd6ab-115">Description</span></span>                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="bd6ab-116">**INapServerCallback:: alcompletar**</span><span class="sxs-lookup"><span data-stu-id="bd6ab-116">**INapServerCallback::OnComplete**</span></span>](inapservercallback-oncomplete-method.md) | <span data-ttu-id="bd6ab-117">Lo usan los SHV para indicar la finalización de la solicitud asincrónica.</span><span class="sxs-lookup"><span data-stu-id="bd6ab-117">Used by SHVs to signal asynchronous request completion.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bd6ab-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd6ab-118">Requirements</span></span>



| <span data-ttu-id="bd6ab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd6ab-119">Requirement</span></span> | <span data-ttu-id="bd6ab-120">Value</span><span class="sxs-lookup"><span data-stu-id="bd6ab-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6ab-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd6ab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6ab-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bd6ab-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="bd6ab-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd6ab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6ab-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd6ab-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd6ab-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd6ab-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd6ab-126"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd6ab-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd6ab-127">IDL</span><span class="sxs-lookup"><span data-stu-id="bd6ab-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd6ab-128"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd6ab-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="bd6ab-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd6ab-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd6ab-130"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd6ab-130"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="bd6ab-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd6ab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd6ab-132">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="bd6ab-132">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="bd6ab-133">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="bd6ab-133">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

