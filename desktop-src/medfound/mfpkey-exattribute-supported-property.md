---
description: Especifica si una transformación de Media Foundation (MFT) copia los atributos de los ejemplos de entrada a los ejemplos de salida.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: Propiedad MFPKEY_EXATTRIBUTE_SUPPORTED (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908778"
---
# <a name="mfpkey_exattribute_supported-property"></a><span data-ttu-id="0c9b7-103">\_Propiedad compatible con el MFPKEY EXattribute \_</span><span class="sxs-lookup"><span data-stu-id="0c9b7-103">MFPKEY\_EXATTRIBUTE\_SUPPORTED property</span></span>

<span data-ttu-id="0c9b7-104">Especifica si una transformación de Media Foundation (MFT) copia los atributos de los ejemplos de entrada a los ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-104">Specifies whether a Media Foundation transform (MFT) copies attributes from input samples to output samples.</span></span>



<span data-ttu-id="0c9b7-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c9b7-105">Data type</span></span>

<span data-ttu-id="0c9b7-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="0c9b7-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="0c9b7-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="0c9b7-107">PROPVARIANT member</span></span>

<span data-ttu-id="0c9b7-108">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c9b7-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="0c9b7-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="0c9b7-109">VT\_BOOL</span></span>

<span data-ttu-id="0c9b7-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="0c9b7-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="0c9b7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c9b7-111">Remarks</span></span>

<span data-ttu-id="0c9b7-112">Este atributo puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-112">This attribute can have the following values.</span></span>



| <span data-ttu-id="0c9b7-113">Value</span><span class="sxs-lookup"><span data-stu-id="0c9b7-113">Value</span></span>              | <span data-ttu-id="0c9b7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c9b7-114">Description</span></span>                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9b7-115">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="0c9b7-115">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="0c9b7-116">MFT copia los atributos de los ejemplos de entrada a los ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-116">The MFT copies attributes from the input samples to the output samples.</span></span>                                                                                 |
| <span data-ttu-id="0c9b7-117">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0c9b7-117">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="0c9b7-118">La sesión multimedia copia los atributos de los ejemplos de entrada a los ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-118">The Media Session copies attributes from input samples to output samples.</span></span> <span data-ttu-id="0c9b7-119">No sobrescribe ningún atributo que el MFT establezca en los ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-119">It does not overwrite any attributes that the MFT sets on the output samples.</span></span> |



 

<span data-ttu-id="0c9b7-120">Para obtener este atributo, llame a **QueryInterface** en la MFT para la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="0c9b7-120">To get this attribute, call **QueryInterface** on the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="0c9b7-121">El valor predeterminado es **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-121">The default value is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="0c9b7-122">Si MFT no expone la interfaz **IPropertyStore** o si no se establece esta propiedad, trate el valor como **variante \_ false**.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-122">If the MFT does not expose the **IPropertyStore** interface, or if this property is not set, treat the value as **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="0c9b7-123">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-123">This property is read-only.</span></span>

> [!NOTE] 
> <span data-ttu-id="0c9b7-124">Este atributo no se aplica a MFTs asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-124">This attribute does not apply to asynchronous MFTs.</span></span> <span data-ttu-id="0c9b7-125">Los atributos no se copiarán de los ejemplos de entrada a los ejemplos de salida de MFTs asincrónicos, independientemente del valor de este atributo.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-125">Attributes will not be copied from the input samples to the output samples for asynchronous MFTs, regardless of the value of this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="0c9b7-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0c9b7-126">Examples</span></span>

<span data-ttu-id="0c9b7-127">En el ejemplo siguiente se devuelve VARIANT \_ true si una MFT copia los atributos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0c9b7-127">The following example returns VARIANT\_TRUE if an MFT copies sample attributes.</span></span>


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a><span data-ttu-id="0c9b7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c9b7-128">Requirements</span></span>



| <span data-ttu-id="0c9b7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c9b7-129">Requirement</span></span> | <span data-ttu-id="0c9b7-130">Value</span><span class="sxs-lookup"><span data-stu-id="0c9b7-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9b7-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c9b7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0c9b7-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0c9b7-132">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0c9b7-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c9b7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0c9b7-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c9b7-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0c9b7-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c9b7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c9b7-136"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c9b7-136"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c9b7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c9b7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c9b7-138">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c9b7-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0c9b7-139">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c9b7-139">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c9b7-140">**IMFTransform::P rocessOutput**</span><span class="sxs-lookup"><span data-stu-id="0c9b7-140">**IMFTransform::ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




