---
description: Obtiene el método al que se llama cuando se completa la acción asincrónica.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'IAsyncAction:: get_Completed (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154307"
---
# <a name="iasyncactionget_completed-method"></a><span data-ttu-id="f314e-103">IAsyncAction:: get \_ completed (método)</span><span class="sxs-lookup"><span data-stu-id="f314e-103">IAsyncAction::get\_Completed method</span></span>

<span data-ttu-id="f314e-104">Obtiene el método al que se llama cuando se completa la acción asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f314e-104">Gets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f314e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f314e-105">Syntax</span></span>


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a><span data-ttu-id="f314e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f314e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f314e-107">*controlador* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f314e-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f314e-108">Tipo: **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f314e-108">Type: **[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span></span>

<span data-ttu-id="f314e-109">El método que controla la notificación de finalización.</span><span class="sxs-lookup"><span data-stu-id="f314e-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f314e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f314e-110">Return value</span></span>

<span data-ttu-id="f314e-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f314e-111">Type: **HRESULT**</span></span>

<span data-ttu-id="f314e-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f314e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f314e-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f314e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f314e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f314e-114">Requirements</span></span>



| <span data-ttu-id="f314e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f314e-115">Requirement</span></span> | <span data-ttu-id="f314e-116">Value</span><span class="sxs-lookup"><span data-stu-id="f314e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f314e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f314e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f314e-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f314e-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="f314e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f314e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f314e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f314e-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="f314e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f314e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f314e-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f314e-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f314e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f314e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f314e-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="f314e-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
