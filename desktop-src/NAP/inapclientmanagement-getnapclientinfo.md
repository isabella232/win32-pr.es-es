---
title: Método INapClientManagement GetNapClientInfo (NapManagement. h)
description: Recupera información sobre el cliente de NAP.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- Método GetNapClientInfo NAP
- Método GetNapClientInfo NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método GetNapClientInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534630"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a><span data-ttu-id="1aae3-106">INapClientManagement:: GetNapClientInfo (método)</span><span class="sxs-lookup"><span data-stu-id="1aae3-106">INapClientManagement::GetNapClientInfo method</span></span>

> [!Note]  
> <span data-ttu-id="1aae3-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1aae3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1aae3-108">El método **GetNapClientInfo** recupera información sobre el cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="1aae3-108">The **GetNapClientInfo** method retrieves information about the NAP client.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aae3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1aae3-109">Syntax</span></span>


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a><span data-ttu-id="1aae3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1aae3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aae3-111">*isNapEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1aae3-111">*isNapEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aae3-112">Un puntero a un valor BOOLEANO que se establece en **true** si NAP está habilitado; en caso contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="1aae3-112">A pointer to a BOOL that is set to **TRUE** if NAP is enabled; otherwise it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1aae3-113">*nombrecliente* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1aae3-113">*clientName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aae3-114">Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene el nombre del cliente.</span><span class="sxs-lookup"><span data-stu-id="1aae3-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client name.</span></span>

</dd> <dt>

<span data-ttu-id="1aae3-115">*clientDescription* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1aae3-115">*clientDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aae3-116">Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la descripción del cliente.</span><span class="sxs-lookup"><span data-stu-id="1aae3-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client description.</span></span>

</dd> <dt>

<span data-ttu-id="1aae3-117">*protocolVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1aae3-117">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aae3-118">Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión del protocolo.</span><span class="sxs-lookup"><span data-stu-id="1aae3-118">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aae3-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1aae3-119">Return value</span></span>

<span data-ttu-id="1aae3-120">El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="1aae3-120">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="1aae3-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1aae3-121">Return code</span></span>                                                                                         | <span data-ttu-id="1aae3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1aae3-122">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1aae3-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1aae3-123"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="1aae3-124">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="1aae3-124">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1aae3-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1aae3-125"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="1aae3-126">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="1aae3-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1aae3-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1aae3-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="1aae3-128">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="1aae3-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1aae3-129"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="1aae3-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1aae3-130">NapAgent no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="1aae3-130">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="1aae3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1aae3-131">Requirements</span></span>



| <span data-ttu-id="1aae3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aae3-132">Requirement</span></span> | <span data-ttu-id="1aae3-133">Value</span><span class="sxs-lookup"><span data-stu-id="1aae3-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aae3-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1aae3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1aae3-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1aae3-135">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1aae3-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1aae3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1aae3-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1aae3-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1aae3-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1aae3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aae3-139"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aae3-139"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="1aae3-140">IDL</span><span class="sxs-lookup"><span data-stu-id="1aae3-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1aae3-141"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1aae3-141"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="1aae3-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1aae3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aae3-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aae3-143"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="1aae3-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="1aae3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aae3-145">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="1aae3-145">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





