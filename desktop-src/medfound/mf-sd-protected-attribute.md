---
description: Indica si una secuencia contiene contenido protegido.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: MF_SD_PROTECTED atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717003"
---
# <a name="mf_sd_protected-attribute"></a><span data-ttu-id="38f9f-103">\_ \_ Atributo protegido de MF SD</span><span class="sxs-lookup"><span data-stu-id="38f9f-103">MF\_SD\_PROTECTED attribute</span></span>

<span data-ttu-id="38f9f-104">Indica si una secuencia contiene contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="38f9f-104">Indicates whether a stream contains protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="38f9f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="38f9f-105">Data type</span></span>

<span data-ttu-id="38f9f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="38f9f-106">**UINT32**</span></span>

<span data-ttu-id="38f9f-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="38f9f-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f9f-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38f9f-108">Remarks</span></span>

<span data-ttu-id="38f9f-109">Este atributo se aplica a los descriptores de flujo.</span><span class="sxs-lookup"><span data-stu-id="38f9f-109">This attribute applies to stream descriptors.</span></span> <span data-ttu-id="38f9f-110">Si el valor del atributo es **true**, el flujo contiene contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="38f9f-110">If the value of the attribute is **TRUE**, the stream contains protected content.</span></span> <span data-ttu-id="38f9f-111">Si el valor es **false** o no se establece el atributo, el flujo contiene un contenido sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="38f9f-111">If the value is **FALSE**, or the attribute is not set, the stream contains clear content.</span></span>

<span data-ttu-id="38f9f-112">En lugar de comprobar cada secuencia para este atributo, puede pasar un descriptor de presentación a la función [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) .</span><span class="sxs-lookup"><span data-stu-id="38f9f-112">Instead of checking each stream for this attribute, you can pass a presentation descriptor to the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function.</span></span> <span data-ttu-id="38f9f-113">Esta función comprueba si el descriptor de presentación contiene cualquier flujo protegido.</span><span class="sxs-lookup"><span data-stu-id="38f9f-113">This function tests whether the presentation descriptor contains any protected streams.</span></span>

<span data-ttu-id="38f9f-114">Un origen multimedia debe establecer este atributo en el descriptor de flujo si el contenido requiere la ruta de acceso a medios protegidos (PMP).</span><span class="sxs-lookup"><span data-stu-id="38f9f-114">A media source should set this attribute on the stream descriptor if the content requires the protected media path (PMP).</span></span>

<span data-ttu-id="38f9f-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="38f9f-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="38f9f-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="38f9f-116">Examples</span></span>


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="38f9f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38f9f-117">Requirements</span></span>



| <span data-ttu-id="38f9f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="38f9f-118">Requirement</span></span> | <span data-ttu-id="38f9f-119">Value</span><span class="sxs-lookup"><span data-stu-id="38f9f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="38f9f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38f9f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="38f9f-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="38f9f-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="38f9f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38f9f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="38f9f-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="38f9f-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="38f9f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38f9f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="38f9f-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="38f9f-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38f9f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="38f9f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f9f-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="38f9f-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="38f9f-128">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="38f9f-128">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="38f9f-129">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="38f9f-129">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="38f9f-130">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="38f9f-130">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="38f9f-131">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="38f9f-131">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




