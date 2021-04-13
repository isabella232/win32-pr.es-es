---
description: Habilita el uso de una transformación de Media Foundation asincrónica (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: MF_TRANSFORM_ASYNC_UNLOCK atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543227"
---
# <a name="mf_transform_async_unlock-attribute"></a><span data-ttu-id="86aad-103">MF \_ transformar \_ \_ atributo Async Unlock</span><span class="sxs-lookup"><span data-stu-id="86aad-103">MF\_TRANSFORM\_ASYNC\_UNLOCK attribute</span></span>

<span data-ttu-id="86aad-104">Habilita el uso de una transformación de Media Foundation asincrónica (MFT).</span><span class="sxs-lookup"><span data-stu-id="86aad-104">Enables the use of an asynchronous Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="86aad-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="86aad-105">Data type</span></span>

<span data-ttu-id="86aad-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="86aad-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="86aad-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="86aad-107">Get/set</span></span>

<span data-ttu-id="86aad-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="86aad-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="86aad-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="86aad-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="86aad-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86aad-110">Remarks</span></span>

<span data-ttu-id="86aad-111">Los MFTs asincrónicos no son compatibles con versiones anteriores de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="86aad-111">Asynchronous MFTs are not compatible with earlier versions of Microsoft Media Foundation.</span></span> <span data-ttu-id="86aad-112">Para evitar que las aplicaciones existentes usen accidentalmente un MFT asincrónico, este atributo debe establecerse en un valor distinto de cero antes de que se pueda usar una MFT asincrónica.</span><span class="sxs-lookup"><span data-stu-id="86aad-112">To prevent existing applications from accidentally using an asynchronous MFT, this attribute must be set to a nonzero value before an asynchronous MFT can be used.</span></span> <span data-ttu-id="86aad-113">La canalización de Media Foundation establece automáticamente el atributo, de modo que la mayoría de las aplicaciones no necesitan usar este atributo.</span><span class="sxs-lookup"><span data-stu-id="86aad-113">The Media Foundation pipeline automatically sets the attribute, so that most applications do not need to use this attribute.</span></span> <span data-ttu-id="86aad-114">Sin embargo, si una aplicación usa un MFT asincrónico fuera de la canalización de Media Foundation, la aplicación debe establecer este atributo.</span><span class="sxs-lookup"><span data-stu-id="86aad-114">However, if an application uses an asynchronous MFT outside of the Media Foundation pipeline, the application must set this attribute.</span></span>

<span data-ttu-id="86aad-115">Los MFTs sincrónicos no requieren este atributo.</span><span class="sxs-lookup"><span data-stu-id="86aad-115">Synchronous MFTs do not require this attribute.</span></span>

<span data-ttu-id="86aad-116">Para probar si una MFT es asincrónica, obtenga el valor del atributo [MF \_ Transform \_ Async](mf-transform-async.md) en la MFT.</span><span class="sxs-lookup"><span data-stu-id="86aad-116">To test whether an MFT is asynchronous, get the value of the [MF\_TRANSFORM\_ASYNC](mf-transform-async.md) attribute on the MFT.</span></span>

## <a name="examples"></a><span data-ttu-id="86aad-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="86aad-117">Examples</span></span>

<span data-ttu-id="86aad-118">El código siguiente desbloquea una MFT asincrónica.</span><span class="sxs-lookup"><span data-stu-id="86aad-118">The following code unlocks an asynchronous MFT.</span></span>


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="86aad-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86aad-119">Requirements</span></span>



| <span data-ttu-id="86aad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="86aad-120">Requirement</span></span> | <span data-ttu-id="86aad-121">Value</span><span class="sxs-lookup"><span data-stu-id="86aad-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86aad-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86aad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="86aad-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="86aad-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="86aad-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86aad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="86aad-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="86aad-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="86aad-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86aad-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="86aad-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="86aad-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86aad-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="86aad-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86aad-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86aad-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="86aad-130">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="86aad-130">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="86aad-131">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="86aad-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




