---
description: Proporciona el progreso y otras notificaciones durante una transferencia.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'IWiaTransferCallback:: TransferCallback (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696517"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a><span data-ttu-id="7414f-103">IWiaTransferCallback:: TransferCallback (método)</span><span class="sxs-lookup"><span data-stu-id="7414f-103">IWiaTransferCallback::TransferCallback method</span></span>

<span data-ttu-id="7414f-104">Proporciona el progreso y otras notificaciones durante una transferencia.</span><span class="sxs-lookup"><span data-stu-id="7414f-104">Provides progress and other notifications during a transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7414f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7414f-105">Syntax</span></span>


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a><span data-ttu-id="7414f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7414f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7414f-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7414f-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7414f-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="7414f-108">Type: **LONG**</span></span>

<span data-ttu-id="7414f-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="7414f-109">Currently unused.</span></span> <span data-ttu-id="7414f-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="7414f-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7414f-111">*pWiaTransferParams* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7414f-111">*pWiaTransferParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7414f-112">Tipo: \**[**WiaTransferParams**](-wia-wiatransferparams.md) \** _</span><span class="sxs-lookup"><span data-stu-id="7414f-112">Type: \**[**WiaTransferParams**](-wia-wiatransferparams.md)\** _</span></span>

<span data-ttu-id="7414f-113">Especifica un puntero a una estructura [_ *WiaTransferParams* \*](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="7414f-113">Specifies a pointer to a [_ *WiaTransferParams*\*](-wia-wiatransferparams.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7414f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7414f-114">Return value</span></span>

<span data-ttu-id="7414f-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7414f-115">Type: **HRESULT**</span></span>

<span data-ttu-id="7414f-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7414f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7414f-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7414f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7414f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7414f-118">Remarks</span></span>

<span data-ttu-id="7414f-119">Cuando un filtro de procesamiento de imágenes implementa este método, el minicontrolador de adquisición de imágenes de Windows (WIA) 2,0 lo llama durante la adquisición de la imagen para devolver mensajes de progreso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7414f-119">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to send progress messages back to the application.</span></span>

<span data-ttu-id="7414f-120">**IWiaTransferCallback:: TransferCallback** de un filtro debe delegarse en el método **IWiaTransferCallback:: TransferCallback** de la devolución de llamada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7414f-120">A filter's **IWiaTransferCallback::TransferCallback** must delegate to the application callback's **IWiaTransferCallback::TransferCallback** method.</span></span> <span data-ttu-id="7414f-121">Normalmente, el flujo de filtro filtra los datos que se le pasan y escribe los datos filtrados directamente en la secuencia proporcionada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7414f-121">Usually, the filter stream filters the data passed to it and writes the filtered data directly to the application provided stream.</span></span> <span data-ttu-id="7414f-122">Cuando el filtro de procesamiento de imágenes almacena datos entre llamadas a su método [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , también debe modificar los valores *lPercentComplete* y *ulBytesWrittenToCurrentStream* en la estructura [**WiaTransferParams**](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="7414f-122">When image processing filter stores data between calls to its [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method, it must also modify the *lPercentComplete* and *ulBytesWrittenToCurrentStream* values in the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7414f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7414f-123">Requirements</span></span>



| <span data-ttu-id="7414f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7414f-124">Requirement</span></span> | <span data-ttu-id="7414f-125">Value</span><span class="sxs-lookup"><span data-stu-id="7414f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7414f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7414f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7414f-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7414f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7414f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7414f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7414f-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7414f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7414f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7414f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7414f-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="7414f-131"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="7414f-132">IDL</span><span class="sxs-lookup"><span data-stu-id="7414f-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7414f-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7414f-133"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="7414f-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7414f-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="7414f-135"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7414f-135"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
