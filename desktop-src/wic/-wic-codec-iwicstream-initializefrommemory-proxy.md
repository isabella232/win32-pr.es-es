---
description: Función de proxy para el método InitializeFromMemory.
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: IWICStream_InitializeFromMemory_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fe034698635a35c098f6466712d17489f301dd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717213"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="7053c-103">IWICStream \_ InitializeFromMemory \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="7053c-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="7053c-104">Función de proxy para el método [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="7053c-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7053c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7053c-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="7053c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7053c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7053c-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7053c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7053c-108">Tipo: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="7053c-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="7053c-109">Puntero a este objeto [_ *IWICStream* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="7053c-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="7053c-110">*pbBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7053c-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7053c-111">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="7053c-111">Type: \**BYTE\** _</span></span>

<span data-ttu-id="7053c-112">Puntero al búfer utilizado para inicializar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7053c-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="7053c-113">_cbBufferSize \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7053c-113">_cbBufferSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7053c-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7053c-114">Type: **DWORD**</span></span>

<span data-ttu-id="7053c-115">Tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="7053c-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7053c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7053c-116">Return value</span></span>

<span data-ttu-id="7053c-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7053c-117">Type: **HRESULT**</span></span>

<span data-ttu-id="7053c-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7053c-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7053c-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7053c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7053c-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7053c-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7053c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7053c-121">Requirements</span></span>



| <span data-ttu-id="7053c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7053c-122">Requirement</span></span> | <span data-ttu-id="7053c-123">Value</span><span class="sxs-lookup"><span data-stu-id="7053c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7053c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7053c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7053c-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7053c-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7053c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7053c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7053c-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7053c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7053c-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7053c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7053c-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7053c-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




