---
description: Establece una nueva devolución de llamada de aplicación para el filtro de procesamiento de imágenes que se va a usar para las llamadas de reenvío.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'IWiaImageFilter:: SetNewCallback (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810772"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a><span data-ttu-id="5516f-103">IWiaImageFilter:: SetNewCallback (método)</span><span class="sxs-lookup"><span data-stu-id="5516f-103">IWiaImageFilter::SetNewCallback method</span></span>

<span data-ttu-id="5516f-104">Establece una nueva devolución de llamada de aplicación para el filtro de procesamiento de imágenes que se va a usar para las llamadas de reenvío.</span><span class="sxs-lookup"><span data-stu-id="5516f-104">Sets a new application callback for the image processing filter to use for forwarding calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="5516f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5516f-105">Syntax</span></span>


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="5516f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5516f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5516f-107">*pWiaTransferCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5516f-107">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5516f-108">Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span><span class="sxs-lookup"><span data-stu-id="5516f-108">Type: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span></span>

<span data-ttu-id="5516f-109">Especifica un puntero a la interfaz [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5516f-109">Specifies a pointer to the application's [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5516f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5516f-110">Return value</span></span>

<span data-ttu-id="5516f-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5516f-111">Type: **HRESULT**</span></span>

<span data-ttu-id="5516f-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5516f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5516f-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5516f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5516f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5516f-114">Remarks</span></span>

<span data-ttu-id="5516f-115">No llame a este método directamente desde su aplicación.</span><span class="sxs-lookup"><span data-stu-id="5516f-115">Do not call this method directly from your application.</span></span>

<span data-ttu-id="5516f-116">El filtro de procesamiento de imágenes es necesario para liberar la interfaz de devolución de llamada de la aplicación previamente almacenada antes de establecer la nueva devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="5516f-116">The image processing filter is required to release the previously stored application callback interface before setting the new callback.</span></span>

<span data-ttu-id="5516f-117">Si *pWiaTransferCallback* es **null**, el filtro de procesamiento de imágenes simplemente debe liberar la devolución de llamada de la aplicación anterior y devolver S \_ .</span><span class="sxs-lookup"><span data-stu-id="5516f-117">If *pWiaTransferCallback* is **NULL**, the image processing filter should simply release the old application callback and return S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="5516f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5516f-118">Requirements</span></span>



| <span data-ttu-id="5516f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5516f-119">Requirement</span></span> | <span data-ttu-id="5516f-120">Value</span><span class="sxs-lookup"><span data-stu-id="5516f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5516f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5516f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5516f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5516f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5516f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5516f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5516f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5516f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5516f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5516f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5516f-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5516f-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5516f-127">IDL</span><span class="sxs-lookup"><span data-stu-id="5516f-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5516f-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5516f-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




