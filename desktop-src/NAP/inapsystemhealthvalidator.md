---
title: Interfaz INapSystemHealthValidator (NapSystemHealthValidator. h)
description: Deben ser implementados por los desarrolladores de SHV para permitir que el sistema NAP se comunique con un SHV.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- Interfaz INapSystemHealthValidator NAP
- Interfaz INapSystemHealthValidator NAP, descripción
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801826"
---
# <a name="inapsystemhealthvalidator-interface"></a><span data-ttu-id="31c05-105">Interfaz INapSystemHealthValidator</span><span class="sxs-lookup"><span data-stu-id="31c05-105">INapSystemHealthValidator interface</span></span>

> [!Note]  
> <span data-ttu-id="31c05-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="31c05-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="31c05-107">**INapSystemHealthValidator** proporciona métodos que los desarrolladores de SHV deben implementar para permitir que el sistema NAP se comunique con un SHV.</span><span class="sxs-lookup"><span data-stu-id="31c05-107">The **INapSystemHealthValidator** provides methods that must be implemented by SHV developers to enable the NAP system to communicate with an SHV.</span></span>

## <a name="members"></a><span data-ttu-id="31c05-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="31c05-108">Members</span></span>

<span data-ttu-id="31c05-109">La interfaz **INapSystemHealthValidator** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="31c05-109">The **INapSystemHealthValidator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="31c05-110">**INapSystemHealthValidator** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="31c05-110">**INapSystemHealthValidator** also has these types of members:</span></span>

-   [<span data-ttu-id="31c05-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="31c05-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="31c05-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="31c05-112">Methods</span></span>

<span data-ttu-id="31c05-113">La interfaz **INapSystemHealthValidator** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="31c05-113">The **INapSystemHealthValidator** interface has these methods.</span></span>



| <span data-ttu-id="31c05-114">Método</span><span class="sxs-lookup"><span data-stu-id="31c05-114">Method</span></span>                                                                                   | <span data-ttu-id="31c05-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="31c05-115">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31c05-116">**INapSystemHealthValidator:: Validate**</span><span class="sxs-lookup"><span data-stu-id="31c05-116">**INapSystemHealthValidator::Validate**</span></span>](inapsystemhealthvalidator-validate-method.md) | <span data-ttu-id="31c05-117">El sistema NAP llama a este método definido por la aplicación para validar el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recibido de un cliente.</span><span class="sxs-lookup"><span data-stu-id="31c05-117">The NAP system calls this application defined method to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="31c05-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31c05-118">Requirements</span></span>



| <span data-ttu-id="31c05-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="31c05-119">Requirement</span></span> | <span data-ttu-id="31c05-120">Value</span><span class="sxs-lookup"><span data-stu-id="31c05-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31c05-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31c05-121">Minimum supported client</span></span><br/> | <span data-ttu-id="31c05-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="31c05-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="31c05-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31c05-123">Minimum supported server</span></span><br/> | <span data-ttu-id="31c05-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="31c05-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31c05-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31c05-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="31c05-126"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="31c05-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="31c05-127">IDL</span><span class="sxs-lookup"><span data-stu-id="31c05-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31c05-128"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="31c05-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31c05-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="31c05-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c05-130">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="31c05-130">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="31c05-131">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="31c05-131">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

