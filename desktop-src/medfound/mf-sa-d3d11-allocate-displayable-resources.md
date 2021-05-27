---
description: Especifica si el asignador de ejemplo (SA) de MFT debe asignar la textura subyacente de Direct3D mediante la D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE asignación.
title: MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES (Mftransform.h)
ms.topic: reference
ms.date: 03/31/2018
ms.openlocfilehash: fedcfbe98344dd9b424c1a8ce90e847e98f1af51
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548710"
---
# <a name="mf_sa_d3d_allocate_displayable_resources-attribute"></a><span data-ttu-id="d5de8-103">Atributo ALLOCATE DISPLAYABLE RESOURCES de MF \_ SA \_ D3D \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="d5de8-103">MF\_SA\_D3D\_ALLOCATE\_DISPLAYABLE\_RESOURCES attribute</span></span>

<span data-ttu-id="d5de8-104">Especifica si el asignador de ejemplo (SA) de MFT debe asignar la textura de Direct3D subyacente mediante la [D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) asignación.</span><span class="sxs-lookup"><span data-stu-id="d5de8-104">Specifies if the MFT’s Sample Allocator (SA) should allocate the underlying Direct3D Texture using the [D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> 

## <a name="data-type"></a><span data-ttu-id="d5de8-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d5de8-105">Data type</span></span>

<span data-ttu-id="d5de8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d5de8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d5de8-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5de8-107">Remarks</span></span>

<span data-ttu-id="d5de8-108">Este atributo está disponible con la Windows 10 compilación 20348.</span><span class="sxs-lookup"><span data-stu-id="d5de8-108">This attribute is available staring with Windows 10 build 20348.</span></span> 

> [!NOTE]
> <span data-ttu-id="d5de8-109">El **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE** de miembro de la [D3D11_RESOURCE_MISC_FLAG](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeración estará disponible en una versión futura del SDK.</span><span class="sxs-lookup"><span data-stu-id="d5de8-109">The **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE** member field of the [D3D11_RESOURCE_MISC_FLAG](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration will be available in a future release of the SDK.</span></span>

<span data-ttu-id="d5de8-110">La Media Foundation de plataforma establece el **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** al representar vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5de8-110">The Media Foundation platform layer sets the **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** attribute when rendering video.</span></span> <span data-ttu-id="d5de8-111">Una aplicación también podría optar por establecer este atributo si quiere implementar su propio representador de vídeo y hacer uso de recursos que se pueden mostrar de D3D11.</span><span class="sxs-lookup"><span data-stu-id="d5de8-111">An app could also opt to set this attribute if it wants to implement its own video renderer and make use of D3D11 Displayable Resources.</span></span> 

## <a name="example"></a><span data-ttu-id="d5de8-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5de8-112">Example</span></span>

<span data-ttu-id="d5de8-113">En el ejemplo de código siguiente se muestra el uso del **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** atributo .</span><span class="sxs-lookup"><span data-stu-id="d5de8-113">The following code example demonstrates the usage of the **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** attribute.</span></span>

```cpp
class DecoderMFT : public IMFAttributes, public IMFTransform 
{ 
    //  
    ... Other implementation details ommitted 
    // 

public: 
    // Implementation of IMFAttributes::GetAttributes which is invoked by the MF Topology Loader 
    STDMETHODIMP GetAttribtues(IMFAttributes** attributes) 
    { 
        m_attributes.copyTo(attributes); 
        return S_OK; 
    } 

 

private: 
    // Private method to be called before DecoderMFT initializes its sample pool. 
    // A good place for this to happen is in the method which processes the  
    // 'MFT_MESSAGE_NOTIFY_BEGIN_STREAMING' event. 
    // At a minimum, this processing would be in DecoderMFT's implementation of IMFTransform::ProcessMessage.  

    HRESULT ConfigureTextureFlags() 
    { 
        UINT32 allocateDisplayables = MFGetAttributeUINT32(m_attributes.get(), 
            MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES, 0); 

        // If no MF_SA_* attributes which correspond to D3D misc flags are set then it is valid for 
        // miscFlags to be set to 0. 
        m_textureDesc.miscFlags = 0; 
        UINT32 sharedResources = 0; 

        if (allocateDisplayables != 0) 
        { 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_DISPLAYABLE; 
            // The following flag is required for the decoders output to 
            // use D3D11_RESOURCE_MISC_DISPLAYABLE. 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_EXCLUSIVE_WRITER; 

            // The following flags are required for the presentation API 
            // to consume and present these resources (also known as direct presentation). 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED; 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED_NTHANDLE; 

            sharedResources = 1; 
        } 
        else  
        { 
            // This handles the case when MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES was 0 or missing. 
            sharedResources = MFGetAttributeUINT32(m_attributes.get(), MF_SA_D3D11_SHARED_WITHOUT_MUTEX, 0); 

            if (sharedResources != 0) 
            { 
                m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED; 
            } 
            else 
            { 
                UINT32 sharedKeyMutex = MFGetAttributeUINT32(m_attributes.get(), MF_SA_D3D11_SHARED, 0); 

                if (sharedKeyMutex != 0) 
                { 
                    m_textureDesc.micsFlags |= D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX; 
                } 
            } 
        } 

        // Processing for other MF_SA_* attributes which imply D3D11_RESOURCE_MISC flag 
        // omitted from this sample. 

        return S_OK; 

    } 

    // Private method showing how DecoderMFT can create a texture with the flags required 
    // to satisfy "MF_SA_D3D11_ALLOCATE_DISPLAYBLE_RESOURCES".  
    // Because this is a private function we know the passed in pointer is always valid. 
    // This would be invoked by another private DecoderMFT function when allocating an MFSample 
    // for its sample pool. 

    HRESULT AllocateTextureForSample(ID3D11Texture2D** texture2D) 
    { 
        return m_d3dDevice->CreateTexture2D(&m_textureDesc, nullptr, texture2D); 
    } 

    // ... other members omitted 
    wil::com_ptr_nothrow<IMFAttributes> m_attributes; 
    wil::com_ptr_nothrow<ID3D11Device> m_d3dDevice; 

    // This a texture description for D3D11 resources. 
    D3D11_TEXTURE_2D_DESC m_textureDesc = {}; 

}; 
```

## <a name="requirements"></a><span data-ttu-id="d5de8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5de8-114">Requirements</span></span>



| <span data-ttu-id="d5de8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5de8-115">Requirement</span></span> | <span data-ttu-id="d5de8-116">Value</span><span class="sxs-lookup"><span data-stu-id="d5de8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5de8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5de8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5de8-118">Windows 10 compilación 20348</span><span class="sxs-lookup"><span data-stu-id="d5de8-118">Windows 10 build 20348</span></span><br/>                                    |
| <span data-ttu-id="d5de8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5de8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5de8-120"><dt>Mftransform.h</dt></span><span class="sxs-lookup"><span data-stu-id="d5de8-120"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5de8-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d5de8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5de8-122">Lista alfabética de Media Foundation atributos</span><span class="sxs-lookup"><span data-stu-id="d5de8-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d5de8-123">**ATTRIBUTEAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d5de8-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d5de8-124">**ATTRIBUTEAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d5de8-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d5de8-125">Media Foundation atributos</span><span class="sxs-lookup"><span data-stu-id="d5de8-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




