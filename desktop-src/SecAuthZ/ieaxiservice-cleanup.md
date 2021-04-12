---
description: Libera los recursos utilizados por la interfaz IeAxiService.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: 'IeAxiService:: Cleanup (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: b29784ae360ec78b9f7e01d2045617615333a5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277970"
---
# <a name="ieaxiservicecleanup-method"></a><span data-ttu-id="ce6aa-103">IeAxiService:: Cleanup (método)</span><span class="sxs-lookup"><span data-stu-id="ce6aa-103">IeAxiService::Cleanup method</span></span>

<span data-ttu-id="ce6aa-104">El método **Cleanup** libera los recursos utilizados por la interfaz [**IeAxiService**](ieaxiservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ce6aa-104">The **Cleanup** method frees resources used by the [**IeAxiService**](ieaxiservice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6aa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce6aa-105">Syntax</span></span>


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a><span data-ttu-id="ce6aa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce6aa-106">Parameters</span></span>

<span data-ttu-id="ce6aa-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ce6aa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce6aa-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce6aa-108">Return value</span></span>

<span data-ttu-id="ce6aa-109">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="ce6aa-109">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="ce6aa-110">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="ce6aa-110">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="ce6aa-111">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="ce6aa-111">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6aa-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce6aa-112">Requirements</span></span>



| <span data-ttu-id="ce6aa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce6aa-113">Requirement</span></span> | <span data-ttu-id="ce6aa-114">Value</span><span class="sxs-lookup"><span data-stu-id="ce6aa-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6aa-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce6aa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6aa-116">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ce6aa-116">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ce6aa-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce6aa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6aa-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ce6aa-118">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="ce6aa-119">IID</span><span class="sxs-lookup"><span data-stu-id="ce6aa-119">IID</span></span><br/>                      | <span data-ttu-id="ce6aa-120">IID \_ IeAxiService se define como E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="ce6aa-120">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="ce6aa-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce6aa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6aa-122">**IeAxiService**</span><span class="sxs-lookup"><span data-stu-id="ce6aa-122">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

