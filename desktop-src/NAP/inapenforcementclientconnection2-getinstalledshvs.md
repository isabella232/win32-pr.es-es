---
title: Método INapEnforcementClientConnection2 GetInstalledShvs (NapEnforcementClient. h)
description: Lo usa el agente NAP para consultar los validadores de mantenimiento del sistema (SHV) instalados en el cliente.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Método GetInstalledShvs NAP
- Método GetInstalledShvs NAP, interfaz INapEnforcementClientConnection2
- Interfaz INapEnforcementClientConnection2 NAP, método GetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493247"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a><span data-ttu-id="fa1f6-106">INapEnforcementClientConnection2:: GetInstalledShvs (método)</span><span class="sxs-lookup"><span data-stu-id="fa1f6-106">INapEnforcementClientConnection2::GetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="fa1f6-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fa1f6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fa1f6-108">El agente NAP usa el método **GetInstalledShvs** para consultar los validadores de mantenimiento del sistema (SHV) instalados en el cliente.</span><span class="sxs-lookup"><span data-stu-id="fa1f6-108">The **GetInstalledShvs** method is used by the NAP Agent to query the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa1f6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa1f6-109">Syntax</span></span>


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a><span data-ttu-id="fa1f6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa1f6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa1f6-111">*recuento* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fa1f6-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa1f6-112">Un puntero a un valor [SystemHealthEntityCount](nap-datatypes.md) que especifica el número de SHV instalados en los *identificadores*.</span><span class="sxs-lookup"><span data-stu-id="fa1f6-112">A pointer to a [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of installed SHVs in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="fa1f6-113">*identificadores* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fa1f6-113">*ids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa1f6-114">Puntero a una matriz de valores [SystemHealthEntityId](nap-datatypes.md) que contiene los identificadores de SHV instalados.</span><span class="sxs-lookup"><span data-stu-id="fa1f6-114">A pointer to an array of [SystemHealthEntityId](nap-datatypes.md) values that contain the installed SHV IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa1f6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa1f6-115">Return value</span></span>

<span data-ttu-id="fa1f6-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="fa1f6-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fa1f6-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fa1f6-117">Return code</span></span>                                                                                   | <span data-ttu-id="fa1f6-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa1f6-118">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="fa1f6-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="fa1f6-119"><dt>**S\_OK** </dt></span></span> </dl>         | <span data-ttu-id="fa1f6-120">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa1f6-120">Operation succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="fa1f6-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fa1f6-121"><dt>**E\_INVALIDARG** </dt></span></span> </dl> | <span data-ttu-id="fa1f6-122">Se pasó un argumento no válido al método.</span><span class="sxs-lookup"><span data-stu-id="fa1f6-122">An invalid argument was passed to the method.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fa1f6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa1f6-123">Requirements</span></span>



| <span data-ttu-id="fa1f6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa1f6-124">Requirement</span></span> | <span data-ttu-id="fa1f6-125">Value</span><span class="sxs-lookup"><span data-stu-id="fa1f6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa1f6-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa1f6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fa1f6-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fa1f6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fa1f6-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa1f6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fa1f6-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa1f6-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fa1f6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa1f6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa1f6-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa1f6-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa1f6-132">IDL</span><span class="sxs-lookup"><span data-stu-id="fa1f6-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa1f6-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa1f6-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="fa1f6-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa1f6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa1f6-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa1f6-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fa1f6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa1f6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa1f6-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="fa1f6-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





