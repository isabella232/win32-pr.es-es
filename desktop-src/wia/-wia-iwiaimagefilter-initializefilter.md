---
description: Inicializa el filtro. Lo llama la adquisición de imágenes de Windows (WIA) 2,0 antes de descargar cada imagen.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'IWiaImageFilter:: InitializeFilter (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716051"
---
# <a name="iwiaimagefilterinitializefilter-method"></a><span data-ttu-id="8e1cc-104">IWiaImageFilter:: InitializeFilter (método)</span><span class="sxs-lookup"><span data-stu-id="8e1cc-104">IWiaImageFilter::InitializeFilter method</span></span>

<span data-ttu-id="8e1cc-105">Inicializa el filtro.</span><span class="sxs-lookup"><span data-stu-id="8e1cc-105">Initializes the filter.</span></span> <span data-ttu-id="8e1cc-106">Lo llama la adquisición de imágenes de Windows (WIA) 2,0 antes de descargar cada imagen.</span><span class="sxs-lookup"><span data-stu-id="8e1cc-106">Called by Windows Image Acquisition (WIA) 2.0 before each image download.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1cc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e1cc-107">Syntax</span></span>


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="8e1cc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e1cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e1cc-109">*pWiaItem2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1cc-109">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1cc-110">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="8e1cc-110">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="8e1cc-111">Especifica un puntero al elemento [_ *IWiaItem2* \*](-wia-iwiaitem2.md) que representa la imagen de vista previa.</span><span class="sxs-lookup"><span data-stu-id="8e1cc-111">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item that represents the preview image.</span></span>

</dd> <dt>

<span data-ttu-id="8e1cc-112">*pWiaTransferCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1cc-112">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1cc-113">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="8e1cc-113">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="8e1cc-114">Especifica un puntero a la interfaz [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8e1cc-114">Specifies a pointer to the application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e1cc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e1cc-115">Return value</span></span>

<span data-ttu-id="8e1cc-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8e1cc-116">Type: **HRESULT**</span></span>

<span data-ttu-id="8e1cc-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8e1cc-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e1cc-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e1cc-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e1cc-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e1cc-119">Remarks</span></span>

<span data-ttu-id="8e1cc-120">Se llama a este método cuando una aplicación llama a [**download**](-wia-iwiatransfer-download.md) y cuando una aplicación llama a la función del componente de vista previa de WIA 2,0 `GetNewPreview` .</span><span class="sxs-lookup"><span data-stu-id="8e1cc-120">This method is called when an application calls [**Download**](-wia-iwiatransfer-download.md) and when an application calls the WIA 2.0 Preview Component's `GetNewPreview` function.</span></span> <span data-ttu-id="8e1cc-121">**IWiaImageFilter:: InitializeFilter** almacena las referencias a *pWiaItem2* y *pWiaTransferCallback* para pasarlas a estas funciones.</span><span class="sxs-lookup"><span data-stu-id="8e1cc-121">**IWiaImageFilter::InitializeFilter** stores the references to *pWiaItem2* and *pWiaTransferCallback* to pass into these functions.</span></span> <span data-ttu-id="8e1cc-122">Estos dos punteros de interfaz deben almacenarse como variables de miembro y se debe llamar a [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para cada uno.</span><span class="sxs-lookup"><span data-stu-id="8e1cc-122">These two interface pointers should be stored as member variables and [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) should be called for each.</span></span> <span data-ttu-id="8e1cc-123">Los punteros de interfaz también son necesarios en la implementación del filtro de [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) y [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) durante la adquisición de la imagen.</span><span class="sxs-lookup"><span data-stu-id="8e1cc-123">The interface pointers are also needed in the filter's implementation of [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) and [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) during image acquisition.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1cc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e1cc-124">Requirements</span></span>



| <span data-ttu-id="8e1cc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e1cc-125">Requirement</span></span> | <span data-ttu-id="8e1cc-126">Value</span><span class="sxs-lookup"><span data-stu-id="8e1cc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1cc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e1cc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8e1cc-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8e1cc-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8e1cc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e1cc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8e1cc-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e1cc-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8e1cc-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e1cc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e1cc-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e1cc-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e1cc-133">IDL</span><span class="sxs-lookup"><span data-stu-id="8e1cc-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8e1cc-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8e1cc-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 
