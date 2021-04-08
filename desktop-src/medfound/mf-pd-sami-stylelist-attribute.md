---
description: Contiene los nombres descriptivos de los estilos de intercambio de medios accesibles (SAMI) sincronizados definidos en el archivo SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: MF_PD_SAMI_STYLELIST atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913165"
---
# <a name="mf_pd_sami_stylelist-attribute"></a><span data-ttu-id="ac6ba-103">MF \_ PD \_ Sami \_ STYLELIST (atributo)</span><span class="sxs-lookup"><span data-stu-id="ac6ba-103">MF\_PD\_SAMI\_STYLELIST attribute</span></span>

<span data-ttu-id="ac6ba-104">Contiene los nombres descriptivos de los estilos de intercambio de medios accesibles (SAMI) sincronizados definidos en el archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="ac6ba-104">Contains the friendly names of the Synchronized Accessible Media Interchange (SAMI) styles defined in the SAMI file.</span></span>

<span data-ttu-id="ac6ba-105">El [origen de medios Sami](sami-media-source.md) establece este atributo en el descriptor de presentación que crea.</span><span class="sxs-lookup"><span data-stu-id="ac6ba-105">The [SAMI Media Source](sami-media-source.md) sets this attribute on the presentation descriptor that it creates.</span></span>

## <a name="data-type"></a><span data-ttu-id="ac6ba-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ac6ba-106">Data type</span></span>

<span data-ttu-id="ac6ba-107">Byte array</span><span class="sxs-lookup"><span data-stu-id="ac6ba-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="ac6ba-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac6ba-108">Remarks</span></span>

<span data-ttu-id="ac6ba-109">El BLOB de atributo tiene la estructura siguiente:</span><span class="sxs-lookup"><span data-stu-id="ac6ba-109">The attribute blob has the following structure:</span></span>



<span data-ttu-id="ac6ba-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ac6ba-110">Data Type</span></span>

<span data-ttu-id="ac6ba-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac6ba-111">Description</span></span>

<span data-ttu-id="ac6ba-112">Tamaño (bytes)</span><span class="sxs-lookup"><span data-stu-id="ac6ba-112">Size (bytes)</span></span>

<span data-ttu-id="ac6ba-113">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="ac6ba-113">**DWORD**</span></span>

<span data-ttu-id="ac6ba-114">Número de cadenas de estilo.</span><span class="sxs-lookup"><span data-stu-id="ac6ba-114">Number of style strings.</span></span>

<span data-ttu-id="ac6ba-115">4</span><span class="sxs-lookup"><span data-stu-id="ac6ba-115">4</span></span>

<span data-ttu-id="ac6ba-116">Para cada cadena de estilo:</span><span class="sxs-lookup"><span data-stu-id="ac6ba-116">For each style string:</span></span>

<span data-ttu-id="ac6ba-117">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="ac6ba-117">**DWORD**</span></span>

<span data-ttu-id="ac6ba-118">Tamaño de la cadena en bytes, incluido el carácter **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ac6ba-118">Size of the string in bytes, including the **NULL** character.</span></span>

<span data-ttu-id="ac6ba-119">4</span><span class="sxs-lookup"><span data-stu-id="ac6ba-119">4</span></span>

<span data-ttu-id="ac6ba-120">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ac6ba-120">**LPWSTR**</span></span>

<span data-ttu-id="ac6ba-121">Cadena de caracteres anchos terminada en null que contiene el nombre del estilo.</span><span class="sxs-lookup"><span data-stu-id="ac6ba-121">Null-terminated wide-character string containing the name of the style.</span></span>

<span data-ttu-id="ac6ba-122">Varía</span><span class="sxs-lookup"><span data-stu-id="ac6ba-122">Varies</span></span>



 

<span data-ttu-id="ac6ba-123">Para establecer el estilo o recuperar el estilo actual, use la interfaz [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .</span><span class="sxs-lookup"><span data-stu-id="ac6ba-123">To set the style or retrieve the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span>

<span data-ttu-id="ac6ba-124">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ac6ba-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="ac6ba-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ac6ba-125">Examples</span></span>


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="ac6ba-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac6ba-126">Requirements</span></span>



| <span data-ttu-id="ac6ba-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac6ba-127">Requirement</span></span> | <span data-ttu-id="ac6ba-128">Value</span><span class="sxs-lookup"><span data-stu-id="ac6ba-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac6ba-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac6ba-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ac6ba-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ac6ba-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ac6ba-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac6ba-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ac6ba-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac6ba-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ac6ba-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac6ba-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac6ba-134"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac6ba-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac6ba-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac6ba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac6ba-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac6ba-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ac6ba-137">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="ac6ba-137">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="ac6ba-138">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="ac6ba-138">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="ac6ba-139">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ac6ba-139">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ac6ba-140">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="ac6ba-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="ac6ba-141">Origen de medios SAMI</span><span class="sxs-lookup"><span data-stu-id="ac6ba-141">SAMI Media Source</span></span>](sami-media-source.md)
</dt> </dl>

 

 




