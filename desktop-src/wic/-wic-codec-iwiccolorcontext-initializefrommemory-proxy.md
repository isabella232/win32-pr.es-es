---
description: Función de proxy para el método InitializeFromMemory.
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: IWICColorContext_InitializeFromMemory_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 32c3c24902b6c3157b9776d84c5a8eea47cce43e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706492"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="8eb17-103">IWICColorContext \_ InitializeFromMemory \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="8eb17-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="8eb17-104">Función de proxy para el método [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="8eb17-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb17-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8eb17-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="8eb17-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8eb17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eb17-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8eb17-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eb17-108">Tipo: \**[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) \** _</span><span class="sxs-lookup"><span data-stu-id="8eb17-108">Type: \**[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\** _</span></span>

</dd> <dt>

<span data-ttu-id="8eb17-109">_pbBuffer \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8eb17-109">_pbBuffer\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eb17-110">Tipo: \**const byte \** _</span><span class="sxs-lookup"><span data-stu-id="8eb17-110">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="8eb17-111">Búfer que se usa para inicializar [_ *IWICColorContext* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="8eb17-111">The buffer used to initialize the [_ *IWICColorContext*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="8eb17-112">*cbBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8eb17-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eb17-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8eb17-113">Type: **UINT**</span></span>

<span data-ttu-id="8eb17-114">Tamaño del búfer de *pbBuffer* .</span><span class="sxs-lookup"><span data-stu-id="8eb17-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eb17-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8eb17-115">Return value</span></span>

<span data-ttu-id="8eb17-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8eb17-116">Type: **HRESULT**</span></span>

<span data-ttu-id="8eb17-117">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8eb17-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8eb17-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8eb17-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eb17-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8eb17-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb17-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eb17-120">Requirements</span></span>



| <span data-ttu-id="8eb17-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb17-121">Requirement</span></span> | <span data-ttu-id="8eb17-122">Value</span><span class="sxs-lookup"><span data-stu-id="8eb17-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb17-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8eb17-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb17-124">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8eb17-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8eb17-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8eb17-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb17-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8eb17-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8eb17-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8eb17-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eb17-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8eb17-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




