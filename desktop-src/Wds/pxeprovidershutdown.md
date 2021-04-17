---
title: Función de devolución de llamada PxeProviderShutdown
description: Se llama para cerrar el proveedor.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Función de devolución de llamada PxeProviderShutdown servicios de implementación de Windows
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705139"
---
# <a name="pxeprovidershutdown-callback-function"></a><span data-ttu-id="ad7cf-104">Función de devolución de llamada PxeProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="ad7cf-104">PxeProviderShutdown callback function</span></span>

<span data-ttu-id="ad7cf-105">Se llama para cerrar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-105">Called to shutdown the provider.</span></span> <span data-ttu-id="ad7cf-106">Esta función se registra mediante una llamada a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el parámetro *CallbackType* establecido en apagado de la **\_ devolución de llamada \_ PXE**.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SHUTDOWN**.</span></span> <span data-ttu-id="ad7cf-107">Después de llamar a esta función, el identificador *hProvider* pasado a la función [*PxeProviderInitialize*](pxeproviderinitialize.md) ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-107">After this function is called, the *hProvider* handle passed to the [*PxeProviderInitialize*](pxeproviderinitialize.md) function is no longer valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7cf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad7cf-108">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a><span data-ttu-id="ad7cf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad7cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad7cf-110">*pContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ad7cf-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7cf-111">Valor de contexto que se pasa a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="ad7cf-111">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad7cf-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad7cf-112">Return value</span></span>

<span data-ttu-id="ad7cf-113">Si el cierre del proveedor se realiza correctamente, la devolución de llamada debe devolver el **error \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-113">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="ad7cf-114">En caso de error, se debe devolver un código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-114">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad7cf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad7cf-115">Requirements</span></span>



| <span data-ttu-id="ad7cf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad7cf-116">Requirement</span></span> | <span data-ttu-id="ad7cf-117">Value</span><span class="sxs-lookup"><span data-stu-id="ad7cf-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7cf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad7cf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ad7cf-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ad7cf-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="ad7cf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad7cf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ad7cf-121">Windows Server 2008, Windows Server 2003 con \[ solo aplicaciones de escritorio de SP2\]</span><span class="sxs-lookup"><span data-stu-id="ad7cf-121">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad7cf-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad7cf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7cf-123">Funciones de servidor de servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="ad7cf-123">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="ad7cf-124">*PxeProviderInitialize*</span><span class="sxs-lookup"><span data-stu-id="ad7cf-124">*PxeProviderInitialize*</span></span>](pxeproviderinitialize.md)
</dt> <dt>

[<span data-ttu-id="ad7cf-125">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="ad7cf-125">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





