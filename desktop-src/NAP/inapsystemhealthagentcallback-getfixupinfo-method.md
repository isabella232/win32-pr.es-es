---
title: Método INapSystemHealthAgentCallback GetFixupInfo (NapSystemHealthAgent. h)
description: El NapAgent llama a este método para determinar el estado del agente de mantenimiento del sistema mientras está procesando un SoHResponse.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Método GetFixupInfo NAP
- Método GetFixupInfo NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método GetFixupInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150439"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a><span data-ttu-id="19008-106">INapSystemHealthAgentCallback:: GetFixupInfo (método)</span><span class="sxs-lookup"><span data-stu-id="19008-106">INapSystemHealthAgentCallback::GetFixupInfo method</span></span>

> [!Note]  
> <span data-ttu-id="19008-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="19008-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="19008-108">El NapAgent llama al método **INapSystemHealthAgentCallback:: GetFixupInfo** para determinar el estado del agente de mantenimiento del sistema mientras está procesando un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="19008-108">The **INapSystemHealthAgentCallback::GetFixupInfo** method is called by the NapAgent to determine the state of the system health agent, while it is processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="19008-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19008-109">Syntax</span></span>


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="19008-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19008-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19008-111">*información* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="19008-111">*info* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19008-112">Un puntero a un puntero a una estructura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) que contiene el estado de corrección del agente.</span><span class="sxs-lookup"><span data-stu-id="19008-112">A pointer to a pointer to a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure that contains the fix-up status of the agent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19008-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19008-113">Return value</span></span>

<span data-ttu-id="19008-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="19008-114">This method can return one of these values.</span></span>



| <span data-ttu-id="19008-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="19008-115">Return code</span></span>                                                                          | <span data-ttu-id="19008-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="19008-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="19008-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="19008-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="19008-118">Indica que se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="19008-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="19008-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19008-119">Remarks</span></span>

<span data-ttu-id="19008-120">Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.</span><span class="sxs-lookup"><span data-stu-id="19008-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="19008-121">El agente de mantenimiento del sistema debe devolver **S \_ OK** inmediatamente sin bloquearse.</span><span class="sxs-lookup"><span data-stu-id="19008-121">The system health agent must return **S\_OK** immediately without blocking.</span></span>

## <a name="requirements"></a><span data-ttu-id="19008-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19008-122">Requirements</span></span>



| <span data-ttu-id="19008-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="19008-123">Requirement</span></span> | <span data-ttu-id="19008-124">Value</span><span class="sxs-lookup"><span data-stu-id="19008-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19008-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19008-125">Minimum supported client</span></span><br/> | <span data-ttu-id="19008-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="19008-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="19008-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19008-127">Minimum supported server</span></span><br/> | <span data-ttu-id="19008-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="19008-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="19008-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19008-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="19008-130"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="19008-130"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="19008-131">IDL</span><span class="sxs-lookup"><span data-stu-id="19008-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19008-132"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19008-132"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19008-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="19008-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19008-134">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="19008-134">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





