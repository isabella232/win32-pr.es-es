---
title: Método IConnectionBrokerRequest CheckStatus (Cbclient. h)
description: Se llama para determinar el estado de una solicitud asincrónica.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- Método CheckStatus Servicios de Escritorio remoto
- Método CheckStatus Servicios de Escritorio remoto, interfaz IConnectionBrokerRequest
- Interfaz IConnectionBrokerRequest Servicios de Escritorio remoto, método CheckStatus
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422573"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a><span data-ttu-id="44903-106">IConnectionBrokerRequest:: CheckStatus (método)</span><span class="sxs-lookup"><span data-stu-id="44903-106">IConnectionBrokerRequest::CheckStatus method</span></span>

<span data-ttu-id="44903-107">Se llama para determinar el estado de una solicitud asincrónica.</span><span class="sxs-lookup"><span data-stu-id="44903-107">Called to determine the status of an asynchronous request.</span></span>

## <a name="syntax"></a><span data-ttu-id="44903-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44903-108">Syntax</span></span>


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a><span data-ttu-id="44903-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44903-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44903-110">*pReqStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="44903-110">*pReqStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44903-111">Dirección de una variable que recibe un valor de la enumeración del [**\_ \_ Estado de la solicitud CB**](cb-request-status.md) que indica el estado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="44903-111">The address of a variable that receives a value of the [**CB\_REQUEST\_STATUS**](cb-request-status.md) enumeration that indicates the status of the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44903-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44903-112">Return value</span></span>

<span data-ttu-id="44903-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="44903-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="44903-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="44903-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44903-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44903-115">Requirements</span></span>



| <span data-ttu-id="44903-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44903-116">Requirement</span></span> | <span data-ttu-id="44903-117">Value</span><span class="sxs-lookup"><span data-stu-id="44903-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44903-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44903-118">Minimum supported client</span></span><br/> | <span data-ttu-id="44903-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="44903-119">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="44903-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44903-120">Minimum supported server</span></span><br/> | <span data-ttu-id="44903-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44903-121">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="44903-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44903-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="44903-123"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="44903-123"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="44903-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44903-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="44903-125"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44903-125"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="44903-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44903-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44903-127"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44903-127"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44903-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="44903-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44903-129">**IConnectionBrokerRequest**</span><span class="sxs-lookup"><span data-stu-id="44903-129">**IConnectionBrokerRequest**</span></span>](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





