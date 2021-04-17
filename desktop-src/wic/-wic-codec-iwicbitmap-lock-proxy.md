---
description: Función de proxy para el método lock.
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: IWICBitmap_Lock_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf07a0afc0fbd2629ffe54b543271014d5817d71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677363"
---
# <a name="iwicbitmap_lock_proxy-function"></a><span data-ttu-id="7487c-103">IWICBitmap \_ \_ función proxy de bloqueo</span><span class="sxs-lookup"><span data-stu-id="7487c-103">IWICBitmap\_Lock\_Proxy function</span></span>

<span data-ttu-id="7487c-104">Función de proxy para el método [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) .</span><span class="sxs-lookup"><span data-stu-id="7487c-104">Proxy function for the [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7487c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7487c-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a><span data-ttu-id="7487c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7487c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7487c-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7487c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7487c-108">Tipo: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="7487c-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="7487c-109">Puntero a este objeto [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="7487c-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="7487c-110">*prcLock* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7487c-110">*prcLock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7487c-111">Tipo: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="7487c-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="7487c-112">Rectángulo al que se va a obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="7487c-112">The rectangle to be accessed.</span></span>

</dd> <dt>

<span data-ttu-id="7487c-113">_flags \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7487c-113">_flags\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7487c-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7487c-114">Type: **DWORD**</span></span>

<span data-ttu-id="7487c-115">El modo de acceso que desea obtener para el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7487c-115">The access mode you wish to obtain for the lock.</span></span>

</dd> <dt>

<span data-ttu-id="7487c-116">*ppILock* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7487c-116">*ppILock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7487c-117">Tipo: **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span><span class="sxs-lookup"><span data-stu-id="7487c-117">Type: **[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span></span>

<span data-ttu-id="7487c-118">Puntero que recibe la ubicación de memoria bloqueada.</span><span class="sxs-lookup"><span data-stu-id="7487c-118">A pointer that receives the locked memory location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7487c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7487c-119">Return value</span></span>

<span data-ttu-id="7487c-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7487c-120">Type: **HRESULT**</span></span>

<span data-ttu-id="7487c-121">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7487c-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7487c-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7487c-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7487c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7487c-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7487c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7487c-124">Requirements</span></span>



| <span data-ttu-id="7487c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7487c-125">Requirement</span></span> | <span data-ttu-id="7487c-126">Value</span><span class="sxs-lookup"><span data-stu-id="7487c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7487c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7487c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7487c-128">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7487c-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7487c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7487c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7487c-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7487c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7487c-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7487c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7487c-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7487c-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




