---
title: Método INapEnforcementClientCallback GetConnections (NapEnforcementClient. h)
description: Lo llama NapAgent y lo implementa el cliente de cumplimiento para devolver un conjunto de conexiones.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Método GetConnections NAP
- Método GetConnections NAP, interfaz INapEnforcementClientCallback
- Interfaz INapEnforcementClientCallback NAP, método GetConnections
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905635"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a><span data-ttu-id="2fc10-106">INapEnforcementClientCallback:: GetConnections (método)</span><span class="sxs-lookup"><span data-stu-id="2fc10-106">INapEnforcementClientCallback::GetConnections method</span></span>

> [!Note]  
> <span data-ttu-id="2fc10-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="2fc10-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2fc10-108">El NapAgent llama al método de devolución de llamada **INapEnforcementClientCallback:: GetConnections** y lo implementa el cliente de cumplimiento para devolver un conjunto de conexiones.</span><span class="sxs-lookup"><span data-stu-id="2fc10-108">The **INapEnforcementClientCallback::GetConnections** callback method is called by the NapAgent and implemented by the enforcement client to return a set of connections.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc10-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fc10-109">Syntax</span></span>


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a><span data-ttu-id="2fc10-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fc10-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc10-111">*conexiones* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2fc10-111">*connections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc10-112">Puntero al conjunto actual de [**conexiones**](connections-struct.md)mantenidas.</span><span class="sxs-lookup"><span data-stu-id="2fc10-112">A pointer to the current set of maintained [**Connections**](connections-struct.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc10-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fc10-113">Return value</span></span>

<span data-ttu-id="2fc10-114">Este método de devolución de llamada debe devolver uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="2fc10-114">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="2fc10-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2fc10-115">Return code</span></span>                                                                                                | <span data-ttu-id="2fc10-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fc10-116">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2fc10-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc10-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="2fc10-118">Devuelve este valor si la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2fc10-118">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="2fc10-119"><dt>**el \_ servidor RPC S \_ \_ no está disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc10-119"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="2fc10-120">Al devolver este valor, el aplicador se quita de la lista Bound-SHA y la entrada de caché de NapAgent correspondiente que se va a vaciar.</span><span class="sxs-lookup"><span data-stu-id="2fc10-120">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="2fc10-121">Después, el SHA con error puede volver a inicializarse con el NapAgent.</span><span class="sxs-lookup"><span data-stu-id="2fc10-121">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2fc10-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fc10-122">Requirements</span></span>



| <span data-ttu-id="2fc10-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fc10-123">Requirement</span></span> | <span data-ttu-id="2fc10-124">Value</span><span class="sxs-lookup"><span data-stu-id="2fc10-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc10-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fc10-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2fc10-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2fc10-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2fc10-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fc10-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2fc10-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2fc10-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2fc10-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fc10-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fc10-130"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fc10-130"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fc10-131">IDL</span><span class="sxs-lookup"><span data-stu-id="2fc10-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2fc10-132"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2fc10-132"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fc10-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fc10-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc10-134">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="2fc10-134">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





