---
title: Método BasicDevice.remove_ConnectionStatusChanged
description: Anula el registro de un controlador de eventos para el evento ConnectionStatusChanged. | Método BasicDevice.remove_ConnectionStatusChanged
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- método remove_ConnectionStatusChanged API de streaming multimedia
- método remove_ConnectionStatusChanged API de streaming multimedia, interfaz BasicDevice
- BasicDevice interface media streaming API, método remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280106"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="4aba0-107">BasicDevice. Remove \_ ConnectionStatusChanged (método)</span><span class="sxs-lookup"><span data-stu-id="4aba0-107">BasicDevice.remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="4aba0-108">Anula el registro de un controlador de eventos para el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="4aba0-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aba0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4aba0-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="4aba0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4aba0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aba0-111">*token* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4aba0-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aba0-112">Referencia a un token obtenido del método [**Add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) cuando se registró el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="4aba0-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aba0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4aba0-113">Return value</span></span>

<span data-ttu-id="4aba0-114">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4aba0-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4aba0-115">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="4aba0-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4aba0-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4aba0-116">Return code</span></span>                                                                          | <span data-ttu-id="4aba0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4aba0-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4aba0-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4aba0-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4aba0-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="4aba0-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4aba0-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4aba0-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="4aba0-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4aba0-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

