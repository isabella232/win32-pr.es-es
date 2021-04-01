---
title: Método INapClientManagement RegisterEnforcementClient (NapManagement. h)
description: Registra un cliente de cumplimiento con el sistema NAP.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Método RegisterEnforcementClient NAP
- Método RegisterEnforcementClient NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método RegisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150624"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a><span data-ttu-id="b9170-106">INapClientManagement:: RegisterEnforcementClient (método)</span><span class="sxs-lookup"><span data-stu-id="b9170-106">INapClientManagement::RegisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="b9170-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b9170-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b9170-108">El método **RegisterEnforcementClient** registra un cliente de cumplimiento con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="b9170-108">The **RegisterEnforcementClient** method registers an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9170-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9170-109">Syntax</span></span>


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a><span data-ttu-id="b9170-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9170-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9170-111">*aplicación forzada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9170-111">*enforcer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9170-112">Puntero a una estructura de datos [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contiene la información de registro asociada al cliente de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="b9170-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structure that contains the registration information that is associated with the enforcement client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9170-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9170-113">Return value</span></span>

<span data-ttu-id="b9170-114">El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="b9170-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="b9170-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b9170-115">Return code</span></span>                                                                                            | <span data-ttu-id="b9170-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9170-116">Description</span></span>                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9170-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b9170-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="b9170-118">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="b9170-118">Operation successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="b9170-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b9170-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="b9170-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="b9170-120">Permissions error, access denied.</span></span><br/>                                      |
| <dl> <span data-ttu-id="b9170-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b9170-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="b9170-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b9170-122">System resource limit, could not perform the operation.</span></span><br/>                |
| <dl> <span data-ttu-id="b9170-123"><dt>**\_ \_ identificador conflictivo de NAP \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="b9170-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="b9170-124">Ya está registrado un agente de cumplimiento con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="b9170-124">An enforcement agent using the given identifier is already registered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b9170-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9170-125">Requirements</span></span>



| <span data-ttu-id="b9170-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9170-126">Requirement</span></span> | <span data-ttu-id="b9170-127">Value</span><span class="sxs-lookup"><span data-stu-id="b9170-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9170-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9170-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b9170-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b9170-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b9170-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9170-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b9170-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9170-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b9170-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9170-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9170-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9170-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9170-134">IDL</span><span class="sxs-lookup"><span data-stu-id="b9170-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9170-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9170-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="b9170-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9170-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9170-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9170-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="b9170-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9170-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9170-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="b9170-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





