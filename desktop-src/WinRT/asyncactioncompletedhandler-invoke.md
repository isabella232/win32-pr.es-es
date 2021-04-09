---
description: Invoca el método al que se llama cuando se completa la acción asincrónica especificada.
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: 'AsyncActionCompletedHandler:: Invoke (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 1cba9c48fa955b82fdc337ba641acbd4c62f6406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154311"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a><span data-ttu-id="a7324-103">AsyncActionCompletedHandler:: Invoke (método)</span><span class="sxs-lookup"><span data-stu-id="a7324-103">AsyncActionCompletedHandler::Invoke method</span></span>

<span data-ttu-id="a7324-104">Invoca el método al que se llama cuando se completa la acción asincrónica especificada.</span><span class="sxs-lookup"><span data-stu-id="a7324-104">Invokes the method that is called when the specified asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7324-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7324-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a7324-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7324-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7324-107">*asyncInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7324-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7324-108">Tipo: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) \** _</span><span class="sxs-lookup"><span data-stu-id="a7324-108">Type: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)\** _</span></span>

<span data-ttu-id="a7324-109">La acción asincrónica que informa de la finalización.</span><span class="sxs-lookup"><span data-stu-id="a7324-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7324-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7324-110">Return value</span></span>

<span data-ttu-id="a7324-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a7324-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a7324-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a7324-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7324-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7324-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7324-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7324-114">Requirements</span></span>



| <span data-ttu-id="a7324-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7324-115">Requirement</span></span> | <span data-ttu-id="a7324-116">Value</span><span class="sxs-lookup"><span data-stu-id="a7324-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7324-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7324-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a7324-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a7324-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="a7324-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7324-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a7324-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7324-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="a7324-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7324-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7324-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7324-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7324-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7324-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7324-124">**AsyncActionCompletedHandler**</span><span class="sxs-lookup"><span data-stu-id="a7324-124">**AsyncActionCompletedHandler**</span></span>](asyncactioncompletedhandler.md)
</dt> </dl>

 

