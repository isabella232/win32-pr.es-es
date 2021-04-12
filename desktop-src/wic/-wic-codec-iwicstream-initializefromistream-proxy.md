---
description: Función de proxy para el método InitializeFromIStream.
ms.assetid: 3ab780bb-7fe7-4abe-9ea7-86f54ea15d91
title: IWICStream_InitializeFromIStream_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromIStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d80a60d2a142b3c69c03b7352c81bcd0f5fc3ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278192"
---
# <a name="iwicstream_initializefromistream_proxy-function"></a><span data-ttu-id="0b80f-103">IWICStream \_ InitializeFromIStream \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="0b80f-103">IWICStream\_InitializeFromIStream\_Proxy function</span></span>

<span data-ttu-id="0b80f-104">Función de proxy para el método [**InitializeFromIStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) .</span><span class="sxs-lookup"><span data-stu-id="0b80f-104">Proxy function for the [**InitializeFromIStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b80f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b80f-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromIStream_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ IStream    *pIStream
);
```



## <a name="parameters"></a><span data-ttu-id="0b80f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b80f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b80f-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0b80f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b80f-108">Tipo: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="0b80f-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="0b80f-109">Puntero a este objeto [_ *IWICStream* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="0b80f-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="0b80f-110">*pIStream* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b80f-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b80f-111">Tipo: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="0b80f-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="0b80f-112">Secuencia de inicialización.</span><span class="sxs-lookup"><span data-stu-id="0b80f-112">The initialize stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b80f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b80f-113">Return value</span></span>

<span data-ttu-id="0b80f-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0b80f-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0b80f-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0b80f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0b80f-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0b80f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b80f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b80f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0b80f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b80f-118">Requirements</span></span>



| <span data-ttu-id="0b80f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b80f-119">Requirement</span></span> | <span data-ttu-id="0b80f-120">Value</span><span class="sxs-lookup"><span data-stu-id="0b80f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b80f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b80f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0b80f-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b80f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0b80f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b80f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0b80f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b80f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0b80f-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b80f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b80f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b80f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

