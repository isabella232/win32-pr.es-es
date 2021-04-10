---
title: Método INapEnforcementClientConnection2 SetInstalledShvs (NapEnforcementClient. h)
description: Lo usa el agente NAP para establecer los validadores de mantenimiento del sistema (SHV) instalados en el cliente.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Método SetInstalledShvs NAP
- Método SetInstalledShvs NAP, interfaz INapEnforcementClientConnection2
- Interfaz INapEnforcementClientConnection2 NAP, método SetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151230"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a><span data-ttu-id="27dde-106">INapEnforcementClientConnection2:: SetInstalledShvs (método)</span><span class="sxs-lookup"><span data-stu-id="27dde-106">INapEnforcementClientConnection2::SetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="27dde-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="27dde-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="27dde-108">El agente NAP usa el método **SetInstalledShvs** para establecer los validadores de mantenimiento del sistema (SHV) instalados en el cliente.</span><span class="sxs-lookup"><span data-stu-id="27dde-108">The **SetInstalledShvs** method is used by the NAP Agent to set the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="27dde-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27dde-109">Syntax</span></span>


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a><span data-ttu-id="27dde-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27dde-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27dde-111">*recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27dde-111">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27dde-112">Valor [SystemHealthEntityCount](nap-datatypes.md) que especifica el número de SHV que se van a instalar en los *identificadores*.</span><span class="sxs-lookup"><span data-stu-id="27dde-112">A [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of SHVs to install in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="27dde-113">*identificadores* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27dde-113">*ids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27dde-114">Un puntero a un valor de [SystemHealthEntityId](nap-datatypes.md) que contiene una lista de identificadores de SHV que se van a instalar.</span><span class="sxs-lookup"><span data-stu-id="27dde-114">A pointer to a [SystemHealthEntityId](nap-datatypes.md) value that contains a list of SHV IDs to install.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27dde-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27dde-115">Return value</span></span>

<span data-ttu-id="27dde-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="27dde-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="27dde-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="27dde-117">Return code</span></span>                                                                                  | <span data-ttu-id="27dde-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="27dde-118">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="27dde-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="27dde-119"><dt>**S\_OK** </dt></span></span> </dl>        | <span data-ttu-id="27dde-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="27dde-120">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="27dde-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="27dde-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="27dde-122">El parámetro *Count* era 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="27dde-122">The *count* parameter was 0 (zero).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="27dde-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27dde-123">Requirements</span></span>



| <span data-ttu-id="27dde-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="27dde-124">Requirement</span></span> | <span data-ttu-id="27dde-125">Value</span><span class="sxs-lookup"><span data-stu-id="27dde-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27dde-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27dde-126">Minimum supported client</span></span><br/> | <span data-ttu-id="27dde-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="27dde-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="27dde-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27dde-128">Minimum supported server</span></span><br/> | <span data-ttu-id="27dde-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="27dde-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="27dde-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27dde-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="27dde-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="27dde-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="27dde-132">IDL</span><span class="sxs-lookup"><span data-stu-id="27dde-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="27dde-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="27dde-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="27dde-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27dde-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27dde-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27dde-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="27dde-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="27dde-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27dde-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="27dde-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





