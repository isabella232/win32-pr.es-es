---
description: Establece el método al que se llama cuando se completa la acción asincrónica.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: IAsyncAction::p ut_Completed método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.put_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: ec26401aeeed61445b0f244880864366fd5c6118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001151"
---
# <a name="iasyncactionput_completed-method"></a><span data-ttu-id="d58cb-103">IAsyncAction: \_ método completado:p UT</span><span class="sxs-lookup"><span data-stu-id="d58cb-103">IAsyncAction::put\_Completed method</span></span>

<span data-ttu-id="d58cb-104">Establece el método al que se llama cuando se completa la acción asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d58cb-104">Sets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d58cb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d58cb-105">Syntax</span></span>


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a><span data-ttu-id="d58cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d58cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d58cb-107">*controlador* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d58cb-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d58cb-108">Tipo: \**[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d58cb-108">Type: \**[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\** _</span></span>

<span data-ttu-id="d58cb-109">El método que controla la notificación de finalización.</span><span class="sxs-lookup"><span data-stu-id="d58cb-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d58cb-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d58cb-110">Return value</span></span>

<span data-ttu-id="d58cb-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d58cb-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d58cb-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d58cb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d58cb-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d58cb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d58cb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d58cb-114">Requirements</span></span>



| <span data-ttu-id="d58cb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d58cb-115">Requirement</span></span> | <span data-ttu-id="d58cb-116">Value</span><span class="sxs-lookup"><span data-stu-id="d58cb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d58cb-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d58cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d58cb-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d58cb-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="d58cb-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d58cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d58cb-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d58cb-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="d58cb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d58cb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d58cb-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d58cb-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d58cb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d58cb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d58cb-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="d58cb-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
