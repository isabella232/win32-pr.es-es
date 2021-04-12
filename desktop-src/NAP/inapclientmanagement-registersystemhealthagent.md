---
title: Método INapClientManagement RegisterSystemHealthAgent (NapManagement. h)
description: Registra un SHA con el sistema NAP.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Método RegisterSystemHealthAgent NAP
- Método RegisterSystemHealthAgent NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método RegisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491710"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a><span data-ttu-id="c95ed-106">INapClientManagement:: RegisterSystemHealthAgent (método)</span><span class="sxs-lookup"><span data-stu-id="c95ed-106">INapClientManagement::RegisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="c95ed-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c95ed-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c95ed-108">El método **RegisterSystemHealthAgent** registra un Sha con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="c95ed-108">The **RegisterSystemHealthAgent** method registers an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c95ed-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c95ed-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a><span data-ttu-id="c95ed-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c95ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c95ed-111">*agente* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c95ed-111">*agent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c95ed-112">Puntero a una estructura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contiene la información de registro para el Sha.</span><span class="sxs-lookup"><span data-stu-id="c95ed-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the registration information for the SHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c95ed-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c95ed-113">Return value</span></span>

<span data-ttu-id="c95ed-114">El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="c95ed-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="c95ed-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c95ed-115">Return code</span></span>                                                                                            | <span data-ttu-id="c95ed-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c95ed-116">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c95ed-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c95ed-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="c95ed-118">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="c95ed-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c95ed-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c95ed-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="c95ed-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="c95ed-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c95ed-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c95ed-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="c95ed-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c95ed-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c95ed-123"><dt>**\_ \_ identificador conflictivo de NAP \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="c95ed-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="c95ed-124">Un SHA que usa este identificador ya está registrado.</span><span class="sxs-lookup"><span data-stu-id="c95ed-124">An SHA that uses this ID is already registered.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="c95ed-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c95ed-125">Requirements</span></span>



| <span data-ttu-id="c95ed-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c95ed-126">Requirement</span></span> | <span data-ttu-id="c95ed-127">Value</span><span class="sxs-lookup"><span data-stu-id="c95ed-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c95ed-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c95ed-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c95ed-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c95ed-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c95ed-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c95ed-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c95ed-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c95ed-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c95ed-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c95ed-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c95ed-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="c95ed-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="c95ed-134">IDL</span><span class="sxs-lookup"><span data-stu-id="c95ed-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c95ed-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c95ed-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="c95ed-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c95ed-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c95ed-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c95ed-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="c95ed-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c95ed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c95ed-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="c95ed-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





