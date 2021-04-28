---
description: 'IWICColorContext_InitializeFromMemory_Proxy función: función de proxy para el método InitializeFromMemory.'
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: IWICColorContext_InitializeFromMemory_Proxy función
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
ms.openlocfilehash: e77bbcf1e430891b031b2e77bc168c33f781eacf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097223"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="88946-103">Función IWICColorContext \_ InitializeFromMemory \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="88946-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="88946-104">Función de proxy para [**el método InitializeFromMemory.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory)</span><span class="sxs-lookup"><span data-stu-id="88946-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="88946-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88946-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="88946-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88946-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88946-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="88946-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88946-108">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="88946-108">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

</dd> <dt>

<span data-ttu-id="88946-109">*pbBuffer* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="88946-109">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88946-110">Tipo: **const \* BYTE**</span><span class="sxs-lookup"><span data-stu-id="88946-110">Type: **const BYTE\***</span></span>

<span data-ttu-id="88946-111">Búfer utilizado para inicializar [**IWICColorContext.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)</span><span class="sxs-lookup"><span data-stu-id="88946-111">The buffer used to initialize the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="88946-112">*cbBufferSize* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="88946-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88946-113">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="88946-113">Type: **UINT**</span></span>

<span data-ttu-id="88946-114">Tamaño del búfer *pbBuffer.*</span><span class="sxs-lookup"><span data-stu-id="88946-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88946-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88946-115">Return value</span></span>

<span data-ttu-id="88946-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="88946-116">Type: **HRESULT**</span></span>

<span data-ttu-id="88946-117">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="88946-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88946-118">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="88946-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88946-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88946-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="88946-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88946-120">Requirements</span></span>



| <span data-ttu-id="88946-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="88946-121">Requirement</span></span> | <span data-ttu-id="88946-122">Valor</span><span class="sxs-lookup"><span data-stu-id="88946-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88946-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88946-123">Minimum supported client</span></span><br/> | <span data-ttu-id="88946-124">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="88946-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="88946-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88946-125">Minimum supported server</span></span><br/> | <span data-ttu-id="88946-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="88946-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="88946-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88946-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88946-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="88946-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




