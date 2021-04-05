---
description: Especifica si una transformación de Media Foundation (MFT) realiza el procesamiento asincrónico.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: MF_TRANSFORM_ASYNC atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811012"
---
# <a name="mf_transform_async-attribute"></a><span data-ttu-id="b59fc-103">MF \_ transformar \_ atributo Async</span><span class="sxs-lookup"><span data-stu-id="b59fc-103">MF\_TRANSFORM\_ASYNC attribute</span></span>

<span data-ttu-id="b59fc-104">Especifica si una transformación de Media Foundation (MFT) realiza el procesamiento asincrónico.</span><span class="sxs-lookup"><span data-stu-id="b59fc-104">Specifies whether a Media Foundation transform (MFT) performs asynchronous processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="b59fc-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b59fc-105">Data type</span></span>

<span data-ttu-id="b59fc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b59fc-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b59fc-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="b59fc-107">Get/set</span></span>

<span data-ttu-id="b59fc-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b59fc-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b59fc-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b59fc-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b59fc-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b59fc-110">Remarks</span></span>

<span data-ttu-id="b59fc-111">El atributo es un valor booleano:</span><span class="sxs-lookup"><span data-stu-id="b59fc-111">The attribute is a Boolean value:</span></span>

-   <span data-ttu-id="b59fc-112">Si el atributo es distinto de cero, el MFT realiza el procesamiento asincrónico.</span><span class="sxs-lookup"><span data-stu-id="b59fc-112">If the attribute is nonzero, the MFT performs asynchronous processing.</span></span>
-   <span data-ttu-id="b59fc-113">Si el atributo es 0 o no está establecido, el MFT es sincrónico.</span><span class="sxs-lookup"><span data-stu-id="b59fc-113">If the attribute is 0 or not set, the MFT is synchronous.</span></span>

<span data-ttu-id="b59fc-114">Para obtener este atributo, primero llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos de la MFT.</span><span class="sxs-lookup"><span data-stu-id="b59fc-114">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT's attribute store.</span></span> <span data-ttu-id="b59fc-115">Si el método se ejecuta correctamente, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obtener el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="b59fc-115">If that method succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span> <span data-ttu-id="b59fc-116">Si se produce un error en cualquiera de los dos métodos, la MFT es sincrónica.</span><span class="sxs-lookup"><span data-stu-id="b59fc-116">If either of the two methods fails, the MFT is synchronous.</span></span>

<span data-ttu-id="b59fc-117">En el caso de MFTs asincrónico, este atributo debe establecerse en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b59fc-117">For asynchronous MFTs, this attribute must be set to a nonzero value.</span></span> <span data-ttu-id="b59fc-118">En el caso de MFTs sincrónicos, este atributo es opcional, pero debe establecerse en 0 si está presente.</span><span class="sxs-lookup"><span data-stu-id="b59fc-118">For synchronous MFTs, this attribute is optional, but must be set to 0 if present.</span></span>

<span data-ttu-id="b59fc-119">Los MFTs asincrónicos no son compatibles con versiones anteriores de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b59fc-119">Asynchronous MFTs are not compatible with earlier versions of Media Foundation.</span></span> <span data-ttu-id="b59fc-120">Para usar una MFT asincrónica, el cliente debe establecer el atributo [**MF \_ Transform \_ Async \_ Unlock**](mf-transform-async-unlock.md) en la MFT.</span><span class="sxs-lookup"><span data-stu-id="b59fc-120">To use an asynchronous MFT, the client must set the [**MF\_TRANSFORM\_ASYNC\_UNLOCK**](mf-transform-async-unlock.md) attribute on the MFT.</span></span> <span data-ttu-id="b59fc-121">(La canalización de Microsoft Media Foundation realiza este paso automáticamente).</span><span class="sxs-lookup"><span data-stu-id="b59fc-121">(The Microsoft Media Foundation pipeline performs this step automatically.)</span></span>

## <a name="examples"></a><span data-ttu-id="b59fc-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b59fc-122">Examples</span></span>

<span data-ttu-id="b59fc-123">El código siguiente comprueba si un MFT realiza el procesamiento asincrónico.</span><span class="sxs-lookup"><span data-stu-id="b59fc-123">The following code tests whether an MFT performs asynchronous processing.</span></span>


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="b59fc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b59fc-124">Requirements</span></span>



| <span data-ttu-id="b59fc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b59fc-125">Requirement</span></span> | <span data-ttu-id="b59fc-126">Value</span><span class="sxs-lookup"><span data-stu-id="b59fc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b59fc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b59fc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b59fc-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="b59fc-128">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b59fc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b59fc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b59fc-130">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="b59fc-130">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b59fc-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b59fc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b59fc-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b59fc-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b59fc-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b59fc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b59fc-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b59fc-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b59fc-135">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="b59fc-135">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="b59fc-136">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="b59fc-136">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="b59fc-137">**\_desbloqueo asincrónico de transformación MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b59fc-137">**MF\_TRANSFORM\_ASYNC\_UNLOCK**</span></span>](mf-transform-async-unlock.md)
</dt> </dl>

 

 




